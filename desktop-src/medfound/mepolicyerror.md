---
description: Déclenché par une sortie approuvée si une erreur se produit lors de l’application de la stratégie de sortie.
ms.assetid: 0cc62915-1ed6-4d1d-9600-0dac0b9034e3
title: Événement MEPolicyError (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b75083974ee0e76d7d8e21f0a2c83c2feee8d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518603"
---
# <a name="mepolicyerror-event"></a>Événement MEPolicyError

Déclenché par une sortie approuvée si une erreur se produit lors de l’application de la stratégie de sortie.

Si la session multimédia reçoit cet événement, elle arrête la lecture et transfère l’événement à l’application.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) sont les suivantes.



| Valeur                      | Description                                                    |
|----------------------------|----------------------------------------------------------------|
| \_stratégie MF \_ E \_ non prise en charge | La sortie approuvée ne prend pas en charge la stratégie de sortie actuelle. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




