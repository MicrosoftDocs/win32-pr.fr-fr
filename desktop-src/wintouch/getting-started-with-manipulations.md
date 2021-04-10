---
title: Manipulations
description: Cette section explique la manipulation d’objets pour Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Tactile Windows, manipulations
- manipulations, à propos de
- manipulations, différences de mouvements
- mouvements, différences de manipulation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10fe65494de990305e4268aa4191b5dabaa267f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309349"
---
# <a name="manipulations"></a>Manipulations

Cette section explique la manipulation d’objets pour Windows Touch.

## <a name="manipulation-overview"></a>Vue d’ensemble de la manipulation

Un moyen pratique de réfléchir aux manipulations consiste à les considérer comme un sur-ensemble de gestes. Ce que vous pouvez faire avec les gestes, vous pouvez le faire avec davantage de flexibilité et avec une précision plus fine en utilisant des manipulations. La différence entre les manipulations et les gestes est illustrée par un exemple simple. Vous pouvez développer un objet et le traduire en même temps à l’aide de manipulations. avec les gestes, vous ne pouvez effectuer qu’un seul à la fois. Cette capacité à manipuler un objet en temps réel rend les applications plus intuitives aux utilisateurs en offrant une expérience plus réaliste.

Les API de manipulation sont utilisées pour simplifier les opérations de transformation sur les objets pour les applications tactiles. Les manipulations sont effectuées dans Windows 7 par le biais de l’objet COM de manipulations. En utilisant des manipulations, les développeurs peuvent prendre en charge l’inertie plus facilement (physique des objets) et peuvent facilement effectuer des transformations sur les objets d’une manière qui est cohérente avec les autres applications. Les sections suivantes expliquent les différentes façons dont vous pouvez effectuer des manipulations.



| Section                                                                                            | Description                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ajout de la prise en charge de manipulation au code non managé](adding-manipulation-support-in-unmanaged-code.md) | Explique comment implémenter un récepteur d’événements pour l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) et ajouter des gestionnaires d’événements à votre code. |
| [Manipulations avancées](advanced-manipulations.md)                                               | Explique comment effectuer des manipulations complexes.                                                                                                       |
| [Rotation d’un seul doigt](single-finger-rotation.md)                                               | Explique comment faire pivoter un objet à l’aide d’un point pivot et du processeur de manipulation.                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Manipulations et inertie](manipulation-and-inertia.md)
</dt> </dl>

 

 




