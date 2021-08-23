---
title: TooManyChildren
description: TooManyChildren
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d7888f3bbdfe32facfa93997c6c57f754cc3aa3742419f66fd595f086aefce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993989"
---
# <a name="toomanychildren"></a>TooManyChildren

## <a name="text"></a>Texte

Arrêt de la recherche de frères supplémentaires après la recherche de {0} frères. Arborescence incorrecte possible

## <a name="type"></a>Type

Avertissement

## <a name="description"></a>Description

L’arborescence d’éléments peut être cyclique et la profondeur d’arborescence est infinie.

Ce problème peut entraîner des problèmes de navigation pour les outils automatisés, car ils entrent en tant que référence circulaire ou boucle infinie.

## <a name="possible-causes"></a>Causes possibles

-   La conception d’une application ou d’un contrôle peut être trop complexe. Cet avertissement peut être signalé pour les contrôles d’affichage de liste qui ont un grand nombre d’éléments. Dans ce cas, vous pouvez généralement ignorer cet avertissement.
-   Implémentation MSAA incorrecte ou non valide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




