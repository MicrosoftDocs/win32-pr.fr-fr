---
title: Découvrez DirectShow dans le kit de développement logiciel (SDK) Windows Media format 11, architecture de haut niveau, modulaire et extensible de diffusion de données pour la plate-forme Windows.
description: À propos de DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011292"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>À propos de DirectShow (SDK Windows Media format 11)

DirectShow est une architecture de diffusion en continu modulaire, modulaire et de haut niveau pour la plate-forme Windows. Il fournit les composants logiciels sous-jacents et les interfaces de programmation d’application (API) pour un large éventail d’applications audio et vidéo numériques sur le marché dès aujourd’hui. DirectShow est disponible dans le cadre du kit de développement logiciel (SDK) Microsoft DirectX. Pour en savoir plus sur DirectShow, consultez le kit de développement logiciel (SDK) Microsoft Platform.

Dans DirectShow, tous les composants de streaming de données sont appelés *filtres*. Un filtre peut représenter un périphérique matériel, un codeur logiciel ou un décodeur, un convertisseur audio ou vidéo, ou toute fonctionnalité de traitement audio/vidéo. Pour permettre aux applications DirectShow de lire et d’écrire du contenu au format Windows Media, y compris le contenu protégé par les Rights Management numériques (DRM), Microsoft fournit deux filtres qui encapsulent des portions du kit de développement logiciel (SDK) de format Windows Media. Il s’agit du [lecteur ASF WM](wm-asf-reader-filter.md) et de l' [enregistreur ASF WM](wm-asf-writer-filter.md). Ces filtres et les interfaces qu’ils exposent sont collectivement désignés sous le terme de composants QASF, après la DLL dans laquelle ils sont empaquetés. (Q représente quartz, un nom de code précoce pour DirectShow.)

> [!Note]  
> L’utilisation des codecs de série Windows Media Audio et Video 9 par le biais des composants QASF DirectShow nécessite Microsoft Windows Millennium Edition ou version ultérieure, ou DirectX 8,0 ou version ultérieure.

 

Le diagramme suivant montre un graphique de filtre DirectShow permettant de lire les fichiers Windows Media Video.

![graphique de lecture vidéo Windows Media](images/wmv-wmasfreader.png)

Le [lecteur ASF WM](wm-asf-reader-filter.md) est un composant qasf, les décodeurs sont des composants du kit de développement logiciel (SDK) de format Windows Media hébergés dans le filtre de wrappers DMO (un composant qasf) et les convertisseurs sont des composants DirectShow.

 

 




