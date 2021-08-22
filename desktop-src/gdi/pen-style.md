---
description: L’attribut style spécifie le motif de ligne qui apparaît lorsqu’un stylet cosmétique ou géométrique particulier est utilisé. Il existe huit styles de stylet prédéfinis. L’illustration suivante montre les sept de ces styles qui sont définis par le système.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Style de stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42cc82510c58d36cec76039488ecc13c826609a0870b929f18d82282a87ba8cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666509"
---
# <a name="pen-style"></a>Style de stylet

L’attribut style spécifie le motif de ligne qui apparaît lorsqu’un stylet cosmétique ou géométrique particulier est utilisé. Il existe huit styles de stylet prédéfinis. L’illustration suivante montre les sept de ces styles qui sont définis par le système.

![Illustration montrant sept lignes, chacune d’elles étant dessinée à l’aide d’un style prédéfini différent](images/cspen-01.png)

Le style de cadre intérieur est identique au style plein pour les plumes cosmétiques. Toutefois, elle fonctionne différemment lorsqu’elle est utilisée avec un stylet géométrique. Si le stylet géométrique est plus grand qu’un pixel unique et qu’une fonction de dessin utilise le stylet pour dessiner une bordure autour d’un objet rempli, le système dessine la bordure à l’intérieur du cadre de l’objet. En utilisant le style d’image interne, une application peut garantir qu’un objet apparaît entièrement dans les dimensions spécifiées, quelle que soit la largeur géométrique du stylet.

Outre les sept styles définis par le système, il existe un huitième style qui est défini par l’utilisateur (ou l’application). Un style défini par l’utilisateur génère des lignes avec une série personnalisée de tirets et de points.

Utilisez la fonction [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) pour créer un stylet avec les styles définis par le système. Utilisez la fonction **ExtCreatePen** pour créer un stylet avec un style défini par l’utilisateur.

 

 



