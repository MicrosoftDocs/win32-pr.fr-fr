---
description: le système d’exploitation Windows 7 offre une prise en charge intégrée des périphériques de capteur.
ms.assetid: 751ba2fc-fbff-4418-82ac-eebc8a145b14
title: vue d’ensemble du capteur de Windows et de la plateforme d’emplacement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01b6d3132ad6e1bc299895bc39668edbe19b91c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416346"
---
# <a name="overview-of-the-windows-sensor-and-location-platform"></a>vue d’ensemble du capteur de Windows et de la plateforme d’emplacement

le système d’exploitation Windows 7 offre une prise en charge intégrée des périphériques de capteur. Cela comprend la prise en charge des capteurs de localisation, tels que les périphériques GPS. dans le cadre de cette prise en charge, le capteur de Windows et la plateforme d’emplacement constituent un moyen standard pour les fabricants de périphériques d’exposer des appareils de capteur aux développeurs de logiciels et aux consommateurs. En même temps, la plateforme offre aux développeurs une API standardisée et une interface de pilote de périphérique (DDI) pour travailler avec des capteurs et des données de capteur.

## <a name="about-sensor-devices"></a>À propos des appareils capteur

Les capteurs présentent de nombreuses configurations et, d’un point de vue spécifique, presque tout ce qui fournit des données sur les phénomènes physiques peut être appelé capteur. Même si nous considérons généralement les capteurs comme des périphériques matériels, les capteurs logiques peuvent également fournir des informations par le biais de l’émulation de la fonctionnalité de capteur dans le logiciel ou le microprogramme. En outre, un seul périphérique matériel peut contenir plusieurs capteurs.

le capteur de Windows et la plateforme d’emplacement organisent les capteurs en *catégories*, qui représentent des classes étendues de périphériques de capteur et des *types* qui représentent des genres spécifiques de capteurs. Par exemple, un capteur dans un contrôleur de jeu vidéo qui détecte la position et le mouvement de la main d’un joueur (peut-être pour un jeu de bowling vidéo) est catégorisé comme capteur d’orientation, mais son type est un accéléromètre 3D. dans le code, Windows représente des catégories et des types à l’aide d’identificateurs globaux uniques (guid), dont la plupart sont prédéfinis. Les fabricants de périphériques peuvent créer des catégories et des types en définissant et en publiant de nouveaux GUID, le cas échéant.

Les périphériques d’emplacement constituent une catégorie particulièrement intéressante. À l’heure actuelle, la plupart des gens sont familiarisés avec les systèmes de positionnement global (GPS). dans Windows, un capteur GPS fait partie de la catégorie d’emplacement. La catégorie d’emplacement peut inclure d’autres types de capteur. Certains de ces types de capteurs sont basés sur des logiciels, tels qu’un programme de résolution d’adresses IP qui fournit des informations d’emplacement basées sur une adresse Internet, un triangulateur de tour mobile qui détermine l’emplacement en fonction des tours proches ou un fournisseur d’emplacement réseau Wi-Fi qui lit les informations d’emplacement à partir du concentrateur de réseau sans fil connecté.

## <a name="about-the-platform"></a>À propos de la plateforme

le capteur de Windows et la plateforme d’emplacement sont constitués des composants utilisateur et développeur suivants :

-   la DDI permet à Windows de fournir aux appareils de capteur une méthode standard pour se connecter à l’ordinateur et fournir des données à d’autres sous-systèmes.
-   l’API de capteur Windows fournit un ensemble de méthodes, de propriétés et d’événements pour travailler avec des capteurs connectés et des données de capteur.
-   l’api d’emplacement Windows, qui repose sur l’api de capteur Windows, fournit un ensemble d’objets de programmation, notamment des objets de script, pour l’utilisation des informations d’emplacement.
-   Le panneau de configuration emplacement et autres capteurs permet aux administrateurs de l’ordinateur de définir des capteurs, y compris des capteurs d’emplacement, pour chaque utilisateur.

Les sections suivantes décrivent chacun de ces composants.

