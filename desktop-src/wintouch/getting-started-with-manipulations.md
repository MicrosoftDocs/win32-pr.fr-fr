---
title: Manipulations
description: cette section explique la manipulation d’objets pour Windows Touch.
ms.assetid: 7f905c36-7804-422c-8a60-a281e03c5e15
keywords:
- Windows Toucher, manipulations
- manipulations, à propos de
- manipulations, différences de mouvements
- mouvements, différences de manipulation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5368b39de1f35cc9a547bc240fc3c984fc1f10f658972b0f845a965e09bb29c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435984"
---
# <a name="manipulations"></a>Manipulations

cette section explique la manipulation d’objets pour Windows Touch.

## <a name="manipulation-overview"></a>Vue d’ensemble de la manipulation

Un moyen pratique de réfléchir aux manipulations consiste à les considérer comme un sur-ensemble de gestes. Ce que vous pouvez faire avec les gestes, vous pouvez le faire avec davantage de flexibilité et avec une précision plus fine en utilisant des manipulations. La différence entre les manipulations et les gestes est illustrée par un exemple simple. Vous pouvez développer un objet et le traduire en même temps à l’aide de manipulations. avec les gestes, vous ne pouvez effectuer qu’un seul à la fois. Cette capacité à manipuler un objet en temps réel rend les applications plus intuitives aux utilisateurs en offrant une expérience plus réaliste.

Les API de manipulation sont utilisées pour simplifier les opérations de transformation sur les objets pour les applications tactiles. les manipulations sont effectuées dans Windows 7 via l’objet COM de manipulations. En utilisant des manipulations, les développeurs peuvent prendre en charge l’inertie plus facilement (physique des objets) et peuvent facilement effectuer des transformations sur les objets d’une manière qui est cohérente avec les autres applications. Les sections suivantes expliquent les différentes façons dont vous pouvez effectuer des manipulations.



| Section                                                                                            | Description                                                                                                                                          |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ajout de la prise en charge de manipulation au code non managé](adding-manipulation-support-in-unmanaged-code.md) | Explique comment implémenter un récepteur d’événements pour l’interface [**\_ IManipulationEvents**](/windows/win32/api/manipulations/nn-manipulations-_imanipulationevents) et ajouter des gestionnaires d’événements à votre code. |
| [Manipulations avancées](advanced-manipulations.md)                                               | Explique comment effectuer des manipulations complexes.                                                                                                       |
| [Rotation d’un seul doigt](single-finger-rotation.md)                                               | Explique comment faire pivoter un objet à l’aide d’un point pivot et du processeur de manipulation.                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Manipulations et inertie](manipulation-and-inertia.md)
</dt> </dl>

 

 




