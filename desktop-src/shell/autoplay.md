---
description: L’exécution automatique est une fonctionnalité du système d’exploitation Windows.
title: Création d’une application de CD-ROM compatible avec l’exécution automatique
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5c583c1d-a4eb-4291-a839-c1ca7c51342c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 33f3ccc0a253690cd377cad908f87b43ac1ea304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201282"
---
# <a name="creating-an-autorun-enabled-cd-rom-application"></a>Création d’une application de CD-ROM compatible avec l’exécution automatique

L’exécution automatique est une fonctionnalité du système d’exploitation Windows. Il automatise les procédures d’installation et de configuration des produits conçus pour les plateformes Windows distribuées sur les CD-ROM. Quand les utilisateurs insèrent un disque compact à extension automatique dans leur lecteur de CD-ROM, l’exécution automatique exécute automatiquement une application sur le CD-ROM qui installe, configure ou exécute le produit sélectionné.

L’exécution automatique peut être utilisée pour installer et exécuter des applications de CD-ROM. Bien que l’exécution automatique soit le plus souvent utilisée pour les applications Windows, elle peut également être utilisée pour installer, configurer ou exécuter des applications MS-DOS dans une session Microsoft MS-DOS Windows. Vous pouvez configurer chaque application ms-dos avec une icône unique, un fichier Config.sys et un fichier Autoexec.bat. Windows crée les fichiers de configuration corrects pour l’application ms-dos. L’application de démarrage démarre ensuite l’application ms-dos dans une fenêtre.

> [!Note]  
> Pour que l’exécution automatique fonctionne, le lecteur de CD-ROM doit avoir des pilotes de périphérique 32 ou 64 bits qui détectent quand un utilisateur insère un CD-ROM et notifie le système.

 

Les sections suivantes expliquent comment implémenter une application de CD-ROM activée pour l’exécution automatique.

-   [Création d’une application AutoRun-Enabled](autoplay-works.md)
-   [Entrées autorun. inf](autorun-cmds.md)
-   [Activation et désactivation de l’exécution automatique](autoplay-reg.md)

 

 



