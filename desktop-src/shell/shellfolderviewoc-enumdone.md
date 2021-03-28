---
description: Indique que l’objet ShellFolderView a terminé l’énumération du contenu du dossier.
title: Événement ShellFolderViewOC. EnumDone (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 3ce02fd418a93ec5914c438fcad39d8dc73c5c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991717"
---
# <a name="shellfolderviewocenumdone-event"></a>Événement ShellFolderViewOC. EnumDone

Indique que l’objet [**ShellFolderView**](shellfolderview.md) a terminé l’énumération du contenu du dossier.

## <a name="syntax"></a>Syntaxe


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a>Paramètres

Ce gestionnaire d’événements n’a aucun paramètre.

## <a name="remarks"></a>Notes

L’objet [**ShellFolderView**](shellfolderview.md) doit énumérer le contenu d’un dossier avant de pouvoir l’afficher. Dans le cas de dossiers volumineux ou situés sur un système distant, ce processus peut prendre plusieurs minutes. Pendant ce temps, un graphique Torch animé s’affiche pour indiquer à l’utilisateur que le traitement est en cours. Une fois l’énumération terminée, l’événement **EnumDone** est déclenché et le graphique de torche est remplacé par le contenu du dossier.

Fournissez le code de gestion des événements pour cet événement, comme indiqué ici.


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