## <a name="architecture-diagram"></a>Diagramme de l’architecture

Le diagramme suivant montre la relation entre les composants.

![diagramme de plateforme de capteur et d’emplacement](images/platformarchitecture.png)

## <a name="device-driver-interface"></a>Interface de pilote de périphérique

les fabricants de capteurs peuvent créer des pilotes de périphérique pour connecter les capteurs avec Windows 7. les pilotes de périphérique de capteur sont implémentés à l’aide du modèle de pilote WPD (Windows Portable devices), qui est basé sur l’infrastructure de pilote de Mode utilisateur Windows (UMDF). De nombreux pilotes de périphériques ont été écrits à l’aide de ces frameworks. Étant donné que ces technologies sont établies, les programmeurs de pilote de périphérique expérimentés trouveront l’écriture d’un pilote de capteur comme une tâche familière. L’interface DDI de capteur utilise des interfaces et des types de données spécifiques UMDF et WPD, et définit également des commandes et des paramètres WPD spécifiques au capteur, le cas échéant. pour plus d’informations sur la création de pilotes de périphérique de capteur, consultez le Kit de pilotes Windows.

## <a name="sensor-api"></a>API Sensor

L’API de capteur permet aux développeurs C++ de créer des programmes basés sur des capteurs à l’aide d’un ensemble d’interfaces COM. L’API définit des interfaces pour effectuer des tâches de programmation de capteur courantes qui incluent la gestion des capteurs par catégorie, type ou ID, la gestion des événements de capteur, l’utilisation de capteurs individuels et de regroupements de capteurs, et l’utilisation de données de capteur. le SDK Windows comprend des fichiers d’en-tête, de la documentation, des exemples et des outils pour aider les développeurs de logiciels à utiliser des capteurs dans des programmes Windows. Cette documentation décrit l’API de capteur.

## <a name="location-api"></a>API d’emplacement

Reposant sur l’API de capteur, l’API d’emplacement offre un moyen simple de récupérer des données sur l’emplacement géographique tout en protégeant la confidentialité des utilisateurs. L’API location fournit ses fonctionnalités via un ensemble d’interfaces COM qui représentent des objets. Ces objets peuvent être utilisés par des programmeurs qui comprennent comment utiliser COM par le biais du langage de programmation C++ ou dans des langages de script, tels que des JScript. La prise en charge des scripts permet d’accéder facilement aux données de localisation des projets qui s’exécutent dans la zone ordinateur local, tels que les gadgets. le SDK Windows inclut des fichiers d’en-tête, de la documentation (y compris la documentation de référence sur les scripts), des exemples et des outils pour aider les développeurs Web et les développeurs de logiciels à utiliser les informations d’emplacement dans leurs programmes.

## <a name="location-and-other-sensors-control-panel"></a>Panneau de configuration emplacement et autres capteurs

Windows 7 comprend un panneau de configuration qui permet aux administrateurs de l’ordinateur d’activer ou de désactiver les capteurs à l’ensemble du système ou pour chaque utilisateur. Étant donné que certains capteurs peuvent exposer des données sensibles, cette interface utilisateur permet aux administrateurs de contrôler si tous les programmes ont accès à chaque capteur pour chaque utilisateur. Les utilisateurs peuvent également afficher les propriétés du capteur et modifier la description du capteur qui est affichée dans l’interface utilisateur.

Le panneau de configuration fournit également une page d’emplacement par défaut pour permettre aux utilisateurs de fournir leur emplacement. Quand aucun capteur n’est disponible, la plateforme utilise l’emplacement fourni par l’utilisateur. Les utilisateurs peuvent fournir des champs d’adresse postale, tels que l’adresse postale, la ville, l’État ou la province et le pays ou la région.

## <a name="related-topics"></a>Rubriques connexes

[À propos de l’API de capteur](about-the-sensor-api.md)

[Windows Site Web central du développement de matériel](https://www.microsoft.com/whdc/device/sensors/default.mspx)

[Centre de développement Windows](https://msdn.microsoft.com/windows/default.aspx?wt.svl=client)
