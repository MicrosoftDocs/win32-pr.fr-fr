---
title: Découpage automatique
description: Découpage automatique
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fb39f3a9f15ed6e1e96493ed2cbdd62db40403
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310677"
---
# <a name="automatic-clipping"></a>Découpage automatique

Il est fortement recommandé qu’un conteneur de contrôles ActiveX prenne en charge le découpage automatique de ses contrôles. Cela entraînera une opération plus efficace pour la plupart des contrôles. Si le découpage automatique est pris en charge, la propriété ambiante autoclip doit être prise en charge et avoir la valeur **true**.

Le découpage automatique est la capacité d’un conteneur à s’assurer que la sortie dessinée d’un contrôle passe uniquement à la zone de découpage actuelle du conteneur. Dans un conteneur qui prend en charge le découpage automatique, un contrôle peut peindre sans tenir compte de sa zone de découpage, car le conteneur détourne automatiquement tout dessin qui se produit en dehors de la zone du contrôle. Si un conteneur ne prend pas en charge le découpage automatique, les contrôles générés par le CDK créeront une fenêtre parente supplémentaire si une région de découpage non null est passée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

 




