---
description: Envoie un message au contrôle spécifié dans une boîte de dialogue.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535891"
---
# <a name="_senddlgitemmessage-function"></a>\_SendDlgItemMessage fonction)

\[Cette fonction est un wrapper sur la fonction **SendDlgItemMessage** . Cette fonction peut être modifiée ou non disponible à l’avenir. Les applications doivent appeler **SendDlgItemMessage** directement.\]

Envoie un message au contrôle spécifié dans une boîte de dialogue. Consultez [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).

## <a name="syntax"></a>Syntaxe


```C++
LRESULT _SendDlgItemMessage(
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

[**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
