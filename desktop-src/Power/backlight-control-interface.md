---
description: L’interface de contrôle du rétroéclairage est une interface IOCTL standardisée pour contrôler la luminosité du rétroéclairage de l’écran LCD.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interface de contrôle de rétroéclairage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518257"
---
# <a name="backlight-control-interface"></a>Interface de contrôle de rétroéclairage

L’interface de contrôle du rétroéclairage est une interface IOCTL standardisée pour contrôler la luminosité du rétroéclairage de l’écran LCD.

Les applications qui requièrent le contrôle par programmation de la luminosité du rétroéclairage ou fournissent des contrôles pour l’utilisateur doivent utiliser cette interface plutôt qu’une interface propriétaire. dans le cas contraire, le système ne peut pas interroger la luminosité matérielle actuelle et risque de ne plus être synchronisé.

La première étape consiste à interroger l’appareil pour la luminosité prise en charge à l’aide du code de contrôle de [**\_ \_ \_ \_ luminosité pris en charge pour la requête de vidéo IOCTL**](ioctl-video-query-supported-brightness.md) . Cette opération retourne une mémoire tampon qui spécifie les niveaux de luminosité disponibles. Ensuite, vous pouvez interroger l’appareil pour la luminosité actuelle de l’affichage à l’aide du code de contrôle luminosité de l' [**\_ affichage des requêtes de vidéo \_ \_ \_ IOCTL**](ioctl-video-query-display-brightness.md) . Cette opération renvoie les paramètres actuels pour la luminosité de l’alternance (AC), la luminosité du courant direct (DC) et l’état de l’alimentation.

Pour modifier la luminosité de l’affichage, utilisez le jeu de vidéos IOCTL code de contrôle de [**\_ \_ \_ \_ luminosité**](ioctl-video-set-display-brightness.md) . Vous pouvez définir la luminosité de l’alimentation, la luminosité du contrôleur de périphérique ou les deux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de l’alimentation](about-power-management.md)
</dt> </dl>

 

 



