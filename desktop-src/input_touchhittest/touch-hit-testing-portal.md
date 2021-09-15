---
title: Test d’atteinte tactile
description: Les rubriques de cette section fournissent une vue d’ensemble de la prise en charge du test d’atteinte tactile dans Windows 8.
ms.assetid: bdd7630c-b2d8-4080-a149-efec018f697d
keywords:
- intervention de l'utilisateur
- entrée
- pointeur
- interface tactile
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 8cf6d28badb47a176a6feccf166344003faf1de8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522545"
---
# <a name="touch-hit-testing"></a>Test d’atteinte tactile

## <a name="purpose"></a>Objectif

Les rubriques de cette section fournissent une vue d’ensemble de la prise en charge du test d’atteinte tactile dans Windows. Le test d’atteinte tactile vous permet d’identifier une cible d’entrée selon que la zone de contenu d’un élément d’interface utilisateur se trouve dans la zone de contact ou qu’elle inclue le point de contact.

Le test tactile utilise une géométrie de contact complexe pour l’ensemble de la zone tactile plutôt qu’une seule coordonnée x-y interpolée. L’utilisation de la géométrie de contact entière améliore considérablement la précision et la précision lorsque vous identifiez la cible la plus probable de l’entrée tactile.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
| --- | --- |
| [Référence de test de positionnement tactile](touchhittest-reference.md)<br/> | Les rubriques de cette section fournissent les spécifications de référence pour le [test d’atteinte tactile](touch-hit-testing-portal.md).<br/> |

## <a name="developer-audience"></a>Développeurs concernés

Les API de test de positionnement tactile sont conçues pour les développeurs qui créent des infrastructures d’interface utilisateur qui offrent une expérience utilisateur cohérente et optimisée pour les applications de bureau.

## <a name="related-topics"></a>Rubriques connexes

[Interaction de l’utilisateur](../user-interaction.md)
