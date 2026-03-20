# Exercice PowerShell — Filtrer un processus

## Commandes utilisées
```powershell
Start-Process calc
$AllProcess = Get-Process
$AllProcess | Where-Object {$_.Name -like "*Calculator*"}
```

## Remarque
La variable `$AllProcess` doit être créée **après** le lancement de la calculatrice sinon elle n'aura pas le process de la calculatrice en cours.
Sur Windows 11 la calculatrice s'appelle `CalculatorApp` et non `calc`.

## Historique des commandes

| Id | CommandLine |
|----|-------------|
| 1 | `$AllProcess \| Select-Object -Property Name` |
| 4 | `Start-Process calc` |
| 5 | `$AllProcess = Get-Process` |
| 6 | `$AllProcess \| Where-Object {$_.Name -like "*calc*"}` |
| 10 | `$AllProcess \| Where-Object {$_.Name -like "*calc*"}` |
| 14 | `Get-Process` |
| 16 | `$AllProcess \| Where-Object {$_.Name -like "*Calculator*"}` |
| 17 | `$AllProcess = Get-Process` |                                                                                                                                                                              
