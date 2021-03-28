---
description: Une application peut dessiner le contour d’un tracé en appelant la fonction StrokePath, elle peut remplir l’intérieur d’un tracé en appelant la fonction FillPath, et elle peut à la fois tracer et remplir le tracé en appelant la fonction StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Tracés détaillés et remplis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951554"
---
# <a name="outlined-and-filled-paths"></a>Tracés détaillés et remplis

Une application peut dessiner le contour d’un tracé en appelant la fonction [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) , elle peut remplir l’intérieur d’un tracé en appelant la fonction [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) , et elle peut à la fois tracer et remplir le tracé en appelant la fonction [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) .

Chaque fois qu’une application remplit un chemin d’accès, le système utilise le mode de remplissage actuel du contrôleur de réseau. Une application peut récupérer ce mode en appelant la fonction [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) , et elle peut définir un nouveau mode de remplissage en appelant la fonction [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . Pour obtenir une description des deux modes de remplissage, consultez [régions](regions.md).

L’illustration suivante montre la section transversale d’un objet créé par une application de conception assistée par ordinateur à l’aide de chemins d’accès qui ont été indiqués et remplis.

![Illustration montrant la vue en plusieurs sections d’un objet, avec différentes parties indiquées par des motifs de remplissage différents](images/cspth-01.png)

 

 



