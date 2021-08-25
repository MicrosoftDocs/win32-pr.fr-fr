---
title: Commutateurs
description: Commutateurs
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- mixages audio, contrôles
- mixages audio, commutateurs
- mélangeurs, contrôles
- mélangeurs, commutateurs
- basculer les contrôles
- Structure MIXERCONTROLDETAILS_BOOLEAN
- Contrôle booléen
- contrôle Button
- contrôle activé/désactivé
- contrôle mono
- contrôle du volume
- contrôle étendu stéréo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d2e23c5e6438fbc19208e3366283147462c2451a12e3ccdcae6c13fcd93d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805079"
---
# <a name="switches"></a>Commutateurs

Les contrôles de commutateur sont des commutateurs à deux États. Ces contrôles utilisent la [**structure \_ booléenne MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) pour récupérer et définir des propriétés de contrôle. Le tableau suivant décrit les types de commutateurs.



| Contrôler         | Description                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean         | Commutateur générique. Elle peut avoir la valeur **true** ou **false**.                                                                                                                                                                           |
| Bouton          | Affectez la valeur **true** à tous les boutons que le pilote doit gérer comme s’ils avaient été enfoncés. Si la valeur est **false**, aucune action n’est effectuée.                                                                                         |
| Actif/inactif          | Autre commutateur qui est représenté par un graphique autre que celui utilisé pour le commutateur booléen. Elle peut avoir la valeur ON ou OFF.                                                                                                    |
| Désactiver le son            | Désactive une ligne audio (en supprimant le flux de données de la ligne) ou autorise la lecture des données audio. Ce commutateur est fréquemment utilisé pour contrôler les lignes qui alimentent le mélangeur.                                                        |
| Mono            | Bascule entre la sortie mono et stéréo pour une ligne audio stéréo. Désactivez cette option pour lire les données stéréo en tant que canaux distincts. Affectez la valeur ON pour combiner des données des deux canaux en une ligne audio mono.                                            |
| Niveau sonore        | Amplifie les basses de faible volume pour une ligne audio. Affectez la valeur ON pour augmenter les basses de faible volume. Désactivez cette option pour définir les niveaux de volume sur normal. La quantité d’augmentation est spécifique au matériel. Pour plus d’informations, consultez la documentation de votre appareil de mixage. |
| Stéréo améliorée | Augmente la séparation stéréo. Affectez la valeur ON pour augmenter la séparation stéréo. Désactivez la valeur OFF pour aucune amélioration.                                                                                                                                  |



 

 

 