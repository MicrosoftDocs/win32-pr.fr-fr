---
description: Cette section décrit comment utiliser l’API de transcodage pour recoder des fichiers multimédias. L’API de transcodage a été introduite dans Windows 7.
ms.assetid: 24bf68a8-39bf-4302-b28c-71bb23b63469
title: API de transcodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9783c6f99a25ba6835171dcc7f7555a1f747c72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863942"
---
# <a name="transcode-api"></a>API de transcodage

Cette section décrit comment utiliser l’API de transcodage pour recoder des fichiers multimédias. L’API de transcodage a été introduite dans Windows 7.

Le *transcodage* est la conversion d’un fichier multimédia numérique d’un format à un autre. L’API de transcodage est conçue pour être utilisée avec la [session multimédia](media-session.md). Il simplifie l’utilisation de la session multimédia pour certains types d’applications de transcodage :

-   Encodage à vitesse de transmission constante (CBR), où la vitesse de transmission cible est connue à l’avance.
-   Au plus un flux audio et un flux vidéo.
-   Encodage à partir de et vers un fichier.

L’API de transcodage ne prend pas en charge les éléments suivants :

-   Débit binaire variable (VBR) ou encodage à plusieurs passes.
-   Plusieurs flux audio ou plusieurs flux vidéo.
-   Contenu protégé par DRM autre que les fichiers ASF protégés par WMDRM.
-   La diffusion en continu en direct, telle que la diffusion en continu en direct ou en direct.

Si votre application d’encodage respecte ces contraintes, l’API de transcodage est un modèle de programmation plus simple que l’utilisation de la session de média seule.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                          | Description                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos de l’API de transcodage](about-the-transcode-api.md)<br/>                              | Fournit une vue d’ensemble générale de l’API de transcodage.<br/>                                                                                                                                                                |
| [Utilisation de l’API de transcodage](fast-transcode-objects.md)<br/>                               | Décrit comment une application utilise l’API de transcodage.<br/>                                                                                                                                                             |
| [Didacticiel : encodage d’un fichier MP4](tutorial--encoding-an-mp4-file-.md)<br/>               | Didacticiel pas à pas qui montre comment utiliser l’API de transcodage pour encoder un fichier MP4.<br/>                                                                                                                           |
| [Didacticiel : encodage d’un fichier WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md)<br/> | Montre comment utiliser l’API de transcodage pour encoder un fichier WMA. Ce didacticiel modifie le code affiché dans le [Didacticiel : codage d’un fichier MP4](tutorial--encoding-an-mp4-file-.md). vous devez d’abord lire ce didacticiel.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Codage et création de fichier](encoding-and-file-authoring.md)
</dt> <dt>

[Media Foundation : notions essentielles](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Vue d’ensemble de l’encodage dans Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 




