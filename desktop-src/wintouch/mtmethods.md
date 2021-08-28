---
title: Méthodes (IManipulationProcessor)
description: Cette section contient les méthodes de l’interface IManipulationProcessor.
ms.assetid: 33736f79-cb61-449c-80b9-1358db2621e9
keywords:
- Windows Interface tactile, IManipulationProcessor
- Windows Tactile, méthodes d’interface
- manipulations, interface IManipulationProcessor
- Interface IManipulationProcessor, méthodes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 161ac2fc0d30c70e0f305de55a3f65b2eb827a925615977ce726eaa200615806
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964198"
---
# <a name="methods-imanipulationprocessor"></a>Méthodes (IManipulationProcessor)

Cette section contient les méthodes de l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .

Les méthodes suivantes sont exposées par l’interface [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .



| Méthode                                                                      | Description                                                                              |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [**CompleteManipulation**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-completemanipulation) | Cette méthode est appelée lorsque le développeur choisit de terminer la manipulation.                |
| [**GetAngularVelocity**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity)     | Calcule la rapidité de rotation à laquelle l’objet cible se déplace.                  |
| [**GetExpansionVelocity**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity) | Calcule le taux auquel l’objet cible s’étend.                              |
| [**GetVelocityX**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx)                 | Calcule et retourne la vélocité horizontale de l’objet cible.                    |
| [**GetVelocityY**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy)                 | Calcule et retourne la vélocité verticale.                                            |
| [**ProcessDown**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown)                   | Alimente les données vers le processeur de manipulation associé à une cible.                       |
| [**ProcessMove**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove)                   | Alimente les données vers le processeur de manipulation associé à une cible.                       |
| [**ProcessUp**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup)                       | Alimente les données vers le processeur de manipulation associé à une cible.                       |
| [**ProcessDownWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)   | Flux de données incluant un horodateur au processeur de manipulation associé à une cible. |
| [**ProcessMoveWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)   | Flux de données incluant un horodateur au processeur de manipulation associé à une cible. |
| [**ProcessUpWithTime**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)       | Flux de données incluant un horodateur au processeur de manipulation associé à une cible. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




