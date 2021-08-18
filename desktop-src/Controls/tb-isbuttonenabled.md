---
title: Message TB_ISBUTTONENABLED (commctrl. h)
description: Détermine si le bouton spécifié dans une barre d’outils est activé.
ms.assetid: 055ed89a-2f3a-4174-b249-c6e68afbad31
keywords:
- TB_ISBUTTONENABLED les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_ISBUTTONENABLED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07ceb230edb693e065a7ef0455c1374b410a2dcd86995dc1a0ec8c2b354ae028
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918459"
---
# <a name="tb_isbuttonenabled-message"></a>TO \_ ISBUTTONENABLED message

Détermine si le bouton spécifié dans une barre d’outils est activé.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro si le bouton est activé, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





