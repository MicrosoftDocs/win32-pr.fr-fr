---
title: support DirectShow et Windows
description: support DirectShow et Windows
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293159"
---
# <a name="directshow-and-windows-media"></a>support DirectShow et Windows

en guise d’alternative à l’utilisation du kit de développement logiciel (SDK) Windows media Format exclusivement, les applications peuvent également lire et écrire du contenu multimédia Windows à l’aide de Microsoft® DirectShow® architecture de diffusion en continu, comme décrit dans les sections suivantes.



| Section                                                                                   | Description                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos de DirectShow](about-directshow.md)                                                  | décrit DirectShow en termes généraux et indique où obtenir plus d’informations à ce sujet.                                                     |
| [Pourquoi utiliser DirectShow ?](why-use-directshow.md)                                             | décrit comment DirectShow simplifie certaines tâches lors de la création et de la lecture de contenu basé sur des médias Windows.                              |
| [Lecture des fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)                    | Décrit comment lire des fichiers ASF à l’aide de DirectShow.                                                                                           |
| [Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)                  | Décrit comment créer des fichiers ASF à l’aide de DirectShow.                                                                                         |
| [\_Notification d’événement d’État WMT dans DirectShow](wmt-status-notification-in-directshow.md) | Décrit les événements d' **\_ État WMT** qui sont gérés par le lecteur ASF et les filtres d’écriture ASF, ainsi que la façon dont les applications peuvent recevoir ces événements. |
| [Prise en charge de DRM dans DirectShow](drm-support-in-directshow.md)                                | Décrit comment lire et écrire des fichiers protégés par DRM par le biais de DirectShow.                                                                     |
| [DirectShow Référence QASF](directshow-qasf-reference.md)                                | contient la documentation de référence pour les composants DirectShow qui prennent en charge Windows média.                                              |



 

trois exemples d’applications dans le kit de développement logiciel (SDK) illustrent l’utilisation de DirectShow : DSCopy, DSPlay et DSSeekFM. Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).

> [!Note]  
> les Applications qui utilisent les composants QASF inclus dans ce kit de développement logiciel requièrent l’installation du runtime sdk Microsoft DirectX® 8,1 ou version ultérieure sur Windows® 2000, Windows 98 et Windows 95 systèmes. plus précisément, ce runtime est requis par le filtre de Wrapper DMO qui héberge les codecs multimédias Windows dans un graphique de filtre DirectShow.

 

 

 




