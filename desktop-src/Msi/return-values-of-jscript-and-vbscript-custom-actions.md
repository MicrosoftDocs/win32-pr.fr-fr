---
description: les actions personnalisées écrites dans JScript ou Visual Basic, scripting Edition (VBScript) peuvent appeler une fonction facultative. Ces fonctions doivent retourner l’une des valeurs indiquées dans le tableau suivant.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: valeurs de retour des Actions personnalisées JScript et VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50a2b225c59b0e4d1787f2eaceeb094d6fb2abe7f9d9600822b6295ef2dd273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626089"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>valeurs de retour des Actions personnalisées JScript et VBScript

les actions personnalisées écrites dans JScript ou Visual Basic, scripting Edition (VBScript) peuvent appeler une fonction facultative. Ces fonctions doivent retourner l’une des valeurs indiquées dans le tableau suivant.



| Valeur retournée              | Valeur        | Description                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msiDoActionStatusNoAction | 0            | Action non exécutée.                                                                                       |
| msiDoActionStatusSuccess  | IDOK = 1     | Action terminée avec succès.                                                                             |
| msiDoActionStatusUserExit | IDCANCEL = 2 | Arrêt prématuré par l’utilisateur.                                                                             |
| msiDoActionStatusFailure  | IDABORT = 3  | Erreur irrécupérable. retourné en cas d’erreur lors de l’analyse ou de l’exécution du JScript ou de VBScript. |
| msiDoActionStatusSuspend  | IDRETRY = 4  | Séquence suspendue à reprendre ultérieurement.                                                                    |
| msiDoActionStatusFinished | IDIGNORE = 5 | Ignorer les actions restantes. N’est pas une erreur.                                                                      |



 

notez que Windows Installer traduit les valeurs de retour de toutes les actions lorsqu’il écrit la valeur de retour dans le fichier journal. Par exemple, si la valeur de retour de l’action apparaît comme 1 (un) dans le fichier journal, cela signifie que l’action a retourné msiDoActionStatusSuccess. Pour plus d’informations sur cette traduction, consultez [journalisation des valeurs de retour d’action](logging-of-action-return-values.md).

Pour retourner une valeur autre que la réussite à partir d’une action personnalisée de script, vous devez utiliser une cible de fonction pour l’action personnalisée. La fonction cible est spécifiée dans la colonne cible de la [table CustomAction](customaction-table.md).

L’exemple de script suivant montre comment retourner la réussite ou l’échec d’une action personnalisée VBScript.


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



Si ce VBScript était incorporé dans la [table binaire](binary-table.md) du package d’installation comme MyCA.vbs, l’entrée de la [table CustomAction](customaction-table.md) du script serait la suivante :



| Action         | Type | Source   | Cible       |
|----------------|------|----------|--------------|
| MyCustomAction | 6    | MyCA.vbs | MyVBScriptCA |



 

 

 



