---
description: Distribue les messages entrants envoyés, vérifie la file d’attente de messages de thread pour un message publié et récupère le message (le cas échéant).
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532779"
---
# <a name="_peekmessage-function"></a>\_PeekMessage, fonction

\[Cette fonction est un wrapper sur la fonction **PeekMessage** . Cette fonction peut être modifiée ou non disponible à l’avenir. Les applications doivent appeler **PeekMessage** directement.\]

Distribue les messages entrants envoyés, vérifie la file d’attente de messages de thread pour un message publié et récupère le message (le cas échéant). Consultez [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).

## <a name="syntax"></a>Syntaxe


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll ; </dt> <dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
