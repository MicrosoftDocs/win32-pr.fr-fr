---
title: Plateforme de capteur
description: Windows 7 a changé la façon dont les développeurs utilisent les capteurs.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031477"
---
# <a name="sensor-platform"></a>Plateforme de capteur

Windows 7 a changé la façon dont les développeurs utilisent les capteurs. Il inclut la prise en charge native des capteurs, développée par une nouvelle plateforme de développement pour l’utilisation de capteurs, y compris les capteurs d’emplacement, tels que les périphériques GPS (Global Positioning Systems).

Reposant sur la plateforme de capteur, les API d' *emplacement Windows* sont une nouvelle fonctionnalité de Windows 7 qui permet aux développeurs d’applications d’accéder aux informations relatives à l’emplacement physique de l’utilisateur. Les API d' *emplacement Windows* peuvent faire abstraction du matériel, prendre en charge simultanément plusieurs applications et basculer en toute transparence entre les différentes technologies, ce qui allège le développeur d’applications de la charge de gestion de ces contraintes. Les API de *localisation* peuvent être utilisées par les programmeurs par le biais du langage de programmation C++ (par les programmeurs habitués au modèle com), ou en utilisant des objets COM dans des langages de script, tels que Microsoft JScript. La prise en charge des scripts permet d’accéder facilement aux données de localisation des projets tels que les gadgets.

Windows 7 fournit une plate-forme solide et facile à utiliser pour l’utilisation de périphériques de capteur, tels qu’un capteur de lumière ambiante ou une jauge de température, afin de créer une prise en compte de l’environnement dans les applications Windows. Les PC peuvent utiliser des capteurs intégrés à l’ordinateur, connectés par le biais de connexions câblées ou sans fil, ou connectés via un réseau ou *Internet*.

Les API de *capteur* et de *localisation* offrent un moyen standard de découvrir les capteurs et d’accéder par programmation aux données fournies par les capteurs.

Le panneau de configuration du *capteur* permet aux utilisateurs d’activer ou de désactiver les capteurs, de contrôler l’accès aux capteurs susceptibles d’exposer des données sensibles, d’afficher les propriétés de capteur et de modifier la description des capteurs.

L' [extension de classe de capteur](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) est une partie fondamentale du modèle de développement de pilote pour la plateforme de capteur. Il fournit les mécanismes suivants, qui sont utilisés lors de l’écriture d’un pilote de capteur de l' [infrastructure de pilote en mode utilisateur (UMDF)](https://developer.microsoft.com/windows/hardware) :

-   Intégration à la plateforme de capteur
-   Mise en œuvre de la sécurité

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API de capteur](../sensorsapi/portal.md)
</dt> <dt>