---
description: Utilisation des images vidéo
ms.assetid: a5ad74dd-abfd-4810-a512-42e4b98a6c59
title: Utilisation des images vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86407f99138e0b38b67468668fc963bd1bcd7b65e875571643bc7727b4d0d339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870929"
---
# <a name="working-with-video-frames"></a>Utilisation des images vidéo

Une vidéo non compressée est une séquence de bitmaps jouée rapidement, en général à un débit d’environ 30 images par seconde. étant donné que la plupart des vidéos entrent dans un graphique de filtre DirectShow dans un format compressé, le flux vidéo passe généralement par un décodeur pour la décompression. De nombreux décodeurs génèrent des données dans un format YUV et laissent la conversion finale en RVB pour le matériel vidéo juste avant le rendu. Si un décodeur utilise l’accélération vidéo DirectX, le matériel vidéo effectue un travail supplémentaire pour décoder l’image. Ainsi, la décompression finale des bitmaps peut ne pas être effectuée tant que les données n’ont pas atteint le matériel vidéo.

Mais pour effectuer de nombreux types d’analyses vidéo, de traitement ou de modification, il est souvent nécessaire de travailler sur des bitmaps non compressées dans un certain type de format RGB ou YUV avant leur rendu ou leur écriture dans le fichier. Ce travail est généralement effectué dans un filtre de transformation basé sur la classe de base [**CTransformFilter**](ctransformfilter.md) , en particulier dans la méthode **Transform** . Cette méthode reçoit un pointeur vers un objet [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) qui encapsule les données vidéo. La méthode **IMediaSample :: GetPointer** retourne un pointeur vers le premier octet des données brutes. Pour les cadres non compressés, ces données se composent de pixels qui sont accessibles ou modifiés directement par le filtre. Les sections suivantes fournissent des informations générales qui vous aideront à travailler efficacement avec les données DIB de cette manière.

> [!Note]  
> vous pouvez également modifier les bits à l’aide des fonctions GDI, GDI+, DirectDraw ou Direct3D, mais ces techniques n’entrent pas dans le cadre de cet article.

 

Cette section contient les rubriques suivantes :

-   [Bottom-Up de haut en haut et DIB](top-down-vs--bottom-up-dibs.md)
-   [Utilisation d’une couleur RVB 16 bits](working-with-16-bit-rgb.md)

 

 



