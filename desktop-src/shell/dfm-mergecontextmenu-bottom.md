---
description: Autorise le rappel à ajouter des éléments en bas du menu étendu.
title: Message DFM_MERGECONTEXTMENU_BOTTOM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 37414335-4f3c-461e-bd05-d6ef850f972a
api_name:
- DFM_MERGECONTEXTMENU_BOTTOM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b9274a36f531e53f86d05adab20b4970ea5ace84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972014"
---
# <a name="dfm_mergecontextmenu_bottom-message"></a>\_Message DFM MERGECONTEXTMENU \_ Bottom

Autorise le rappel à ajouter des éléments en bas du menu étendu.


```C++
DFM_MERGECONTEXTMENU_BOTTOM

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pqcminfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) contenant les informations utilisées dans la fusion.

</dd> <dt>

*uFlags* \[ dans\]
</dt> <dd>

Indicateurs spécifiant comment le menu contextuel peut être modifié. Ce paramètre utilise les \_ \* valeurs CMF décrites dans [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="remarks"></a>Notes

Si des éléments sont ajoutés au menu contextuel étendu, ils doivent être pris en charge avec les routines qui répondent de manière appropriée lorsque l’un de ces éléments est appelé à l’aide de [**DFM \_ commande InvokeCommand**](dfm-invokecommand.md).

Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est construit. Il existe deux API pour sa construction, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel. Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




