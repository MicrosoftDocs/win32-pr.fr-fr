---
title: attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media Format 11)
description: en savoir plus sur les attributs avec plusieurs valeurs dans le kit de développement logiciel (SDK) Windows Media Format 11. Certains attributs d’éléments multimédias peuvent avoir plusieurs valeurs.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, valeurs multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e87ff070b4714d7d9bc7eb5fcc7728bc4c39bc964a14d8545eff2023967a6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709489"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>attributs avec plusieurs valeurs (kit de développement logiciel (SDK) Windows Media Format 11)

Plusieurs valeurs peuvent être assignées à certains des attributs prédéfinis. Par exemple, **Artist** est un attribut qui peut avoir plusieurs valeurs. Vous pouvez appeler [**IWMHeaderInfo3 :: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) plusieurs fois pour ajouter autant de valeurs d' **artistes** que nécessaire. Si vous effectuez plusieurs appels à **AddAttribute** pour les attributs qui ne prennent pas en charge plusieurs valeurs, la méthode peut retourner un code d’erreur ou ignorer simplement votre demande.

Le tableau suivant répertorie les attributs qui prennent en charge plusieurs valeurs. Certains attributs peuvent avoir plusieurs valeurs uniquement dans des fichiers ASF, tandis que d’autres peuvent avoir plusieurs valeurs dans des fichiers ASF et MP3.



| Attribut                                                 | Prise en charge de plusieurs valeurs |
|-----------------------------------------------------------|-----------------------------|
| [**Auteur**](author.md)                                  | ASF, MP3                    |
| [**WM/AlbumArtist**](wm-albumartist.md)                  | ASF                         |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)              | ASF                         |
| [**WM/Category**](wm-category.md)                        | ASF                         |
| [**WM/Composer**](wm-composer.md)                        | ASF, MP3                    |
| [**WM/conducteur**](wm-conductor.md)                      | ASF                         |
| [**WM/Director**](wm-director.md)                        | ASF                         |
| [**WM/genre**](wm-genre.md)                              | ASF                         |
| [**WM/GenreID**](wm-genreid.md)                          | ASF                         |
| [**WM/langage**](wm-language.md)                        | ASF, MP3                    |
| [**Synchronisation des WM et des paroles \_**](wm-lyrics-synchronised.md) | ASF, MP3                    |
| [**WM/humeur**](wm-mood.md)                                | ASF, MP3                    |
| [**WM/image**](wmpicture.md)                           | ASF, MP3                    |
| [**WM/Producer**](wm-producer.md)                        | ASF                         |
| [**WM/PromotionURL**](wm-promotionurl.md)                | ASF                         |
| [**WM/UserWebURL**](wm-userweburl.md)                    | ASF, MP3                    |
| [**WM/Writer**](wm-writer.md)                            | ASF, MP3                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs**](attributes.md)
</dt> </dl>

 

 




