---
description: Envoie le message spécifié à une fenêtre ou à des fenêtres.
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: _SendMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: bdd8a072970d8e6fb5e9af082f6f220531539a1c0061a7688d48be30dd659a7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572569"
---
# <a name="_sendmessage-function"></a>\_SendMessage, fonction

\[Cette fonction est un wrapper sur la fonction **SendMessage** . Cette fonction peut être modifiée ou non disponible à l’avenir. Les applications doivent appeler **SendMessage** directement.\]

Envoie le message spécifié à une fenêtre ou à des fenêtres. Consultez [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).

## <a name="syntax"></a>Syntaxe


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
