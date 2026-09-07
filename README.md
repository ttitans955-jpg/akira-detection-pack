# Akira Ransomware Detection Pack

Detection content derived from the public Paylogix/Akira incident chain
(VPN gateway access -> remote access tool -> staging -> encryption).

## Rules

| Rule | File | MITRE |
|---|---|---|
| VPN gateway spawning shells | `rules/windows/process_creation/akira_vpn_gateway_shell.yml` | T1078.001 |
| Remote Access Tool deployment | `rules/windows/process_creation/akira_remote_access_tool_deploy.yml` | T1219 |
| WinRAR staging pattern | `rules/windows/process_creation/akira_winrar_staging.yml` | T1560.001 |
| Ransom note / `.akira` marker | `rules/windows/file_rename/akira_ransom_note_creation.yml` | T1486 |

See `convert.md` for SIEM conversion (Sigma CLI).