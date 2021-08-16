---
title: Extensions d’appareil pour les préférences de l’objet playlist
description: Extensions d’appareil pour les préférences de l’objet playlist
ms.assetid: 33b3dd18-fda2-4bf9-a893-5d77cdde6b80
keywords:
- Lecteur Windows Media, extensions de périphérique
- Lecteur Windows Media, extensions
- Lecteur Windows Media, préférences de l’objet Playlist
- extensions d’appareil, préférences de l’objet playlist
- extensions, préférences de l’objet playlist
- Objet playlist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f2acb01de41b753a85fee1c69e0bf015c687da04f50a10531ee5c67b0a13cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340918"
---
# <a name="device-extensions-for-playlist-object-preferences"></a>Extensions d’appareil pour les préférences de l’objet playlist

dans le cadre du processus de synchronisation, Lecteur Windows Media 10 ou version ultérieure copie les objets de sélection sur les appareils mobiles compatibles MTP. Lecteur Windows Media 11 introduit une nouvelle fonctionnalité qui permet aux appareils portables de limiter les types d’objets de sélection copiés. (Lecteur Windows Media synchronise toujours le contenu de la sélection comme spécifié par les règles de synchronisation. Cette fonctionnalité affecte uniquement la synchronisation des objets de sélection.) Lecteur Windows Media copie trois types d’objets de sélection de l’ordinateur vers l’appareil :

-   **Sélections ordinaires.** il s’agit de sélections visibles dans la fonctionnalité de **bibliothèque** de Lecteur Windows Media. Il s’agit notamment des sélections créées par l’utilisateur, des sélections ajoutées à la bibliothèque par des magasins en ligne et des exemples de sélection installés avec le lecteur. Lecteur Windows Media copie uniquement ces playlists sur l’appareil lorsque l’utilisateur les a sélectionnées pour la synchronisation.
-   **Sélections de la synchronisation des stocks.** il s’agit de sélections spéciales qui sont installées avec Lecteur Windows Media et utilisées uniquement pour la synchronisation. ces sélections sont visibles uniquement dans l’assistant installation de l’appareil Lecteur Windows Media.
-   **Sélections implicitement créées.** Ces sélections sont créées lorsque l’utilisateur fait glisser et dépose un dossier de catégorie, tel qu’un **artiste** ou un **album**, dans le volet qui répertorie les éléments à synchroniser.

le fichier d’en-tête nommé wmpdevices. h, qui a été mis à jour pour cette version, définit les structures et les constantes nécessaires à la prise en charge des extensions d’appareils Lecteur Windows Media.

pour qu’un appareil soit reconnu comme prenant en charge les préférences de l’objet de sélection par le biais du jeu d’extensions de périphérique MTP Lecteur Windows Media, il doit inclure les informations suivantes dans le jeu de données DeviceInfo. (Pour plus d’informations sur ce jeu de données, consultez la section 4.6.1 de la spécification MTP.)



| Champ de DataSet          | Ordre des champs | Type de données  | Valeur                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Chaîne** | « microsoft.com/WMPPD : 11,0 » |



 

Le tableau suivant fournit des détails sur l’opération MTP pour les préférences de l’objet playlist.



| Élément                  | Description                                                                                                                                                                                                                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Code d'opération        | 0x9203                                                                                                                                                                                                                                                                                          |
| Paramètre d’opération 1 | 0                                                                                                                                                                                                                                                                                               |
| Paramètre d’opération 2 | 0                                                                                                                                                                                                                                                                                               |
| Paramètre d’opération 3 | 0                                                                                                                                                                                                                                                                                               |
| Paramètre d’opération 4 | 0                                                                                                                                                                                                                                                                                               |
| Paramètre d’opération 5 | 0                                                                                                                                                                                                                                                                                               |
| Données                  | L’appareil retourne une valeur dans le paramètre de réponse 1 pour indiquer la préférence de synchronisation de l’objet de sélection.                                                                                                                                                                                      |
| Direction des données        | R->I                                                                                                                                                                                                                                                                                         |
| Options de code de réponse | \_Réponse MTP \_ OK (0x2001) ou code de réponse d’erreur valide.                                                                                                                                                                                                                                        |
| Paramètre de réponse 1  | 0 ou 1. la valeur 0 indique que Lecteur Windows Media doit synchroniser uniquement les objets de sélection ordinaires. la valeur 1 indique que les Lecteur Windows Media doivent synchroniser les objets de sélection ordinaires, les actions et les objets de sélection de synchronisation créés implicitement, ce qui constitue le comportement par défaut. |
| Paramètre de réponse 2  | 0                                                                                                                                                                                                                                                                                               |
| Paramètre de réponse 3  | 0                                                                                                                                                                                                                                                                                               |
| Paramètre de réponse 4  | 0                                                                                                                                                                                                                                                                                               |
| Paramètre de réponse 5  | 0                                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Remarques

L’implémentation de cette fonctionnalité est facultative pour les périphériques portables. Lecteur Windows Media synchronise les objets de sélection ordinaires, les objets de sélection de synchronisation de stock et les objets de sélection créés implicitement par défaut.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




