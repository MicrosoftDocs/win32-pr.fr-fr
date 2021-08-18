---
title: Téléchargement du contenu multimédia
description: Téléchargement du contenu multimédia
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Lecteur Windows Media des magasins en ligne, téléchargement de contenu multimédia
- magasins en ligne, téléchargement de contenu multimédia
- tapez 1 magasins en ligne, téléchargement de contenu multimédia
- magasins en ligne Lecteur Windows Media, téléchargement de contenu multimédia
- magasins en ligne, téléchargement de contenu multimédia
- types 1 magasins en ligne, téléchargement de contenu multimédia
- contenu multimédia, téléchargement
- Téléchargement du contenu multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a314dc4b59966fd779660a2c1ab26fc2b37d413e4add068f936a6109acd423a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997029"
---
# <a name="downloading-media-content"></a>Téléchargement du contenu multimédia

Lecteur Windows Media gère les téléchargements de fichiers musicaux pour le magasin en ligne. Un téléchargement peut être lancé lorsque la page de découverte appelle [External. Download](external-download.md) ou lorsque l’utilisateur choisit, dans le lecteur, de télécharger un ensemble de pistes. dans les deux cas, Lecteur Windows Media appelle [IWMPContentPartner ::D lécharger](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), en passant une liste de conteneurs de contenu qui décrit l’ensemble des pistes à télécharger et un cookie qui représente la transaction de téléchargement. Le plug-in de partenaire de contenu doit ensuite appeler [IWMPContentPartnerCallback ::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) une fois pour chaque piste du jeu. Quand le plug-in appelle **DownloadTrack**, il passe un **HRESULT** dans le paramètre *hrDownload* . si le plug-in transmet un code de réussite dans *hrDownload*, Lecteur Windows Media télécharge la piste. Si le plug-in passe un code d’échec dans *hrDownload*, le lecteur ne télécharge pas la piste. Pour chaque appel de **Téléchargement**, le plug-in doit fournir le cookie de transaction et l’ID de la piste en question. Pour les pistes qui sont réellement téléchargées, le plug-in doit également fournir l’URL de la piste.

après le téléchargement d’un fichier, Lecteur Windows Media met automatiquement à jour la bibliothèque pour refléter la musique qui vient d’être achetée. Le lecteur fournit des informations d’État au plug-in sur l’opération de téléchargement en appelant [IWMPContentPartner ::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete). Dans cette méthode, le lecteur fournit un **HRESULT** pour indiquer la réussite ou l’échec du téléchargement, l’ID de la piste et la chaîne de paramètres personnalisés fournie par le magasin en ligne lorsqu’il a appelé **DownloadTrack**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins de type 1 en ligne**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




