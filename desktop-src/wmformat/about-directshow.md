---
title: en savoir plus sur les DirectShow dans le kit de développement logiciel (SDK) Windows Media Format 11, une architecture de diffusion de données de haut niveau, modulaire et extensible pour la plateforme Windows.
description: À propos de DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- DirectShow, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aeb5dc9ebc613f7820a8ba4c4f5877ce9ac27068f1c4e873f9e8b00ec2f3b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840408"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>à propos de DirectShow (kit de développement logiciel (SDK) Windows Media Format 11)

DirectShow est une architecture de diffusion en continu modulaire, modulaire et de haut niveau pour la plateforme Windows. Il fournit les composants logiciels sous-jacents et les interfaces de programmation d’application (API) pour un large éventail d’applications audio et vidéo numériques sur le marché dès aujourd’hui. DirectShow est disponible dans le cadre du Kit de développement logiciel (sdk) Microsoft DirectX. pour en savoir plus sur DirectShow, consultez le kit de développement logiciel (SDK) Microsoft platform.

dans DirectShow, tous les composants de streaming de données sont appelés *filtres*. Un filtre peut représenter un périphérique matériel, un codeur logiciel ou un décodeur, un convertisseur audio ou vidéo, ou toute fonctionnalité de traitement audio/vidéo. pour permettre aux applications basées sur DirectShow de lire et d’écrire Windows contenu multimédia au format, notamment le contenu protégé par la Rights Management numérique (DRM), Microsoft fournit deux filtres qui encapsulent des portions du kit de développement logiciel (SDK) Windows Media format. Il s’agit du [lecteur ASF WM](wm-asf-reader-filter.md) et de l' [enregistreur ASF WM](wm-asf-writer-filter.md). Ces filtres et les interfaces qu’ils exposent sont collectivement désignés sous le terme de composants QASF, après la DLL dans laquelle ils sont empaquetés. (Q représente quartz, un nom de code précoce pour DirectShow.)

> [!Note]  
> l’utilisation des codecs de série Windows Media Audio et Video 9 par le biais des composants DirectShow QASF nécessite Microsoft Windows Millennium Edition ou version ultérieure, ou DirectX 8,0 ou version ultérieure.

 

le diagramme suivant montre un graphique de filtre DirectShow permettant de lire les fichiers Windows Media Video.

![graphique de lecture vidéo Windows Media](images/wmv-wmasfreader.png)

le [lecteur ASF WM](wm-asf-reader-filter.md) est un composant QASF, les décodeurs sont Windows les composants du kit de développement logiciel (SDK) Media Format hébergés dans le filtre de Wrapper DMO (composant QASF) et les convertisseurs sont DirectShow composants.

 

 




