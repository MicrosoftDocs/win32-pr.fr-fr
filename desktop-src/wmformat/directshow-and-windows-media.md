---
title: DirectShow et Windows Media
description: DirectShow et Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675677"
---
# <a name="directshow-and-windows-media"></a>DirectShow et Windows Media

En guise d’alternative à l’utilisation du kit de développement logiciel (SDK) Windows Media format exclusivement, les applications peuvent également lire et écrire du contenu Windows Media à l’aide de l’architecture de diffusion en continu Microsoft® DirectShow®, comme décrit dans les sections suivantes.



| Section                                                                                   | Description                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos de DirectShow](about-directshow.md)                                                  | Décrit DirectShow en termes généraux et indique où obtenir plus d’informations à ce sujet.                                                     |
| [Pourquoi utiliser DirectShow ?](why-use-directshow.md)                                             | Décrit comment DirectShow simplifie certaines tâches dans la création et la lecture de contenu basé sur Windows Media.                              |
| [Lecture de fichiers ASF dans DirectShow](reading-asf-files-in-directshow.md)                    | Décrit comment lire des fichiers ASF à l’aide de DirectShow.                                                                                           |
| [Création de fichiers ASF dans DirectShow](creating-asf-files-in-directshow.md)                  | Décrit comment créer des fichiers ASF à l’aide de DirectShow.                                                                                         |
| [\_Notification d’événement d’État WMT dans DirectShow](wmt-status-notification-in-directshow.md) | Décrit les événements d' **\_ État WMT** qui sont gérés par le lecteur ASF et les filtres d’écriture ASF, ainsi que la façon dont les applications peuvent recevoir ces événements. |
| [Prise en charge de DRM dans DirectShow](drm-support-in-directshow.md)                                | Décrit comment lire et écrire des fichiers protégés par DRM par le biais de DirectShow.                                                                     |
| [Informations de référence sur DirectShow QASF](directshow-qasf-reference.md)                                | Contient la documentation de référence pour les composants DirectShow qui prennent en charge Windows Media.                                              |



 

Trois exemples d’applications dans le kit de développement logiciel (SDK) illustrent l’utilisation de DirectShow : DSCopy, DSPlay et DSSeekFM. Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).

> [!Note]  
> Les applications qui utilisent les composants QASF inclus dans ce kit de développement logiciel requièrent l’installation du runtime SDK Microsoft DirectX® 8,1 ou version ultérieure sur les systèmes Windows® 2000, Windows 98 et Windows 95. Plus précisément, ce Runtime est requis par le filtre de wrappers DMO qui héberge les codecs Windows Media dans un graphique de filtre DirectShow.

 

 

 




