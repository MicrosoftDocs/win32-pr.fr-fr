---
title: Outil JActiveX Command-Line
description: L’application de ligne de commande JActiveX est un composant de Visual J++ 6,0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9975e060a3967f927440111719045378aa812f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509218"
---
# <a name="jactivex-command-line-tool"></a>Outil JActiveX Command-Line

L’application de ligne de commande JActiveX est un composant de Visual J++ 6,0. Il lit la bibliothèque de types d’un contrôle Microsoft ActiveX et génère les fichiers sources Java correspondants. Vous pouvez ensuite compiler ces fichiers sources et les importer dans votre application Java.

Pour générer des fichiers sources Java pour un objet COM, à partir de l’invite de commandes, exécutez :

 *nom de fichier* JActiveX

où *filename* est le nom du fichier qui contient la bibliothèque de types. Ce fichier peut avoir l’une des extensions de nom de fichier suivantes :. tlb,. olb,. ocx,. dll ou. exe.

Pour plus d’informations sur les paramètres facultatifs que vous pouvez définir dans JActiveX, consultez la documentation de Visual J++ ou tapez la ligne de commande suivante :

**JActiveX/ ?**

> [!WARNING]
> N’utilisez pas les compilateurs Visual J++ avant la version 1.02.3920 pour compiler les fichiers générés par JActiveX.exe. Cela est dû au fait que les fichiers sources générés doivent être compilés avec un @com-aware compilateur. Seuls les compilateurs Visual J++ postérieurs à la version 1.02.3920 sont @com-aware .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en Java](translating-to-java.md)
</dt> </dl>

 

 




