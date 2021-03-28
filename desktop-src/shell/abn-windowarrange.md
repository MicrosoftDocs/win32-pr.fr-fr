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
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525420"
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

## <a name="remarks"></a>Notes

Le système envoie le message de notification à deux reprises avec *lParam* défini à **true** , puis avec *lParam* défini sur **false**. La première notification est envoyée avant que les fenêtres soient mises en cascade ou en mosaïque, et la seconde est envoyée après l’opération de mise en cascade ou de vignette.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



 

 




