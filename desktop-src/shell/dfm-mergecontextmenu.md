---
description: Autorise le rappel à ajouter des éléments au menu.
title: Message DFM_MERGECONTEXTMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2fd779ac-7dd6-4b81-86dc-8930db27ae59
api_name:
- DFM_MERGECONTEXTMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ddd071e40d3c017a513eb0e85efb634df530a8686afaf7df59b922602d37f22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455969"
---
# <a name="dfm_mergecontextmenu-message"></a>\_Message DFM MERGECONTEXTMENU

Autorise le rappel à ajouter des éléments au menu.


```C++
DFM_MERGECONTEXTMENU

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

## <a name="remarks"></a>Remarques

Si des éléments sont ajoutés au menu contextuel, ils doivent être pris en charge avec les routines qui répondent de manière appropriée lorsque l’un de ces éléments est appelé à l’aide de [**DFM \_ commande InvokeCommand**](dfm-invokecommand.md).

Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est implémenté. Il existe deux API pour son implémentation, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel. Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




