---
title: Catalogue musical
description: Catalogue musical
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player Online stores, catalogues musicaux
- magasins en ligne, catalogues musicaux
- tapez 1 magasins en ligne, catalogues musicaux
- Magasins en ligne du lecteur Windows Media, compilateur de catalogue
- magasins en ligne, compilateur de catalogue
- magasins en ligne de type 1, compilateur de catalogue
- catalogues musicaux
- compilateur de catalogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030774"
---
# <a name="music-catalog"></a>Catalogue musical

Un magasin en ligne de type 1 crée son catalogue musical sous la forme d’un ensemble de fichiers TSV (valeurs séparées par des tabulations). Ensuite, le magasin en ligne utilise le [compilateur de catalogue](catalog-compiler-for-type-1-online-stores.md) de Microsoft pour compiler les fichiers TSV dans un catalogue compressé qui peut être téléchargé par le lecteur Windows Media. Le lecteur Windows Media peut télécharger des fichiers de catalogue complets ou des fichiers de mise à jour de catalogue. Les mises à jour du catalogue contiennent uniquement les informations du catalogue qui ont été modifiées depuis la dernière mise à jour du catalogue. Il revient au plug-in de partenaire de contenu de déterminer s’il faut télécharger un catalogue complet ou une mise à jour. Dans les deux cas, le lecteur Windows Media applique les modifications au catalogue en cours lors de la notification du plug-in.

Si un nouveau catalogue est préparé pour le magasin en ligne, le plug-in peut notifier le lecteur en appelant [IWMPContentPartnerCallback :: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) et en passant wmpcnNewCatalogAvailable comme valeur pour le paramètre de *type* .

Lorsque le lecteur Windows Media est prêt à télécharger un catalogue ou une mise à jour, le lecteur appelle [IWMPContentPartner :: GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl). Cette méthode fournit le plug-in contenant des informations sur le catalogue actuel, telles que la version du catalogue et l’identificateur des paramètres régionaux. Le plug-in répond en fournissant l’URL (Uniform Resource Locator) du catalogue complet correct ou de la mise à jour, ainsi qu’un numéro de version et une date d’expiration mis à jour. Le lecteur Windows Media demande périodiquement des mises à jour du catalogue en fonction des informations fournies par le plug-in dans **GetCatalogURL**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> <dt>

[**Compilateur de catalogue pour les magasins en ligne de type 1**](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[**Interface IWMPContentPartner**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




