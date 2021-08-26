---
description: Ce document décrit la conception et l’utilisation des classes de base MSP. l’utilisation de ces classes n’est pas obligatoire, mais la plupart des développeurs trouvent qu’ils simplifient la tâche de création d’un MSP basé sur DirectShow pour TAPI 3s new MSPI.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Classes de base TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34d4f9f67618c3637bfaff149773ab7b0de4b93f33c8bca8e5eb892527735e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012339"
---
# <a name="tapi-3-msp-base-classes"></a>Classes de base TAPI 3 MSP

Ce document décrit la conception et l’utilisation des classes de base MSP. l’utilisation de ces classes n’est pas obligatoire, mais la plupart des développeurs trouvent qu’ils simplifient la tâche de création d’un MSP basé sur DirectShow pour le nouveau MSPI de l’interface TAPI 3.

Le code source pour les classes de base MSP se trouve dans le répertoire Samples du kit de développement logiciel (SDK) de la plateforme.

il est supposé que vous êtes familiarisé avec COM, ATL, DirectShow et C++. Le lecteur doit également connaître les informations générales dans [à propos du fournisseur de services multimédia (MSP)](about-the-media-service-provider-msp-.md) et de l' [interface MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-.md).

ATL 2,1 est requis pour Windows 2000. à partir de Windows XP, ATL 2,1 et 3,0 se compilent à la fois.

Bibliothèques de classes de base MSP (disponibles dans le kit de développement logiciel (SDK)) :

-   Mspbase. lib
-   Mspid. lib
-   Strmbase. lib
-   Tmuid. lib
    > [!Note]  
    > Les liaisons dynamiques et non statiques doivent être utilisées.

     

Fichiers d’en-tête de classe de base MSP (disponibles dans le kit de développement logiciel) :

-   Mspaddr. h
-   Mspbase. h
-   Mspcall. h
-   Msplog. h
-   Mspstrm. h
-   Mspterm. h
-   Mspthrd. h
-   Msptmac. h
-   Msptmvc. h
-   Msptrmvc. h
-   Msptrmac. h
-   Msptrmar. h
-   Msputils. h

Fichiers sources de la classe de base MSP (disponibles dans les exemples du kit de développement logiciel) :

-   Mspaddr. cpp
-   Mspcall. cpp
-   Msplog. cpp
-   Mspstrm. cpp
-   Mspterm. cpp
-   Mspthrd. cpp
-   Msptrmac. cpp
-   Msptrmar. cpp
-   Msptrmvc. cpp
-   Msputils. cpp

 

 



