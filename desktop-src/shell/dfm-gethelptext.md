---
description: 'DFM_GETHELPTEXT message : permet à l’objet de rappel de spécifier une chaîne de texte d’aide.'
title: Message DFM_GETHELPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d1035ae82a8caf4c9ada5a859663d0d20286b433a9bf527831c29157d8dd6894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860934"
---
# <a name="dfm_gethelptext-message"></a>\_Message DFM GETHELPTEXT

Permet à l’objet de rappel de spécifier une chaîne de texte d’aide.


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*idCmd \_ cchMax* \[ dans\]
</dt> <dd>

Le mot de poids faible de ce paramètre contient l’ID de commande. Le mot de poids fort contient le nombre de caractères dans la mémoire tampon *pszText* .

</dd> <dt>

*pszText* \[ à\]
</dt> <dd>

Chaîne ANSI se terminant par un caractère null qui contient le texte d’aide.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est construit. Il existe deux API pour sa construction, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel. Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DFM \_ GETHELPTEXT** (ANSI)<br/>                                              |



 

 




