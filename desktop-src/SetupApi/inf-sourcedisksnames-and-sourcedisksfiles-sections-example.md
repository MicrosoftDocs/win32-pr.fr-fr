---
description: La section SourceDisksNames d’un fichier INF identifie les disques qui contiennent les fichiers sources en cours d’installation.
ms.assetid: af4bc466-f0a3-4f83-adb7-6bfc276f7764
title: Exemple de sections INF SourceDisksNames et SourceDisksFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00eb8241b8e290f5460cc41b233d3b199df35e709d6e32f2c5a39925a79f851d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739409"
---
# <a name="inf-sourcedisksnames-and-sourcedisksfiles-sections-example"></a>Exemple de sections INF SourceDisksNames et SourceDisksFiles

La section **SourceDisksNames** d’un fichier INF identifie les disques qui contiennent les fichiers sources en cours d’installation. La section **SourceDisksFiles** identifie les fichiers sources et les disques sources qui les contiennent. notez que les plateformes MIPS, Alpha et PPC ne sont pas prises en charge par Windows 2000 ou Windows XP.

à partir de Windows XP, une section **SourceDisksNames** peut spécifier une balise et un fichier cab. Par exemple, la section **SourceDisksNames** suivante peut être utilisée avec un média fixe ou amovible. Si vous utilisez un support amovible, la section exemple vérifie la présence du média en vérifiant d’abord la présence de la balise. Si vous utilisez un média fixe, la section exemple vérifie la présence du média en vérifiant d’abord la présence du fichier CAB. Après vérification de la présence d’un fichier CAB, le système tente de copier les fichiers en dehors de l’armoire et demande tous les fichiers qu’il n’a pas pu copier.

``` syntax
[SourceDisksNames]
1="Dajava" , "Dajava.cab",,, 0x10,"Dajava.tag"
```

pour plus d’informations sur **SourceDisksNames** ou **SourceDisksFiles**, consultez les sections « instructions générales pour le fichier inf » et « sections et Directives du fichier inf » du Kit de développement de pilotes Microsoft Windows 2000.

 

 



