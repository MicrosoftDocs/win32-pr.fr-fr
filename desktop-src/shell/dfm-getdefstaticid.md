---
description: Envoyé par l’implémentation du menu contextuel par défaut lors de la création, en spécifiant la commande de menu par défaut et en autorisant l’autre choix à effectuer. Utilisé par LPFNDFMCALLBACK.
title: Message DFM_GETDEFSTATICID (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393440"
---
# <a name="dfm_getdefstaticid-message"></a>\_Message DFM GETDEFSTATICID

Envoyé par l’implémentation du menu contextuel par défaut lors de la création, en spécifiant la commande de menu par défaut et en autorisant l’autre choix à effectuer. Utilisé par [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*defaultID* \[ in, out\]
</dt> <dd>

Pointeur vers l’ID de la commande de menu sélectionnée. L’indicateur suivant est reconnu.

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Propriétés de cmd DFM \_**


</dt> <dd>

Affichez l’interface utilisateur des **Propriétés** de l’élément sur lequel le menu a été appelé.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Pour remplacer le choix de commande par défaut, votre gestionnaire doit, lors de la réception de ce message, définir la valeur pointée par *defaultID* sur l’ID de la commande de remplacement et retourner \_ OK. Sinon, retourne un code d’échec.

Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est construit. Il existe deux API pour sa construction, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel. Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
