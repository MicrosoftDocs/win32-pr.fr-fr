---
title: Méthodes (IInertiaProcessor)
description: Cette section contient les méthodes de l’interface IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Tactile Windows, interface IInertiaProcessor
- Tactile Windows, méthodes d’interface
- inertie, interface IInertiaProcessor
- Interface IInertiaProcessor, méthodes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106512352"
---
# <a name="methods-iinertiaprocessor"></a>Méthodes (IInertiaProcessor)

Cette section contient les méthodes de l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Méthode                                                 | Description                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Réinitialiser**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | Initialise le processeur avec l’horodatage initial et redémarre l’inertie.                                                                                                                                                    |
| [**Processus**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | Effectue des calculs pour le cycle actuel et peut déclencher l’événement **Delta** ou **Complete** selon que l’extrapolation est terminée ou non. Si l’extrapolation s’est terminée au battement précédent, la méthode est no-op. |
| [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | Effectue des calculs pour le cycle donné et peut déclencher l’événement **Delta** ou **Complete** selon que l’extrapolation est terminée ou non.                                                                        |
| [**Terminé**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | Termine la manipulation actuelle et arrête l’inertie sur le processeur d’inertie.                                                                                                                                              |
| [**CompleteTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | Termine la manipulation actuelle au battement donné, arrête l’inertie sur le processeur d’inertie et déclenche l’événement ManipulationCompleted.                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




