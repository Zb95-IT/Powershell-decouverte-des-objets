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


##  Historique
 Get-History

  Id CommandLine                                                                                                                                                                                                      
  -- -----------                                                                                                                                                                                                      
   1 $AllProcess | Select-Object -Property Name                                                                                                                                                                       
   2 Set-Location                                                                                                                                                                                                     
   3 Get-ChildItem                                                                                                                                                                                                    
   4 Start-Process calc                                                                                                                                                                                               
   5 $AllProcess = Get-Process                                                                                                                                                                                        
   6 $AllProcess | Where-Object {$_.Name -like "*calc*"}                                                                                                                                                              
   7 $AllProcess | Where-Object {$_.Name -like "*alcul*"}                                                                                                                                                             
   8 $AllProcess | Where-Object {$_.Name -like "*alcul*"} Select-Object -Property Name                                                                                                                                
   9 $AllProcess | Where-Object {$_.Name -like "*alcul*"} Select-Object -Property calc                                                                                                                                
  10 $AllProcess | Where-Object {$_.Name -like "*calc*"}                                                                                                                                                              
  11 Start-Process calc.exe...                                                                                                                                                                                        
  12 Get-Process | Select-Object -Property calculatrice                                                                                                                                                               
  13 Get-Process | Select-Object -Property Calculatrice                                                                                                                                                               
  14 Get-Process                                                                                                                                                                                                      
  15 Get-Process | Select-Object -Property CalculatorApp                                                                                                                                                              
  16 $AllProcess | Where-Object {$_.Name -like "*Calculator*"}                                                                                                                                                        
  17 $AllProcess = Get-Process...                                                                                                                                                                                     
