---
description: La classe CAMEvent est un wrapper pour les événements de réinitialisation manuelle et de réinitialisation automatique.
ms.assetid: 228b4e51-afc5-4cb6-b225-309013713983
title: CAMEvent, classe (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bde2db8adf2bb713df665e06eb2cc5f8d2a9a00f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542523"
---
# <a name="camevent-class"></a>CAMEvent, classe

![hiérarchie de la classe camevent](images/util06.png)

La classe **CAMEvent** est un wrapper pour les événements de réinitialisation manuelle et de réinitialisation automatique.

Cette classe offre un moyen pratique de gérer les événements, plutôt que d’appeler des fonctions telles que [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)et [**ResetEvent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent).



| Variables membres protégées                          | Description                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [**m \_ hEvent**](camevent-m-hevent.md)              | Handle d’événement.                                                   |
| M&#233;thodes publiques                                      | Description                                                     |
| [**CAMEvent**](camevent-camevent.md)               | Méthode de constructeur.                                             |
| [**~ CAMEvent**](camevent--camevent.md)             | Méthode de destructeur.                                              |
| [**Vérification**](camevent-check.md)                     | Vérifie si l’événement est défini, sans blocage.              |
| [**Réinitialiser**](camevent-reset.md)                     | Définit l’état de l’événement comme étant non signalé.                     |
| [**Définissez**](camevent-set.md)                         | Signale l’événement.                                              |
| [**Wait**](camevent-wait.md)                       | Bloque jusqu’à ce que l’événement soit signalé, ou jusqu’à ce qu’un délai d’attente se produise. |
| Opérateurs                                           | Description                                                     |
| [**HANDLE d’opérateur**](camevent-operator-handle.md) | Récupère le handle d’événement.                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

