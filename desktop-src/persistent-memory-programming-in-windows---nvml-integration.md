---
description: La technologie mémoire persistante (PM) fournit un accès au niveau octet aux médias non volatiles tout en réduisant considérablement la latence du stockage ou de la récupération des données.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Programmation de mémoire persistante dans l’intégration de Windows-NVML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210359"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Programmation de mémoire persistante dans l’intégration de Windows-NVML

La technologie mémoire persistante (PM) fournit un accès au niveau octet aux médias non volatiles tout en réduisant considérablement la latence du stockage ou de la récupération des données. Il crée un nouveau niveau entre la mémoire du système et le stockage traditionnel. Tout programme dépendant ou mis à l’échelle avec des écritures rapides sur un support permanent peut tirer parti de PM.

L’objectif de cet article est de montrer comment la bibliothèque mémoire non volatile (NVML) peut être intégrée dans un projet Visual Studio pour faciliter son utilisation.

> [!Note]  
> La mémoire persistante est parfois également appelée mémoire de classe de stockage (SCM).

 

## <a name="pm-and-nvml"></a>PM et NVML

La première prise en charge de la mémoire persistante a été introduite dans Windows Server 2016 et la mise à jour anniversaire de Windows 10 (1607). Pour une vue d’ensemble rapide, consultez ces deux vidéos channel9 :

-   [Utilisation de la mémoire non volatile (NVDIMM-N) comme stockage de bloc dans Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P466)
-   [Utilisation de la mémoire non volatile (NVDIMM-N) en tant que stockage Byte-Addressable dans Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P470)

Pour aider les développeurs à tirer parti des avantages offerts par la mémoire persistante, Microsoft a également contribué à mettre en œuvre la bibliothèque mémoire non volatile (NVML) dans Windows. Cette bibliothèque fournit différents outils pour rendre les applications compatibles avec la mémoire persistante. Par exemple, il contient du code qui vous permet de créer facilement un magasin clé-valeur prenant en charge les bases de code pour des recherches et des magasins extrêmement rapides. Vous trouverez plus d’informations sur NVML, y compris des exemples, à la [bibliothèque NVM](https://pmem.io/nvml/).

## <a name="integrating-nvml-into-a-visual-studio-project"></a>Intégration de NVML dans un projet Visual Studio

1. Télécharger les fichiers et en-têtes de la bibliothèque NVML

-   NVML est conservé sur GitHub. Vous pouvez compiler la source vous-même ou simplement télécharger des binaires compilés directement à partir de cet emplacement : [NVML Version 1,2-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).

2. Placez les fichiers et en-têtes de la bibliothèque dans le répertoire de votre choix, par exemple : « C : \\ NVML \\ lib » et « c : \\ NVML \\ Inc », respectivement.

3. Configurez votre projet comme suit :

-   Ouvrez votre projet Visual Studio et dans le « Explorateur de solutions », cliquez avec le bouton droit sur le nom de votre projet.
-   Ouvrez le volet des paramètres du projet en bas de la fenêtre contextuelle résultante.
-   Accédez à « propriétés de configuration-> C/C++ » et ajoutez le dossier dans lequel vous avez stocké l’en-tête (C : \\ NVML \\ Inc) dans le champ « autres répertoires Include ».
-   Ensuite, accédez à « propriétés de configuration-éditeur de liens > » et ajoutez le dossier dans lequel vous avez stocké la bibliothèque (C : \\ NVML \\ lib) dans le champ « répertoires de bibliothèques supplémentaires ».

4. Ensuite, assurez-vous que vous ciblez le projet pour la mise à jour anniversaire de Windows Server 2016 ou Windows 10 :

-   Accédez à « propriétés de configuration-> général » et définissez le champ « version de la plateforme cible » sur « 10.0.14393.0 » et
-   Accédez à « propriétés de configuration-> C/C++ » et ajoutez « NTDDI \_ version = NTDDI \_ WIN10 \_ RS1 ; » au champ « préprocesseur ».

5. Inclure les en-têtes dans votre code et créer un lien vers les bibliothèques requises

-   À ce stade, vous pouvez simplement inclure les fichiers d’en-tête que vous souhaitez utiliser dans votre code comme n’importe quel autre fichier d’en-tête. Par exemple, pour utiliser libpmem :
    -   Ajoutez « \# include <libpmem. h> » et
    -   Ajoutez « libpmem. lib » à « propriétés de configuration-éditeur de liens-> > d’entrée-> dépendances supplémentaires »

À ce stade, vous êtes prêt à appeler les fonctions de la bibliothèque directement dans votre code et à en tirer parti.

 

 



