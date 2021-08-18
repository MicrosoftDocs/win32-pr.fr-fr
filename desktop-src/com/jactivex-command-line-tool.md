---
title: Outil JActiveX Command-Line
description: L’application de ligne de commande JActiveX est un composant de Visual J++ 6,0.
ms.assetid: b356eb85-5dd4-475b-8d53-8c13a84aa976
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae611e56c44b78398817cd0c78804d343fa97754f80fb3b036ea2705c801070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992649"
---
# <a name="jactivex-command-line-tool"></a>Outil JActiveX Command-Line

L’application de ligne de commande JActiveX est un composant de Visual J++ 6,0. il lit la bibliothèque de types d’un contrôle Microsoft ActiveX et génère les fichiers sources Java correspondants. Vous pouvez ensuite compiler ces fichiers sources et les importer dans votre application Java.

Pour générer des fichiers sources Java pour un objet COM, à partir de l’invite de commandes, exécutez :

 *nom de fichier* JActiveX

où *filename* est le nom du fichier qui contient la bibliothèque de types. Ce fichier peut avoir l’une des extensions de nom de fichier suivantes :. tlb,. olb,. ocx, .dll ou .exe.

Pour plus d’informations sur les paramètres facultatifs que vous pouvez définir dans JActiveX, consultez la documentation de Visual J++ ou tapez la ligne de commande suivante :

**JActiveX/ ?**

> [!WARNING]
> N’utilisez pas les compilateurs Visual J++ avant la version 1.02.3920 pour compiler les fichiers générés par JActiveX.exe. Cela est dû au fait que les fichiers sources générés doivent être compilés avec un @com-aware compilateur. Seuls les compilateurs Visual J++ postérieurs à la version 1.02.3920 sont @com-aware .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en Java](translating-to-java.md)
</dt> </dl>

 

 




