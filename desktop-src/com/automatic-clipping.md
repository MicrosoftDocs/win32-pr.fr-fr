---
title: Découpage automatique
description: Découpage automatique
ms.assetid: 9107ee47-52aa-48c8-b141-c821f93fda45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dabc3fd7ece50250ee9e1fea89ff23dd23db533dfcc90d5a939ce1b563ce764
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551235"
---
# <a name="automatic-clipping"></a>Découpage automatique

il est fortement recommandé qu’un conteneur de contrôle ActiveX prenne en charge le découpage automatique de ses contrôles. Cela entraînera une opération plus efficace pour la plupart des contrôles. Si le découpage automatique est pris en charge, la propriété ambiante autoclip doit être prise en charge et avoir la valeur **true**.

Le découpage automatique est la capacité d’un conteneur à s’assurer que la sortie dessinée d’un contrôle passe uniquement à la zone de découpage actuelle du conteneur. Dans un conteneur qui prend en charge le découpage automatique, un contrôle peut peindre sans tenir compte de sa zone de découpage, car le conteneur détourne automatiquement tout dessin qui se produit en dehors de la zone du contrôle. Si un conteneur ne prend pas en charge le découpage automatique, les contrôles générés par le CDK créeront une fenêtre parente supplémentaire si une région de découpage non null est passée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Containers](containers.md)
</dt> </dl>

 

 




