---
title: Inertie
description: Cette section décrit l’inertie pour Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Tactile Windows, inertie
- inertie, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b69ad31ec4a61f8723c9e52f87883dc4af3772
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028695"
---
# <a name="inertia"></a>Inertie

Cette section décrit l’inertie pour Windows Touch.

L’API d’inertie incluse dans Windows 7 permet un comportement cohérent des objets dans les applications tactiles Windows en fournissant un modèle physique simple. L’inertie est activée à l’aide du processeur d’inertie, une classe qui encapsule les fonctionnalités. Le processeur d’inertie fonctionne en traitant les événements qui lui sont passés lorsque les manipulations d’objets se terminent et en gérant les trajectoires d’objet d’une manière qui est cohérente avec les autres applications. Notez que le processeur d’inertie est étroitement couplé au processeur de manipulation pour simplifier l’ajout de la prise en charge de l’inertie aux applications qui utilisent des manipulations. En fait, le processeur d’inertie déclenche les mêmes événements que le processeur de manipulation. La section suivante explique comment prendre en main l’inertie.



| Section                                                                      | Description                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Mécanismes d’inertie](inertia-mechanics.md)                                   | Explique les principes de base des calculs d’inertie.                                                                             |
| [Gestion de l’inertie dans du code non managé](handling-inertia-in-unmanaged-code.md) | Explique comment utiliser l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) pour gérer l’inertie dans du code non managé. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Manipulations et inertie](manipulation-and-inertia.md)
</dt> </dl>

 

 




