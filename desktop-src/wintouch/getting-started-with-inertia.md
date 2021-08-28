---
title: Inertie
description: cette section explique l’inertie pour Windows Touch.
ms.assetid: c33dda89-c715-4da0-a7af-aa0010dfd88b
keywords:
- Windows Toucher, inertie
- inertie, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ff1fd58d52ba73d758254c1dac1e8952df30b836b68ef12b022a29ceafc694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709809"
---
# <a name="inertia"></a>Inertie

cette section explique l’inertie pour Windows Touch.

l’API d’inertie incluse dans Windows 7 permet un comportement cohérent des objets dans les applications tactiles Windows en fournissant un modèle physique simple. L’inertie est activée à l’aide du processeur d’inertie, une classe qui encapsule les fonctionnalités. Le processeur d’inertie fonctionne en traitant les événements qui lui sont passés lorsque les manipulations d’objets se terminent et en gérant les trajectoires d’objet d’une manière qui est cohérente avec les autres applications. Notez que le processeur d’inertie est étroitement couplé au processeur de manipulation pour simplifier l’ajout de la prise en charge de l’inertie aux applications qui utilisent des manipulations. En fait, le processeur d’inertie déclenche les mêmes événements que le processeur de manipulation. La section suivante explique comment prendre en main l’inertie.



| Section                                                                      | Description                                                                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Mécanismes d’inertie](inertia-mechanics.md)                                   | Explique les principes de base des calculs d’inertie.                                                                             |
| [Gestion de l’inertie dans du code non managé](handling-inertia-in-unmanaged-code.md) | Explique comment utiliser l’interface [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) pour gérer l’inertie dans du code non managé. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Manipulations et inertie](manipulation-and-inertia.md)
</dt> </dl>

 

 




