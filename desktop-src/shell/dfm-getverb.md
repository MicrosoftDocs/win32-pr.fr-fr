---
description: Envoyé par l’implémentation du menu contextuel par défaut pour obtenir le verbe pour l’ID de commande donné dans le menu contextuel.
title: Message DFM_GETVERB (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201268"
---
# <a name="dfm_getverb-message"></a>\_Message DFM GETVERB

Envoyé par l’implémentation du menu contextuel par défaut pour obtenir le verbe pour l’ID de commande donné dans le menu contextuel.


```C++

                DFM_GETVERB 

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

Pointeur vers une chaîne se terminant par un caractère null qui contient le texte de verbe.

</dd> </dl>

## <a name="remarks"></a>Notes

Ce message est envoyé à la fonction de rappel ou à l’objet de rappel, en fonction de la façon dont l’objet de menu contextuel par défaut est construit. Il existe deux API pour sa construction, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).

[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) est une version étendue de ce message et fournit plus d’informations sur le rappel. Utilisez **DFM \_ INVOKECOMMANDEX** si les informations supplémentaires fournies par cette interface sont nécessaires dans votre implémentation de.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **DFM \_ GETVERBW** (Unicode) et **DFM \_ GETVERBA** (ANSI)<br/>                 |



 

 




