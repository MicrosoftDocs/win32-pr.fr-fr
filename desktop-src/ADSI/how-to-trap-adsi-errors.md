---
title: Interruption des erreurs ADSI
description: VBScript offre une seule façon d’intercepter les erreurs de gestion des erreurs en ligne.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd66283d2427c2c42162ce46a0a66ecbda87737cf2572d183ebdb0017232e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082533"
---
# <a name="how-to-trap-adsi-errors"></a>Interruption des erreurs ADSI

VBScript offre une seule façon d’intercepter les erreurs : la gestion des erreurs en ligne. Un gestionnaire d’erreurs Inline commence par l’instruction **On Error Resume Next** . Étant donné que **en cas d’erreur, Resume Next** empêchera toute erreur d’arrêter l’exécution du script jusqu’à ce que la fin de l’étendue à partir de laquelle en cas de reprise de l' **erreur suivante** soit appelée, vous devez vérifier la valeur de **Err** à chaque point après l’instruction **On Error Resume Next** où vous vous attendez à ce qu’une erreur se produise. L’exemple suivant illustre la gestion des erreurs inline dans un script ADSI :


```VB
On Error Resume Next

Set myComputer = GetObject(computerPath)
If Err Then AdsiErr()

' Create the new user account
Set newUser = myComputer.Create("user", username)
newUser.SetInfo
If Err Then AdsiErr()

Sub AdsiErr()
    Dim s
    Dim e
    
    If Err.Number = &H8000500E Then
        WScript.Echo "The user " & username & " already exists."
    Elseif Err.Number = &H80005000 Then
        WScript.Echo "Computer " & computerPath & " not found.  Check the ADsPath and try again."
    Else
        e = Hex(Err.Number)
        WScript.Echo "Unexpected Error " & e & "(" & Err.Number & ")"
    End If
    WScript.Quit(1)

End Sub
```



Après chaque emplacement où le script est susceptible de rencontrer une erreur, il existe une instruction **If Err** . L’objet **Err** contient le code d’erreur de la dernière erreur qui s’est produite pendant l’exécution du script. Si aucune erreur ne s’est produite, **Err** a toujours la valeur zéro (0). Dans l’exemple précédent, une erreur entraîne l’interruption de l’exécution de la sous-routine **AdsiErr** , qui vérifie la valeur de **Err. Number** pour les erreurs attendues. Au lieu de détourner avec un message d’erreur énigmatique, le script vous donnera une explication plus efficace pour la raison de l’arrêt de l’exécution.

N’oubliez pas que dans l’étendue dans laquelle la **fonction de reprise** après l’erreur est appelée, toute erreur qui se produit après l’appel **suivant de l’erreur de reprise** sera ignorée. Cela peut en fait compliquer le débogage d’un script si vous oubliez de vérifier la valeur de **Err** dans les emplacements appropriés. Chaque fois que vous vous attendez à ce qu’une erreur soit probable, veillez à vérifier la valeur de **Err**.

(Lorsque vous déboguez initialement le script, vous pouvez simplement laisser le script arrêter son exécution et afficher le numéro de ligne incriminé sur une erreur, puis ajouter les gestionnaires d’erreurs une fois que le déroulement du programme de base est correct.)

 

 




