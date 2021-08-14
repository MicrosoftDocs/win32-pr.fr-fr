---
description: L’illustration suivante montre la relation entre les applications d’analyse et d’analyse et d’autres composants de l’architecture Moniteur réseau.
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: Architecture de l’analyseur et de l’expert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261343005f0cb9fc7de5b7025f9ffe59f11515614ab43609c1b8da9f396e9f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795839"
---
# <a name="expert-and-parser-architecture"></a>Architecture de l’analyseur et de l’expert

L’illustration suivante montre la [relation entre les](experts.md) applications d’analyse et d' [analyse](parsers.md) et d’autres composants de l’architecture Moniteur réseau.

![relation entre les applications d’analyse et d’experts](images/nm-arch1.png)

Le trafic réseau est collecté, sous forme de trames individuelles, à partir du pilote NDIS. Le pilote de Moniteur réseau (Nmnt.sys) achemine ensuite les trames vers un fournisseur de paquets réseau (NPP), qui capture les données et les place dans un ou plusieurs fichiers de capture. Le NPP est une collection d’interfaces COM utilisées pour capturer des données. Dans ce cas, l’interface [**IDelaydC**](idelaydc.md) est utilisée pour effectuer une capture différée.

> [!Note]  
> Le NPP est utilisé pour les captures retardées et en temps réel. Pour les captures en temps réel, l’interface [**IRTC**](irtc.md) est utilisée.

 

Lorsque les trames réseau sont stockées dans le fichier de capture et que le fichier est accessible, les experts et les analyseurs peuvent utiliser l’interface utilisateur Moniteur réseau et les fonctions Moniteur réseau fournies dans Nmapi.dll pour analyser les données. Les fichiers de capture ne sont pas accessibles tant que la capture n’est pas terminée.

 

 



