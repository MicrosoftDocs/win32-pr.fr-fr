---
description: La création d’une application compatible avec l’exécution automatique est une procédure simple. Cette rubrique utilise CD-ROM comme exemple (il s’agit du premier moyen d’implémenter cette technologie), mais aujourd’hui, il existe de nombreux types de médias différents qui peuvent l’utiliser.
title: Création d’une application AutoRun-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: f3a3c265f71b0bdf66d7825e65eb69ab975bfc6bffa5c9a8674ed5a0fb8feb38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224931"
---
# <a name="creating-an-autorun-enabled-application"></a>Création d’une application AutoRun-Enabled

La création d’une application compatible avec l’exécution automatique est une procédure simple. Cette rubrique utilise CD-ROM comme exemple (il s’agit du premier moyen d’implémenter cette technologie), mais aujourd’hui, il existe de nombreux types de médias différents qui peuvent l’utiliser.

Pour activer l’exécution automatique dans votre application, il vous suffit d’inclure deux fichiers essentiels :

-   Un fichier autorun. inf
-   Une application de démarrage

Lorsqu’un utilisateur insère un disque dans un lecteur de CD-ROM sur un ordinateur compatible avec l’exécution automatique, le système vérifie immédiatement si le disque dispose d’un système de fichiers d’ordinateur personnel. Si c’est le cas, le système recherche un fichier nommé [Autorun. inf](#creating-an-autoruninf-file). Ce fichier spécifie une application d’installation qui sera exécutée, ainsi que divers paramètres facultatifs. L’application de démarrage installe, désinstalle, configure et peut-être l’application.

-   [Création d’un fichier autorun. inf](#creating-an-autoruninf-file)
-   [\[Section DeviceInstall \]](#the-deviceinstall-section)
-   [Rubriques connexes](#related-topics)

## <a name="creating-an-autoruninf-file"></a>Création d’un fichier autorun. inf

Autorun. inf est un fichier texte situé dans le répertoire racine du CD-ROM qui contient votre application. Sa fonction principale est de fournir au système le nom et l’emplacement du programme de démarrage de l’application qui sera exécuté lors de l’insertion du disque.

> [!Note]  
> les fichiers Autorun. inf ne sont pas pris en charge sous Windows XP pour les lecteurs qui retournent un disque \_ amovible de [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).

 

Le fichier autorun. inf peut également contenir des informations facultatives, notamment :

-   Nom d’un fichier qui contient une icône qui représente le lecteur de CD-ROM de votre application. cette icône sera affichée par Windows Explorer à la place de l’icône de lecteur standard.
-   Commandes supplémentaires pour le menu contextuel qui s’affiche quand l’utilisateur clique avec le bouton droit sur l’icône CD-ROM. Vous pouvez également spécifier la commande par défaut qui est exécutée lorsque l’utilisateur double-clique sur l’icône.

Les fichiers autorun. inf sont similaires aux fichiers .ini. Ils se composent d’une ou de plusieurs sections, chacune portant un nom placé entre crochets. Chaque section contient une série de commandes qui seront exécutées par l’interpréteur de commandes lorsque le disque est inséré. Deux sections sont actuellement définies pour les fichiers autorun. inf.

-   La section **\[ Autorun \]** contient les commandes d’exécution automatique par défaut. Tous les fichiers autorun. inf doivent disposer d’une section d' **\[ exécution automatique \]** .
-   Une section **\[ Autorun. alpha \]** facultative peut être incluse pour les systèmes qui s’exécutent sur des ordinateurs basés sur RISC. Lorsqu’un disque est inséré dans un lecteur de CD-ROM sur un système RISC, l’interpréteur de commandes exécute les commandes de cette section au lieu de celles figurant dans la section d' **\[ exécution automatique \]** .

> [!Note]  
> Le shell recherche d’abord une section spécifique à l’architecture. S’il n’en trouve pas, il utilise les informations de la section **\[ exécution automatique \]** . Une fois que l’interpréteur de commandes a trouvé une section, il ignore toutes les autres, donc chaque section doit être autonome.

 

Chaque section contient une série de commandes qui déterminent la façon dont l’opération d’exécution automatique a lieu. Cinq commandes sont disponibles.



| Commande                         | Description                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [DefaultIcon](autorun-cmds.md) | Spécifie l’icône par défaut pour l’application.                                        |
| [Icône](autorun-cmds.md)        | Spécifie le chemin d’accès et le nom de fichier d’une icône spécifique à l’application pour le lecteur de CD-ROM. |
| [open](autorun-cmds.md)        | Spécifie le chemin d’accès et le nom de fichier de l’application de démarrage.                           |
| [useautorun](autorun-cmds.md)  | Spécifie que les fonctionnalités de lecture automatique v2 doivent être utilisées si elles sont prises en charge.                       |
| [Shell](autorun-cmds.md)       | Définit la commande par défaut dans le menu contextuel du CD-ROM.                             |
| [verbe de Shell \_](autorun-cmds.md) | Ajoute des commandes au menu contextuel du CD-ROM.                                           |



 

Voici un exemple de fichier autorun. inf simple. Il spécifie Filename.exe comme application de démarrage. La deuxième icône dans Filename.exe représente le lecteur de CD-ROM au lieu de l’icône de lecteur standard.


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



Cet exemple autorun. inf exécute différentes applications de démarrage en fonction du type d’ordinateur.


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a>\[Section DeviceInstall \]

Vous pouvez utiliser la section **\[ DeviceInstall \]** sur n’importe quel support amovible. il est pris en charge uniquement sous Windows XP. vous utilisez **DriverPath** pour spécifier un chemin d’accès de répertoire dans lequel Windows XP recherche des fichiers de pilote, ce qui empêche toute recherche longue dans tout le contenu.

vous utilisez la section **\[ DeviceInstall \]** avec une installation de pilote pour spécifier les répertoires dans lesquels Windows XP doit rechercher les fichiers de pilote dans le média. sous Windows XP, les supports entiers ne sont plus recherchés par défaut, ce qui nécessite que **\[ DeviceInstall \]** spécifie les emplacements de recherche. voici le seul support amovible qui Windows XP effectue une recherche complète sans section **\[ DeviceInstall \]** dans un fichier Autorun. inf.

-   Disquettes détectées dans les lecteurs A ou B.
-   Support CD/DVD moins de 1 gigaoctet (Go).

tous les autres supports doivent inclure une section **\[ DeviceInstall \]** pour Windows XP afin de détecter les pilotes stockés sur ce média.

> [!Note]  
> Comme avec la section d' **\[ exécution automatique \]** , la section **\[ DeviceInstall \]** peut être spécifique à l’architecture.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment implémenter des applications de démarrage autorun](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[Écriture d’une application d’installation d’appareil](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
