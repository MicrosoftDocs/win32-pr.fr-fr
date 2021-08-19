---
title: Indicateur de test
description: Indicateur de test
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- Indicateur de MCI_TEST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837b7812a904ed39fa0350d703b1525bbffa6f981b4736d25927840395932f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801474"
---
# <a name="the-test-flag"></a>Indicateur de test

L’indicateur « test » ( \_ test MCI) interroge l’appareil pour déterminer s’il peut exécuter la commande. L’appareil retourne une erreur s’il ne peut pas exécuter la commande. Elle ne retourne aucune erreur si elle peut gérer la commande. Lorsque vous spécifiez cet indicateur, MCI retourne le contrôle à l’application sans exécuter la commande.

Cet indicateur est pris en charge par les appareils vidéo numériques et VCR pour toutes les commandes, à l’exception de l' [**ouverture**](open.md) ([**MCI \_ Open**](mci-open.md)) et de la [**fermeture**](close.md) ([**MCI \_ Close**](mci-close.md)).

 

 




