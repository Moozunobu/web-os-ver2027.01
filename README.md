
設定ファイルの集約 (/src/config/osVersions.ts):
新しい OS バージョンや URL を追加・変更したい場合は、/src/config/osVersions.ts 内の OS_VERSIONS 配列にオブジェクトを1行追加するだけで完了します。
code
TypeScript
export const OS_VERSIONS: OSVersionConfig[] = [
  {
    id: 'os_version7.5',
    name: 'os_version7.5',
    url: 'https://moozunobu.github.io/web-os-ver7.5/',
    aliases: ['7.5', 'version7.5', 'ver7.5'],
  },
  {
    id: 'os_version7.2',
    name: 'os_version7.2',
    url: 'https://moozunobu.github.io/noob-web-os-ver7.2/',
    aliases: ['7.2', 'version7.2', 'ver7.2'],
  },
  // 💡 新しいバージョンを追加したい場合は、ここに1行追加するだけで自動的にコマンドや選択リストに反映されます。
];
ターミナルコマンドの動的連動:
ver または select-os コマンドを実行した際の番号指定リスト（1, 2...）や、直接のバージョン入力（例: 7.5, os_version7.5）が、すべて設定ファイルから動的に取得・判定されるようになりました。
