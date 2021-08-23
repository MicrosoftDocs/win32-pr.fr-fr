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
ms.openlocfilehash: ea87239628f001feaa82f84ca8c50941b56d3eb99f486934b551e832d1f588c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955528"
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
| [**Chèque**](camevent-check.md)                     | Vérifie si l’événement est défini, sans blocage.              |
| [**Initialisation**](camevent-reset.md)                     | Définit l’état de l’événement comme étant non signalé.                     |
| [**Définie**](camevent-set.md)                         | Signale l’événement.                                              |
| [**Wait**](camevent-wait.md)                       | Bloque jusqu’à ce que l’événement soit signalé, ou jusqu’à ce qu’un délai d’attente se produise. |
| Opérateurs                                           | Description                                                     |
| [**HANDLE d’opérateur**](camevent-operator-handle.md) | Récupère le handle d’événement.                                     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wxutil. h (inclure Flux. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

