---
title: Création d’une description d’appareil
description: Une description d’appareil UPnP est un document XML qui décrit les propriétés d’un appareil et la hiérarchie des périphériques imbriqués qu’il contient.
ms.assetid: b2a7d342-958c-439d-8b17-b4fdc5fbad12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52df95de15481c7004704b6f67cd9478083ac88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939836"
---
# <a name="creating-a-device-description"></a>Création d’une description d’appareil

Une [*Description d’appareil*](d-gly.md) UPnP est un document XML qui décrit les propriétés d’un appareil et la hiérarchie des périphériques imbriqués qu’il contient. Le schéma des descriptions d’appareils basés sur UPnP, connu sous le nom de langage de modèle UPnP (UTL) pour les appareils, est défini dans l’architecture de périphérique UPnP. Les descriptions des appareils contiennent des liens vers les [*descriptions de service*](s-gly.md). Le schéma pour les descriptions de service et UTL for services est également défini dans la spécification « architecture d’appareil UPnP ».

> [!Note]  
> Il peut y avoir des problèmes lors de l’utilisation de la description du service à partir de www.upnp.org.

 

Le développeur d’un appareil doit fournir des descriptions de l’appareil et du service pour l’appareil.

Les éléments d’une description d’appareil que le développeur d’un appareil hébergé doit fournir sont les mêmes que ceux définis dans la spécification « architecture d’appareil UPnP », avec les exceptions suivantes :

-   Les éléments **controlURL** et **eventSubURL** sont obligatoires et doivent être vides. L’hôte de l’appareil renseigne les valeurs de ces champs lorsque l’appareil est publié et annoncé.
-   L’élément **UDN** doit contenir un identificateur unique pour le document de description de l’appareil (autrement dit, il n’a pas besoin d’être globalement unique). Cet identificateur est utilisé pour rechercher les UDN générés par l’hôte d’appareil.
-   Les éléments **SCPDURL** ne doivent pas contenir d’URL pour les descriptions de service. Au lieu de cela, ils doivent contenir le nom du fichier de description du service. Le fichier de description du service doit se trouver dans le [*Répertoire des ressources*](r-gly.md). L’emplacement de ce répertoire doit être fourni à l’hôte de l’appareil pendant le processus d’inscription, par exemple à l’aide d’un programme d’installation. Ce chemin d’accès et tous les chemins d’accès relatifs, basés sur le chemin d’accès enregistré.
-   L’élément **URL** dans l’élément **Icon** ne doit pas contenir d’URL pour les icônes d’appareil. Au lieu de cela, ils doivent contenir le nom du fichier d’icône. S’il est présent, le fichier icône doit se trouver dans le répertoire de ressources. Ce chemin d’accès et tous les chemins d’accès relatifs, basés sur le chemin d’accès enregistré.
-   L’élément **URLBase** ne doit pas être présent.

> [!Note]  
> Toutes les URL générées par l’hôte d’appareil sont des URL relatives. Les URL sont relatives à l’emplacement du document de description de l’appareil, qui est envoyé dans l’annonce initiale de l’appareil.

 

> [!IMPORTANT]
> N’ajoutez pas de commentaires au document de description de l’appareil, car cela peut entraîner des échecs d’inscription lorsque l’hôte de l’appareil Plug-and-Play universel tente d’analyser le document.

 

## <a name="string-length-limitations"></a>Limitations de longueur de chaîne

Les longueurs de chaîne suivantes sont utilisées dans l’API de l’hôte d’appareil avec la technologie UPnP :

-   **DeviceType** – 64 octets
-   **FriendlyName** – 64 octets
-   **fabricant** – 64 octets
-   **ModelDescription** – 128 octets
-   **modelname** – 32 octets
-   **modelNumber** – 32 octets
-   **SerialNumber** – 64 octets
-   **UPC** – 12 octets
-   **serviceType** – 64 octets
-   **ServiceId** – 64 octets

 

 




