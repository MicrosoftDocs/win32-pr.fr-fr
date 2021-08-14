---
title: Modification de la position actuelle
description: Modification de la position actuelle
ms.assetid: f8c4b9b5-c5fb-4292-8418-41650dcd65c0
keywords:
- MCI_SEEK message de commande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14f062fc93a89f54fb89a30b6ac3e53c8d6240cfc28b661a25da48a0b1b2fbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941287"
---
# <a name="changing-the-current-position"></a>Modification de la position actuelle

Pour modifier la position actuelle dans un élément d’appareil, utilisez le message de commande [**MCI \_ Seek**](mci-seek.md) avec l’MCI \_ pour marquer et la structure de [**\_ recherche MCI Seek \_**](mci-seek-parms.md) . Si vous utilisez le membre **dwTo** pour spécifier une position de recherche avec MCI \_ Seek, vous devez interroger le format d’heure et le définir, si nécessaire.

En plus de spécifier une position avec le membre **dwTo** , vous pouvez spécifier la \_ recherche MCI \_ pour \_ Démarrer ou MCI \_ Rechercher les \_ indicateurs de \_ fin pour le paramètre *dwParam1* de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) afin de rechercher les positions de début et de fin de l’élément d’appareil. Si vous utilisez l’un de ces indicateurs, ne spécifiez pas l' \_ indicateur MCI.

 

 