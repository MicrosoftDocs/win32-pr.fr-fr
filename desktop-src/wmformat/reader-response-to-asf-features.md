---
title: Réponse du lecteur aux fonctionnalités ASF
description: Réponse du lecteur aux fonctionnalités ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media Format SDK, lecteurs réponses aux fonctionnalités ASF
- ASF (Advanced Systems Format), réponses des lecteurs aux fonctionnalités
- ASF (format de systèmes avancés), réponses de lecteur aux fonctionnalités
- réponses des lecteurs aux fonctionnalités ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8b8b64649388af6186155009f2a47b0f2b2c96cc42645e64dbb04f3054d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084496"
---
# <a name="reader-response-to-asf-features"></a>Réponse du lecteur aux fonctionnalités ASF

La plupart des fonctionnalités de fichier ASF spéciales peuvent être définies dans des fichiers pour interagir avec des applications de jeu personnalisées conçues pour les gérer. Toutefois, certaines fonctionnalités offrent une prise en charge intégrée dans l’objet Reader.

L’objet lecteur sélectionne automatiquement les flux à partir des jeux qui s’excluent mutuellement par vitesse de transmission. Ce cas spécial est appelé « débit binaire multiple » (MBR). Le flux sélectionné par le lecteur est basé sur la vitesse de transmission du flux. Le numéro du flux et l’ordre dans lequel il a été ajouté à l’objet d’exclusion mutuelle ne sont pas pertinents pour la sélection automatique. Si un fichier contient plus d’un ensemble de flux mutuellement exclusifs par vitesse de transmission, le lecteur sélectionne des flux en fonction du calcul de la meilleure utilisation de la bande passante disponible.

L’exclusion mutuelle basée sur le langage est définie à l’aide d’un paramètre de sortie avant la lecture. Si vous combinez la langue et l’exclusion mutuelle basée sur la fréquence de bits, vous devez regrouper les flux de bits qui s’excluent mutuellement par langue, puis rendre les groupes mutuellement exclusifs par langue. Le lecteur vérifiera d’abord la langue, puis déterminera la vitesse de transmission à utiliser.

La hiérarchisation des flux est définie à l’aide d’un tableau d’enregistrements. Les enregistrements dans le tableau sont dans l’ordre de priorité décroissant. Le dernier flux du tableau est le premier qui sera supprimé par le lecteur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Exclusion mutuelle**](mutual-exclusion.md)
</dt> <dt>

[**Hiérarchisation des flux**](stream-prioritization.md)
</dt> </dl>

 

 




