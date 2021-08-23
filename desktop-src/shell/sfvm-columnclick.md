---
description: 'Notifie l’objet de rappel sur lequel l’utilisateur a cliqué sur un en-tête de colonne pour trier la liste d’objets dans l’affichage des dossiers. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_COLUMNCLICK (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d5ebd98ebc887d26bcee4799ffa3412df803fd0dfa099ac41bc69e1c25d83f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592699"
---
# <a name="sfvm_columnclick-message"></a>\_Message SFVM COLUMNCLICK

Notifie l’objet de rappel sur lequel l’utilisateur a cliqué sur un en-tête de colonne pour trier la liste d’objets dans l’affichage des dossiers. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IColumn* \[ dans\]
</dt> <dd>

Index de la colonne sur laquelle l’utilisateur a cliqué.

</dd> </dl>

## <a name="remarks"></a>Remarques

En réponse à cette notification, vous devez retourner S \_ OK pour réorganiser la liste vous-même. Pour que l’objet de vue de dossier système réorganise la liste, retourne la \_ valeur false.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
