---
description: Windows Le composant de création d’images (WIC) simplifie la gestion des couleurs en fournissant l’interface IWICColorContext et l’interface IWICColorTransform.
ms.assetid: d4d761a6-d5a6-47b8-b655-7651bd415e4e
title: Vue d’ensemble de la gestion des couleurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a8c30074210a0a061fcbd26b05054591d2023805bfdff0848f0d7054dfe07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090048"
---
# <a name="color-management-overview"></a>Vue d’ensemble de la gestion des couleurs

Les images numériques proviennent de et sont ciblées sur un large éventail d’appareils, chacun possédant sa propre gamme et sa propre plage dynamique. Si un photographe devait capturer la même scène sur deux caméras différentes, les couleurs des images obtenues n’apparaissent pas exactement les mêmes, même lorsqu’elles sont rendues sur le même périphérique de sortie car les fonctionnalités de la gamme de couleurs des deux périphériques sources étaient différentes. De même, la même image affichée sur deux appareils cibles différents s’affiche différemment, car les appareils cibles ont des profils de couleurs différents. Pour garantir une reproduction homogène des couleurs entre les appareils, il est nécessaire de créer un mappage entre le profil de couleurs de l’appareil source et le profil de couleurs de l’appareil cible. La gestion des couleurs cherche à produire une correspondance visuelle étroite et cohérente et est une fonctionnalité essentielle de la création d’images professionnelles.

La possibilité de reproduire de manière cohérente les couleurs entre les scanneurs, les moniteurs, les imprimantes et les applications ressemble à un objectif simple, mais sans système de gestion des couleurs dans le système d’exploitation, il est difficile d’y parvenir. Si chaque application est requise pour générer ses propres profils de couleurs, il est presque impossible d’obtenir un échange de couleurs cohérent tout au long du processus de publication, y compris l’analyse, la modification et la composition, la vérification et la distribution.

Windows Le composant de création d’images (WIC) simplifie la gestion des couleurs en fournissant l’interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) et l’interface [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) . Vous pouvez récupérer un objet [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) à l’aide de [**IWICFactory :: CreateColorTransformer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcolortransformer). Le [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) est une abstraction du profil de couleurs de l’appareil. **IWICColorContext** est initialisé avec un frame bitmap, le profil de couleurs de l’appareil source et le profil de couleurs de l’appareil cible. Il effectue la conversion du frame bitmap.

 

 



