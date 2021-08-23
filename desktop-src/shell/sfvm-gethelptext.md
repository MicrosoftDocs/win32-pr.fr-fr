---
description: 'Permet à l’objet de rappel de spécifier une chaîne de texte d’aide pour les éléments de menu ou les boutons de barre d’outils. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_GETHELPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c015c1999cbd60174da1994d92766b4f334630294767ee390be21340aef97cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661019"
---
# <a name="sfvm_gethelptext-message"></a>\_Message SFVM GETHELPTEXT

Permet à l’objet de rappel de spécifier une chaîne de texte d’aide pour les éléments de menu ou les boutons de barre d’outils. Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTEXT 

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

Chaîne terminée par le caractère null qui contient le texte d’aide.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
