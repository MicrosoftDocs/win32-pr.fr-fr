---
description: Avertit un appbar que l’utilisateur a sélectionné la commande cascade, mosaïque horizontale ou Mosaïque verticale à partir du menu contextuel de la barre des tâches.
title: Message ABN_WINDOWARRANGE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 27c679b7ccdb5eb92ebe87676cd136c71adcda862472f6f300056511001a683a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225020"
---
# <a name="abn_windowarrange-message"></a>Message d’ABN \_ WINDOWARRANGE

Avertit un appbar que l’utilisateur a sélectionné la commande cascade, mosaïque horizontale ou Mosaïque verticale à partir du menu contextuel de la barre des tâches.


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fBeginning* 
</dt> <dd>

Indicateur spécifiant si l’opération de cascade ou de vignette commence. Ce paramètre a la **valeur true** si l’opération commence et que les fenêtres n’ont pas encore été déplacées. La **valeur est false** si l’opération est terminée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Le système envoie le message de notification à deux reprises avec *lParam* défini à **true** , puis avec *lParam* défini sur **false**. La première notification est envoyée avant que les fenêtres soient mises en cascade ou en mosaïque, et la seconde est envoyée après l’opération de mise en cascade ou de vignette.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




