---
title: Message EM_SETEDITSTYLEEX (RichEdit. h)
description: Définit les indicateurs de style de modification étendu actuels.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- EM_SETEDITSTYLEEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942663"
---
# <a name="em_seteditstyleex-message"></a>\_Message SETEDITSTYLEEX em

Définit les indicateurs de style de modification étendu actuels.


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie un ou plusieurs indicateurs de style de modification étendus. Pour obtenir la liste des valeurs possibles, consultez [**em \_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).

</dd> <dt>

*lParam* 
</dt> <dd>

Masque composé d’une ou plusieurs des valeurs *wParam* . Seules les valeurs spécifiées dans ce masque seront définies ou désactivées. Cela permet de définir ou d’effacer un seul indicateur sans lire les États de l’indicateur actuel.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est l’état des indicateurs de style de modification étendus après que la modification enrichie a tenté d’implémenter vos modifications de style de modification. Les indicateurs de style de modification sont un ensemble d’indicateurs qui indiquent le style d’édition actuel.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETEDITSTYLEEX em**](em-geteditstyleex.md)
</dt> </dl>

 

