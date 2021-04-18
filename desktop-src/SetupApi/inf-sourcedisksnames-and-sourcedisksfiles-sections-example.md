---
description: La section SourceDisksNames d’un fichier INF identifie les disques qui contiennent les fichiers sources en cours d’installation.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Exemple de sections INF SourceDisksNames et SourceDisksFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f991727a8a2ca9cce2bd2d7161dfbf27b62ce74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519434"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>Exemple de sections INF SourceDisksNames et SourceDisksFiles

La section **SourceDisksNames** d’un fichier INF identifie les disques qui contiennent les fichiers sources en cours d’installation. La section **SourceDisksFiles** identifie les fichiers sources et les disques sources qui les contiennent. Notez que les plateformes MIPS, alpha et PPC ne sont pas prises en charge par Windows 2000 ou Windows XP.

À partir de Windows XP, une section **SourceDisksNames** peut spécifier une balise et un fichier CAB. Par exemple, la section **SourceDisksNames** suivante peut être utilisée avec un média fixe ou amovible. Si vous utilisez un support amovible, la section exemple vérifie la présence du média en vérifiant d’abord la présence de la balise. Si vous utilisez un média fixe, la section exemple vérifie la présence du média en vérifiant d’abord la présence du fichier CAB. Après vérification de la présence d’un fichier CAB, le système tente de copier les fichiers en dehors de l’armoire et demande tous les fichiers qu’il n’a pas pu copier.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

Pour plus d’informations sur **SourceDisksNames** ou **SourceDisksFiles**, consultez les sections « instructions générales pour le fichier INF » et « sections et directives du fichier INF » du kit de développement de pilotes Microsoft Windows 2000.

 

 



