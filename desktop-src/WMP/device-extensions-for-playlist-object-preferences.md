---
title: Extensions d’appareil pour les préférences de l’objet playlist
description: Extensions d’appareil pour les préférences de l’objet playlist
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Windows Media Player, extensions d’appareils
- Windows Media Player, extensions
- Lecteur Windows Media, préférences de l’objet playlist
- extensions d’appareil, préférences de l’objet playlist
- extensions, préférences de l’objet playlist
- Objet playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fd9c6301e33307fc49e50b8aa9042752e020e32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674689"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>Extensions d’appareil pour les préférences de l’objet playlist

Dans le cadre du processus de synchronisation, le lecteur Windows Media 10 ou version ultérieure copie les objets de sélection sur des appareils mobiles compatibles MTP. Le lecteur Windows Media 11 introduit une nouvelle fonctionnalité qui permet aux appareils portables de limiter les types d’objets de sélection copiés. (Le lecteur Windows Media synchronise toujours le contenu de la sélection comme spécifié par les règles de synchronisation. Cette fonctionnalité affecte uniquement la synchronisation des objets de sélection.) Le lecteur Windows Media copie trois types d’objets de sélection de l’ordinateur à l’appareil :

-   **Sélections ordinaires.** Il s’agit de sélections visibles dans la fonctionnalité **bibliothèque** du lecteur Windows Media. Il s’agit notamment des sélections créées par l’utilisateur, des sélections ajoutées à la bibliothèque par des magasins en ligne et des exemples de sélection installés avec le lecteur. Le lecteur Windows Media copie uniquement ces playlists sur l’appareil lorsque l’utilisateur les a sélectionnées pour la synchronisation.
-   **Sélections de la synchronisation des stocks.** Il s’agit de sélections spéciales qui sont installées avec le lecteur Windows Media et utilisées uniquement pour la synchronisation. Ces sélections sont visibles uniquement dans l’Assistant Installation des périphériques du lecteur Windows Media.
-   **Sélections implicitement créées.** Ces sélections sont créées lorsque l’utilisateur fait glisser et dépose un dossier de catégorie, tel qu’un **artiste** ou un **album**, dans le volet qui répertorie les éléments à synchroniser.

Le fichier d’en-tête nommé wmpdevices. h, qui a été mis à jour pour cette version, définit les structures et les constantes nécessaires à la prise en charge des extensions de périphérique du lecteur Windows Media.

Pour qu’un appareil soit reconnu comme prenant en charge les préférences de l’objet de sélection par le biais de l’extension de périphérique MTP du lecteur Windows Media, il doit inclure les informations suivantes dans le jeu de données DeviceInfo. (Pour plus d’informations sur ce jeu de données, consultez la section 4.6.1 de la spécification MTP.)



| Champ de DataSet          | Ordre des champs | Type de données  | Valeur                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Chaîne** | « microsoft.com/WMPPD : 11,0 » |



 

Le tableau suivant fournit des détails sur l’opération MTP pour les préférences de l’objet playlist.



| Élément                  | Description                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Code d’opération        | 0x9203                                                                                                                                                                                                                                                                                          |
| Paramètre d’opération 1 | 0                                                                                                                                                                                                                                                                                               |
| Paramètre d’opération 2 | 0                                                                                                                                                                                                                                                                                               |
| Paramètre d’opération 3 | 0                                                                                                                                                                                                                                                                                               |
| Paramètre d’opération 4 | 0                                                                                                                                                                                                                                                                                               |
| Paramètre d’opération 5 | 0                                                                                                                                                                                                                                                                                               |
| Données                  | L’appareil retourne une valeur dans le paramètre de réponse 1 pour indiquer la préférence de synchronisation de l’objet de sélection.                                                                                                                                                                                      |
| Direction des données        | R->I                                                                                                                                                                                                                                                                                         |
| Options de code de réponse | \_Réponse MTP \_ OK (0x2001) ou code de réponse d’erreur valide.                                                                                                                                                                                                                                        |
| Paramètre de réponse 1  | 0 ou 1. La valeur 0 indique que le lecteur Windows Media ne doit synchroniser que les objets de sélection ordinaires. La valeur 1 indique que le lecteur Windows Media doit synchroniser les objets de sélection ordinaires, les actions et les objets de sélection de synchronisation créés implicitement, ce qui constitue le comportement par défaut. |
| Paramètre de réponse 2  | 0                                                                                                                                                                                                                                                                                               |
| Paramètre de réponse 3  | 0                                                                                                                                                                                                                                                                                               |
| Paramètre de réponse 4  | 0                                                                                                                                                                                                                                                                                               |
| Paramètre de réponse 5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Notes

L’implémentation de cette fonctionnalité est facultative pour les périphériques portables. Le lecteur Windows Media synchronise les objets de sélection ordinaires, les objets de sélection stock Sync et les objets de sélection créés implicitement par défaut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




