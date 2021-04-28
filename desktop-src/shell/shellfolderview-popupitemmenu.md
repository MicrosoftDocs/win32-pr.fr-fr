---
description: 'Méthode ShellFolderView. PopupItemMenu : crée un menu contextuel pour l’élément spécifié et retourne la chaîne de commande sélectionnée.'
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
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083387"
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

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

**Chaîne** qui reçoit la chaîne de commande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,71 ou ultérieure)</dt> </dl> |



 

 
