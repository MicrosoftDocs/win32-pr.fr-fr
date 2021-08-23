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
ms.openlocfilehash: 3a1c17ab1ad303ce95755140ebe7f264b976471c7ecfa507f2152ec9e0ad221c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538833"
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

 

 
