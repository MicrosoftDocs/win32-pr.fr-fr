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
# <a name="compound-file-optimization"></a><span data-ttu-id="f9431-104">Optimisation des fichiers composés</span><span class="sxs-lookup"><span data-stu-id="f9431-104">Compound File Optimization</span></span>

<span data-ttu-id="f9431-105">Le stockage asynchrone permet aux applications de mettre en page précisément des fichiers composés afin que les données soient disponibles dans l’ordre dans lequel les applications en ont besoin.</span><span class="sxs-lookup"><span data-stu-id="f9431-105">Asynchronous storage enables applications to precisely layout compound files so that data is available in the order in which applications will require it.</span></span> <span data-ttu-id="f9431-106">Si une application ne requiert qu’une partie de ses données pour afficher une première page d’informations, ces données peuvent être placées au début du fichier, même si elles résident logiquement à la fin d’un flux.</span><span class="sxs-lookup"><span data-stu-id="f9431-106">If an application requires only part of its data to display a first page of information, this data can be placed at the beginning of the file, even if it logically resides at the end of a stream.</span></span> <span data-ttu-id="f9431-107">Les données de différents flux peuvent être entrelacées.</span><span class="sxs-lookup"><span data-stu-id="f9431-107">Data from different streams can be interleaved.</span></span> <span data-ttu-id="f9431-108">Par exemple, les données audio et vidéo peuvent être entrelacées afin que les opérations de lecture suivantes récupèrent les deux simultanément, une exigence pour les applications multimédias.</span><span class="sxs-lookup"><span data-stu-id="f9431-108">Audio and video data, for example, can be interleaved so that subsequent read operations retrieve both simultaneously, a requirement for multimedia applications.</span></span>

<span data-ttu-id="f9431-109">[**IStorage :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) peut être utilisé pour mettre en forme un DOCFILE, ce qui améliore les performances dans la plupart des scénarios.</span><span class="sxs-lookup"><span data-stu-id="f9431-109">[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) can be used to layout a docfile, thus improving performance in most scenarios.</span></span>

 

 




