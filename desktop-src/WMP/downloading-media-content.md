---
title: Téléchargement du contenu multimédia
description: Téléchargement du contenu multimédia
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Magasins en ligne du lecteur Windows Media, téléchargement de contenu multimédia
- magasins en ligne, téléchargement de contenu multimédia
- tapez 1 magasins en ligne, téléchargement de contenu multimédia
- Windows Media Player Online stores, téléchargement de contenu multimédia
- magasins en ligne, téléchargement de contenu multimédia
- types 1 magasins en ligne, téléchargement de contenu multimédia
- contenu multimédia, téléchargement
- Téléchargement du contenu multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104381681"
---
# <a name="downloading-media-content"></a>Téléchargement du contenu multimédia

Le lecteur Windows Media gère les téléchargements de fichiers musicaux pour le magasin en ligne. Un téléchargement peut être lancé lorsque la page de découverte appelle [External. Download](external-download.md) ou lorsque l’utilisateur choisit, dans le lecteur, de télécharger un ensemble de pistes. Dans les deux cas, le lecteur Windows Media appelle [IWMPContentPartner ::D lécharger](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), en passant une liste de conteneurs de contenu qui décrit l’ensemble des pistes à télécharger et un cookie qui représente la transaction de téléchargement. Le plug-in de partenaire de contenu doit ensuite appeler [IWMPContentPartnerCallback ::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) une fois pour chaque piste du jeu. Quand le plug-in appelle **DownloadTrack**, il passe un **HRESULT** dans le paramètre *hrDownload* . Si le plug-in transmet un code de réussite dans *hrDownload*, le lecteur Windows Media télécharge la piste. Si le plug-in passe un code d’échec dans *hrDownload*, le lecteur ne télécharge pas la piste. Pour chaque appel de **Téléchargement**, le plug-in doit fournir le cookie de transaction et l’ID de la piste en question. Pour les pistes qui sont réellement téléchargées, le plug-in doit également fournir l’URL de la piste.

Après le téléchargement d’un fichier, le lecteur Windows Media met automatiquement à jour la bibliothèque pour refléter la musique récemment achetée. Le lecteur fournit des informations d’État au plug-in sur l’opération de téléchargement en appelant [IWMPContentPartner ::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete). Dans cette méthode, le lecteur fournit un **HRESULT** pour indiquer la réussite ou l’échec du téléchargement, l’ID de la piste et la chaîne de paramètres personnalisés fournie par le magasin en ligne lorsqu’il a appelé **DownloadTrack**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins de type 1 en ligne**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




