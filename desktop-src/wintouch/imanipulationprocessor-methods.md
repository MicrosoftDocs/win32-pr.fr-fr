---
title: Méthodes (IInertiaProcessor)
description: Cette section contient les méthodes de l’interface IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Interface tactile, IInertiaProcessor
- Windows Tactile, méthodes d’interface
- inertie, interface IInertiaProcessor
- Interface IInertiaProcessor, méthodes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cb5c03039c09ef1435fcddd4782a466fff3aa179d57e5abb3887fa9212ca753
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881439"
---
# <a name="methods-iinertiaprocessor"></a>Méthodes (IInertiaProcessor)

Cette section contient les méthodes de l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Méthode                                                 | Description                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Initialisation**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | Initialise le processeur avec l’horodatage initial et redémarre l’inertie.                                                                                                                                                    |
| [**Processus**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | Effectue des calculs pour le cycle actuel et peut déclencher l’événement **Delta** ou **Complete** selon que l’extrapolation est terminée ou non. Si l’extrapolation s’est terminée au battement précédent, la méthode est no-op. |
| [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | Effectue des calculs pour le cycle donné et peut déclencher l’événement **Delta** ou **Complete** selon que l’extrapolation est terminée ou non.                                                                        |
| [**Terminé**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | Termine la manipulation actuelle et arrête l’inertie sur le processeur d’inertie.                                                                                                                                              |
| [**CompleteTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | Termine la manipulation actuelle au battement donné, arrête l’inertie sur le processeur d’inertie et déclenche l’événement ManipulationCompleted.                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




