---
title: Indicateurs de priorité
description: L’indicateur Priority ouvre un objet de stockage en mode de priorité.
ms.assetid: 85f2df6f-9219-4752-8c17-f219c37a4037
keywords:
- Indicateurs de priorité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f4af04174ddb6c0ac459a6f7e6841e061b03c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029893"
---
# <a name="priority-flags"></a>Indicateurs de priorité

L’indicateur Priority ouvre un objet de stockage en mode de priorité. Lorsqu’il ouvre un objet, une application fonctionne généralement à partir d’une copie d’instantané, car d’autres applications peuvent également utiliser l’objet en même temps. Toutefois, lors de l’ouverture d’un objet de stockage en mode de priorité, l’application dispose des droits exclusifs pour valider les modifications apportées à l’objet.

Le mode priorité permet à une application de lire des flux à partir du stockage avant d’ouvrir l’objet dans un mode qui nécessiterait le système pour effectuer une copie d’instantané. Étant donné que l’application dispose d’un accès exclusif, elle n’a pas besoin de créer une copie d’instantané de l’objet. Lorsque l’application ouvre par la suite l’objet dans un mode dans lequel une copie d’instantané est requise, l’application peut exclure les flux qu’elle a déjà lus à partir de l’instantané, ce qui réduit la surcharge liée à l’ouverture de l’objet.

Étant donné que les autres applications ne peuvent pas valider les modifications apportées à un objet pendant qu’il est ouvert en mode de priorité, les applications doivent garder l’objet dans ce mode aussi peu de temps que possible.

 

 




