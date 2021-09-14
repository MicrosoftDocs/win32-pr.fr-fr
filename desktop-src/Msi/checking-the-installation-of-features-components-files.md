---
description: Si, après avoir exécuté une installation, vous devez vérifier qu’une fonctionnalité, un composant ou un fichier particulier a été installé, activez l’option de journalisation détaillée au cours de l’installation. consultez Windows Installer la journalisation et les Options de ligne de commande.
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: Vérification de l’installation des fonctionnalités, des composants, des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cab15b4f0590ee5613865d4b7c21439eec6dbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092253"
---
# <a name="checking-the-installation-of-features-components-files"></a>Vérification de l’installation des fonctionnalités, des composants, des fichiers

Si, après avoir exécuté une installation, vous devez vérifier qu’une fonctionnalité, un composant ou un fichier particulier a été installé, activez l’option de journalisation détaillée au cours de l’installation. consultez [Windows Installer la journalisation](windows-installer-logging.md) et les [Options de ligne de commande](command-line-options.md).

Le journal détaillé contient une entrée pour chaque fonctionnalité et composant que le package d’installation peut installer. Le journal indique l’état de cette fonctionnalité ou de ce composant avant l’installation, l’État demandé par l’installation et l’État dans lequel le programme d’installation a quitté la fonctionnalité ou le composant. Les entrées de fonctionnalités et de composants dans le journal s’affichent comme dans les exemples suivants.

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

Ce journal détaillé indique que :

-   l’état d’installation de la fonctionnalité et du composant QuickTest est absent avant l’exécution du package
-   le package a demandé une installation locale de ces
-   la fonctionnalité et le composant étaient tous deux laissés dans l’état installé localement après l’exécution du package.

L’étiquette « installed » dans le journal fait référence à l’état d’installation actuel de la fonctionnalité ou du composant, « request » fait référence à l’état d’installation demandé de la fonctionnalité ou du composant. « Action » fait référence à l’état d’action réel de la fonctionnalité ou du composant.

Le tableau suivant répertorie les États des composants ou des fonctionnalités possibles qui peuvent s’afficher dans le journal.



| Entrée du journal              | Description                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Demande : null          | Aucune demande.                                                                                                     |
| Action : null           | Aucune action effectuée.                                                                                                |
| Installé : absent      | Le composant ou la fonctionnalité n’est pas installé actuellement.                                                                |
| Demande : absente        | Le composant ou la fonctionnalité de demande d’installation doit être désinstallé.                                                      |
| Action : absent         | Le programme d’installation désinstalle réellement le composant ou la fonctionnalité.                                                             |
| Installé : local       | Le composant ou la fonctionnalité est actuellement installé pour s’exécuter localement.                                                       |
| Demande : local         | Le composant ou la fonctionnalité de demande d’installation doit être installé pour s’exécuter en local.                                           |
| Action : locale          | Le programme d’installation installe le composant ou la fonctionnalité pour une exécution locale.                                                  |
| Installé : source      | Le composant ou la fonctionnalité est actuellement installé pour s’exécuter à partir de la source.                                                 |
| Demandé : source      | L’installation demande que le composant ou la fonctionnalité soit installé pour s’exécuter à partir de la source.                                |
| Action : source         | Le programme d’installation installe réellement le composant ou la fonctionnalité à exécuter à partir de la source.                                        |
| Installé : publier   | La fonctionnalité est actuellement publiée. Les composants ne sont jamais publiés.                                               |
| Demande : publier     | La fonctionnalité des demandes d’installation doit être installée en tant que fonctionnalité publiée.                                            |
| Action : publier      | Le programme d’installation installe la fonctionnalité en tant que fonctionnalité publiée.                                               |
| Demande : réinstaller     | La fonctionnalité des demandes d’installation doit être réinstallée. Les composants n’utilisent pas l’État réinstallation.                            |
| Action : réinstaller      | Le programme d’installation réinstalle réellement la fonctionnalité.                                                                          |
| Installé : actuel     | La fonctionnalité est actuellement installée dans l’état d’installation par défaut.                                           |
| Demande : en cours       | Le composant demandes d’installation doit être installé dans l’état d’installation par défaut.                               |
| Action : en cours        | Le programme d’installation installe la fonctionnalité dans l’état d’installation par défaut.                                  |
| Action : FileAbsent     | Le programme d’installation désinstalle réellement les fichiers du composant et laisse toutes les autres ressources du composant installées.      |
| Action : HKCRAbsent     | Le programme d’installation supprime en fait les informations HKCR du composant. Les informations de fichier et de non-HKCR sont conservées.                  |
| Action : HKCRFileAbsent | Le programme d’installation supprime en fait les informations et les fichiers HKCR du composant. Toutes les autres ressources du composant sont conservées. |



 

Le journal détaillé contient une entrée pour chaque fichier qui peut être installé par le package. Le journal indique ce qui a été fait dans le fichier et fournit une explication. Les entrées de fichier dans le journal apparaissent comme dans l’exemple suivant.

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

Ce journal indique que le programme d’installation ne remplacera pas le fichier Testdb.exe existant, car le fichier existant est identique à la version en cours d’installation.

> [!Note]  
> Si vous avez besoin de créer un package d’installation qui recherche un fichier ou un répertoire existant sur l’ordinateur de l’utilisateur au cours d’une installation, utilisez la méthode décrite dans [recherche d’applications, de fichiers, d’entrées de registre ou de .ini d’entrées de fichier existants](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

 

 

 



