---
description: 'Permet à l’objet de rappel de fournir une page à ajouter à la feuille de propriétés de propriétés de l’objet sélectionné. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_ADDPROPERTYPAGES (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991665"
---
# <a name="sfvm_addpropertypages-message"></a>\_Message SFVM ADDPROPERTYPAGES

Permet à l’objet de rappel de fournir une page à ajouter à la feuille de propriétés de **Propriétés** de l’objet sélectionné. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pData* \[ à\]
</dt> <dd>

Adresse d’une structure [**de \_ \_ données de PropPage SFVM**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .

</dd> </dl>

## <a name="remarks"></a>Notes

Ce message sert essentiellement la même fonction que [**IShellPropSheetExt :: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Pour plus d’informations, consultez [création de gestionnaires de feuille de propriétés](propsheet-handlers.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
