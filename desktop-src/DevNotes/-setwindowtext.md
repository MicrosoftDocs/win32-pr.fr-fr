---
description: Modifie le texte de la barre de titre de la fenêtre spécifiée (le cas échéant).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: _SetWindowText fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: a0c66230d9e7f074fe50ca826ab196ab75a239942257899362b738296b329074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572551"
---
# <a name="_setwindowtext-function"></a>\_SetWindowText fonction)

\[Cette fonction est un wrapper sur la fonction **SetWindowText** . Cette fonction peut être modifiée ou non disponible à l’avenir. Les applications doivent appeler **SetWindowText** directement.\]

Modifie le texte de la barre de titre de la fenêtre spécifiée (le cas échéant). Consultez [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).

## <a name="syntax"></a>Syntaxe


```C++
BOOL _SetWindowText(
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

[**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
