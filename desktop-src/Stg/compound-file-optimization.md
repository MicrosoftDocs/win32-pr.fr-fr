---
title: Optimisation des fichiers composés
description: Le stockage asynchrone permet aux applications de mettre en page précisément des fichiers composés afin que les données soient disponibles dans l’ordre dans lequel les applications en ont besoin.
ms.assetid: 0737c5b2-09f6-4993-bb42-f2a684e5a136
keywords:
- Optimisation des fichiers composés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb55d4d9ba7b264c1a0aac4252d879a7ba98b6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671666"
---
# <a name="compound-file-optimization"></a>Optimisation des fichiers composés

Le stockage asynchrone permet aux applications de mettre en page précisément des fichiers composés afin que les données soient disponibles dans l’ordre dans lequel les applications en ont besoin. Si une application ne requiert qu’une partie de ses données pour afficher une première page d’informations, ces données peuvent être placées au début du fichier, même si elles résident logiquement à la fin d’un flux. Les données de différents flux peuvent être entrelacées. Par exemple, les données audio et vidéo peuvent être entrelacées afin que les opérations de lecture suivantes récupèrent les deux simultanément, une exigence pour les applications multimédias.

[**IStorage :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) peut être utilisé pour mettre en forme un DOCFILE, ce qui améliore les performances dans la plupart des scénarios.

 

 




