---
title: Application de point de contrôle utilisateur générique
description: L’application de point de contrôle utilisateur générique (UCP) vous permet de découvrir des appareils, de contrôler ces appareils détectés et d’afficher les informations d’événement connexes, à l’aide d’une interface graphique.
ms.assetid: 18ac23df-9d69-4a28-91e5-991eb4f3e6ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0bbf454da2bf36becb3c8b0aff2babc87925df7ac658fc9dc7963ba9182fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655732"
---
# <a name="generic-user-control-point-application"></a>Application de point de contrôle utilisateur générique

L’application de point de contrôle utilisateur générique (UCP) vous permet de découvrir des appareils, de contrôler ces appareils détectés et d’afficher les informations d’événement connexes, à l’aide d’une interface graphique.

**Pour démarrer l’application générique UCP**

1.  Créez et configurez \\ le \\ \\ \\ fichier d'devtype.txt netds UPnP GenericUCP CPP \\ (ou le \\ \\ fichierdevtype.txt VisualBasic) avec les informations de l’appareil. Ce fichier vous permet de configurer les UCP génériques pour les recherches « Rechercher par type » et « recherche asynchrone ». Chaque ligne du fichier doit contenir un type d’appareil et la description associée. Par exemple :

    ``` syntax
    upnp:rootdevice All Root Devices
    urn:schemas-upnp-org:device:mediaplayer:1    Media Player
    ```

    Cet exemple est destiné à un périphérique de lecteur multimédia fictif. Le « lecteur multimédia » à la fin de la deuxième ligne ne fait pas partie du type d’appareil. il est fourni à titre d’information dans l’application UCP générique. Il en va de même pour « tous les appareils racine » sur la première ligne.

    Ajoutez une ligne qui contient le type et la description de votre appareil spécifique pour chaque appareil.

2.  Créez et configurez \\ le \\ fichier d'udn.txt netds UPnP \\ GenericUCP \\ CPP \\ (ou le \\ \\ fichierudn.txt VisualBasic) avec des informations UDN pour vos appareils. Ce fichier vous permet de configurer le UCP générique pour la recherche « Rechercher par UDN ». Chaque ligne utilise la forme suivante :

    ``` syntax
    uuid:{7d50b574-4213-4b88-84d9-e5c9241fcb3a}
    ```

    Ajoutez une ligne qui contient vos UDN spécifiques pour chaque appareil.

3.  Exécutez GenericUCP.exe. La fenêtre **UCP générique** s’affiche.

    ![fenêtre UCP générique](images/generic-ucp.png)

> [!Note]  
> Vue de la **Présentation** et du **service d’affichage DESC.** la fonctionnalité n’est pas implémentée dans l’exemple de code C++.

 

 

 




