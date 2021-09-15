---
description: Transfère les événements de l’objet ShellFolderView spécifié au gestionnaire d’événements ShellFolderViewOC correspondant.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Méthode ShellFolderViewOC. SetFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412345"
---
# <a name="shellfolderviewocsetfolderview-method"></a>Méthode ShellFolderViewOC. SetFolderView

Transfère les événements de l’objet [**ShellFolderView**](shellfolderview.md) spécifié au gestionnaire d’événements [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondant.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*oShellFolderView* \[ dans\]
</dt> <dd>

Type : **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\***

Objet [**ShellFolderView**](shellfolderview.md) . Ses événements [**EnumDone**](shellfolderviewoc-enumdone.md) et [**SelectionChanged**](shellfolderview-selectionchanged.md) seront transmis au gestionnaire d’événements [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondant.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



 

 
