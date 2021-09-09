# PowerShell

[Microsoft PowerShell for Beginners](https://www.youtube.com/watch?v=IHrGresKu2w)

## Commands
| Command | Function |
| --- | --- |
| Start-Transcript | Logs a transcript of session & commands |
| Get-Commands | returns all commands |
| `get-command -Noun service` | pulls all things related to the service object |
| `get-help Get-Service -Examples` | provides in-terminal example |
| `get-help Get-Service -Online` | goes do online example |
| `Get-Member` | all the properties and methods on an object |

## Aliases
`get-alias`

## Piping
`Get-Process -Name MicrosoftEdge | Get-Member`

`Get-Process -Name MicrosoftEdge | select-object *`

## Variables
Always prefaced with a `$` sign
| Command | Function |
| --- | --- |
| `$foo = Get-Process MicrosoftEdge` | assign object to variable |
| `$foo.Name` | to get name |
| `$foo.Kill()` | to end process |