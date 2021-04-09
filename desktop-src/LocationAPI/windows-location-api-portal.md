---
description: .
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: API d’emplacement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f643565e80f72ffcefe6981c924b3739b1c4f5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864873"
---
# <a name="location-api"></a>API d’emplacement

\[L’API de localisation Win32 et est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) . Pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). \]

## <a name="purpose"></a>Objectif

Aujourd’hui, les ordinateurs sont plus mobiles que jamais. Des petits ordinateurs portables aux Tablet PC, de nombreux ordinateurs peuvent aller là où l’utilisateur souhaite aller. Les programmes qui tirent parti de la mobilité de l’ordinateur peuvent ajouter de la valeur aux vies du personnel. Par exemple, un programme qui peut trouver des restaurants à proximité et fournir des indications routières semble être une solution naturelle pour un ordinateur portable. Mais même si la technologie permettant de déterminer l’emplacement actuel de l’utilisateur est courante et abordable, la création de solutions sur cette technologie peut être une tâche fastidieuse.

Pour créer un programme prenant en charge l’emplacement, vous devrez peut-être surmonter un grand nombre de problèmes, notamment :

-   Les périphériques GPS (Global Positioning System) qui utilisent des ports COM virtuels, qui permettent d’accéder à un seul programme à la fois.
-   Comprendre et programmer pour les protocoles, tels que la spécification de l’Association d’appareils électroniques nationaux (NMEA), ainsi que les extensions propriétaires de propriétaires.
-   Limité à la programmation de solutions matérielles connues et verticales.
-   Implémentation d’une logique pour gérer les transitions entre différents fournisseurs de localisation, tels que les récepteurs GPS, les réseaux connectés, les réseaux de téléphonie cellulaire, Internet et les paramètres utilisateur.

Cette documentation décrit l’interface de programmation d’applications (API) d’emplacement Windows. L’API location permet de simplifier la programmation prenant en charge l’emplacement en fournissant un moyen standard de récupérer des données sur l’emplacement de l’utilisateur et de standardiser les formats des rapports de données d’emplacement. L’API location gère automatiquement les transitions entre les fournisseurs de données de localisation et choisit toujours le fournisseur le plus précis pour la situation actuelle.

## <a name="developer-audience"></a>Développeurs concernés

L’API location fournit ses fonctionnalités via un ensemble d’interfaces COM. Les fonctionnalités de l’API location peuvent être utilisées par les programmeurs qui sont familiarisés avec l’utilisation de COM par le biais du langage de programmation C++, ou avec l’utilisation d’objets COM dans des langages de script, tels que Microsoft JScript.

## <a name="in-this-section"></a>Dans cette section

-   [Référence de programmation C++ de l’API d’emplacement](windows-location-programming-reference.md)
-   [Référence du modèle objet de l’API Location](windows-location-script-programming-reference.md)

 

 
