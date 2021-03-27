---
description: Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.
title: Méthode ShellFolderView. PopupItemMenu (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209940"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>Méthode ShellFolderView. PopupItemMenu

Crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.

## <a name="syntax"></a>Syntaxe


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vItem* \[ dans\]
</dt> <dd>

Type : **variante**

Objet [**FolderItem**](folderitem.md) pour lequel le menu contextuel sera créé.

</dd> <dt>

*VX* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Position horizontale du menu, en coordonnées d’écran.

</dd> <dt>

*Vy* \[ dans, facultatif\]
</dt> <dd>

Type : **variante**

Position verticale du menu, en coordonnées d’écran.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

_ *String** qui reçoit la chaîne de commande.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
