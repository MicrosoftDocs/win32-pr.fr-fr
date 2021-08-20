---
title: À propos des métadonnées
description: À propos des métadonnées
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Lecteur Windows Media, métadonnées
- métadonnées, à propos de
- métadonnées, attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcccda2af46e60e4bb0733d17e35e1a50d1fe923e9775fa6b10d2c06e3a972a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865359"
---
# <a name="about-the-metadata"></a>À propos des métadonnées

Lecteur Windows Media 10 ou une version ultérieure tente de synchroniser les attributs de métadonnées suivants.



| Attribut Player | WMDM constante globale)  | Description                                                                                                 | Version requise                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| AlbumArtist      | \_wszWMDMAlbumArtist g | **Chaîne** terminée par le caractère NULL contenant le nom de l’artiste principal de l’album.                         | Lecteur Windows Media 11 ou version ultérieure. |
| Album            | \_wszWMDMAlbumTitle g  | **Chaîne** terminée par le caractère null qui contient le titre de l’album sur lequel le contenu a été publié à l’origine.  | Lecteur Windows Media 11 ou version ultérieure. |
| Auteur           | \_wszWMDMAuthor g      | **Chaîne** terminée par le caractère NULL contenant le nom de l’artiste multimédia ou de l’acteur associé au contenu.    | Lecteur Windows Media 11 ou version ultérieure. |
| BuyNow           | \_wszWMDMBuyNow g      | **Valeur booléenne** indiquant si l’utilisateur a choisi d’acheter le contenu.                                 | Lecteur Windows Media 10 ou version ultérieure. |
| WM/genre         | \_wszWMDMGenre g       | **Chaîne** terminée par le caractère null qui contient le genre du contenu.                                             | Lecteur Windows Media 11 ou version ultérieure. |
| UserPlayCount    | \_wszWMDMPlayCount g   | **Valeur DWORD** qui contient le nombre de fois que l’utilisateur a lu le fichier multimédia numérique.                        | Lecteur Windows Media 10 ou version ultérieure. |
| ReleaseDate      | \_wszWMDMYear g        | Date de la version d’origine de l’élément.                                                               | Lecteur Windows Media 11 ou version ultérieure. |
| Titre            | \_wszWMDMTitle g       | **Chaîne** terminée par le caractère null qui contient le titre.                                                            | Lecteur Windows Media 11 ou version ultérieure. |
| WM/TrackNumber   | \_wszWMDMTrack g       | **Valeur DWORD** qui contient le numéro de suivi de l’élément sur l’album sur lequel il a été publié à l’origine.         | Lecteur Windows Media 11 ou version ultérieure. |
| UserRating       | \_wszWMDMUserRating g  | **DWORD** contenant une valeur qui représente l’évaluation de l’étoile spécifiée par l’utilisateur pour le fichier multimédia numérique. | Lecteur Windows Media 10 ou version ultérieure. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extensions d’appareil pour le transfert de métadonnées accéléré**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




