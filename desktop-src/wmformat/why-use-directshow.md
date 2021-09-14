---
title: Pourquoi utiliser DirectShow
description: Pourquoi utiliser DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, matériel
- Windows kit de développement logiciel (SDK) Media Format, Windows Driver Model (WDM)
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), matériel
- ASF (format des systèmes avancés), matériel
- ASF (Advanced Systems Format), Windows Driver Model (WDM)
- ASF (Format des systèmes avancés), Windows Driver Model (WDM)
- DirectShow, à propos de
- DirectShow, matériel
- DirectShow, Windows Driver Model (WDM)
- Windows Modèle de pilote (WDM)
- WDM (Windows Driver Model)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195907"
---
# <a name="why-use-directshow"></a>Pourquoi utiliser DirectShow ?

il existe deux raisons principales pour lesquelles une application peut utiliser DirectShow plutôt que le kit de développement logiciel (SDK) de Format de média Windows directement : pour la commodité de l’architecture de diffusion en continu DirectShow et pour l’accès au matériel.

## <a name="convenience"></a>Aspect pratique

avec DirectShow architecture de diffusion en continu, il n’y a que quelques appels de méthode pour lire Windows Media Audio ou Windows Media Video fichiers. La création de fichiers est également simplifiée. vous spécifiez simplement un profil à l’aide de l’interface **IConfigAsfWriter** sur le filtre, et DirectShow charge automatiquement les composants requis pour le rendu ou l’écriture des flux, et fournit les mécanismes de transfert et de synchronisation du flux de données multimédias. DirectShow est particulièrement utile lors de la conversion de contenu de formats variés en Windows Format multimédia. vous pouvez créer DirectShow des graphiques de filtre qui décodent un large éventail de types de fichiers et de compression, puis qui alimentent les flux décodés dans le filtre de l' [enregistreur ASF WM](wm-asf-writer-filter.md) . Par comparaison, l’exemple UncompAVItoWMV dans ce kit de développement logiciel (SDK) fonctionne uniquement avec les fichiers AVI non compressés. les flux de texte et les flux de données arbitraires peuvent également être créés et/ou rendus à l’aide de DirectShow, mais cela peut nécessiter la création de filtres de DirectShow personnalisés pour le traitement de ces flux.

## <a name="access-to-hardware"></a>Accès au matériel

DirectShow est le seul moyen pour le code d’application d’accéder à des périphériques matériels basés sur des Windows Driver Model (WDM), tels que des caméras DV 1394, des tuners TV et des webcams USB. si votre application doit capturer les données directement à partir d’un périphérique matériel WDM et les transcoder au Format de média Windows, et que le kit de développement logiciel (SDK) Windows media encoder ne répond pas à vos besoins, DirectShow est la seule alternative. DirectShow peut également être utilisé pour accéder à des appareils hérités en fonction de la vidéo de Windows.

 

 




