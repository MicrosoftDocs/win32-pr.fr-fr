---
title: Indicateur de test
description: Indicateur de test
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- Indicateur de MCI_TEST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229824"
---
# <a name="the-test-flag"></a>Indicateur de test

L’indicateur « test » ( \_ test MCI) interroge l’appareil pour déterminer s’il peut exécuter la commande. L’appareil retourne une erreur s’il ne peut pas exécuter la commande. Elle ne retourne aucune erreur si elle peut gérer la commande. Lorsque vous spécifiez cet indicateur, MCI retourne le contrôle à l’application sans exécuter la commande.

Cet indicateur est pris en charge par les appareils vidéo numériques et VCR pour toutes les commandes, à l’exception de l' [**ouverture**](open.md) ([**MCI \_ Open**](mci-open.md)) et de la [**fermeture**](close.md) ([**MCI \_ Close**](mci-close.md)).

 

 




