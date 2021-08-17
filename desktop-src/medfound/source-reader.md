---
description: Le lecteur source est une alternative à l’utilisation de la session de média et du pipeline Microsoft Media Foundation pour traiter les données multimédias.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Lecteur source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81527392c97aae039de8b8cdbd76b1251e03842b6b66c22cc224118d4f428620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101811"
---
# <a name="source-reader"></a>Lecteur source

Le lecteur source est une alternative à l’utilisation de la [session de média](media-session.md) et du pipeline Microsoft Media Foundation pour traiter les données multimédias.

## <a name="why-use-the-source-reader"></a>Pourquoi utiliser le lecteur source ?

Media Foundation fournit un pipeline optimisé pour la lecture. Le pipeline est de bout en bout, ce qui signifie qu’il gère le workflow de la source (par exemple, un fichier vidéo) jusqu’à la destination (telle que l’affichage graphique). Toutefois, si vous souhaitez lire ou modifier les données au fur et à mesure de leur passage dans le pipeline, vous devez écrire un plug-in personnalisé. Cela nécessite une connaissance assez profonde du pipeline Media Foundation. Pour certaines tâches, la création d’un nouveau plug-in est trop importante. Le lecteur source est conçu pour ce type de situation, lorsque vous souhaitez obtenir les données brutes d’une source sans la surcharge de l’ensemble du pipeline.

En interne, le lecteur source contient un pointeur vers une source de média. Une *source de média* est un objet Media Foundation qui génère des données multimédias à partir d’une source externe, telle qu’un fichier multimédia ou un périphérique de capture vidéo. Le lecteur source gère tous les appels de méthode à la source du média. (Pour plus d’informations sur les sources multimédias, consultez [sources multimédias](media-sources.md).)

Si la source du média fournit des données compressées, vous pouvez utiliser le lecteur source pour décoder les données. Dans ce cas, le lecteur source chargera le décodeur approprié et gérera le workflow entre la source du média et le décodeur. Le lecteur source peut également effectuer un traitement vidéo limité : conversion des couleurs YUV en RVB-32 et désentrelacement de logiciels, bien que ces opérations ne soient pas recommandées pour le rendu vidéo en temps réel. L’illustration suivante montre ce processus.

![diagramme du lecteur source](images/sourcereader.png)

Le lecteur source n’envoie pas les données à une destination ; C’est à l’application d’utiliser les données. Par exemple, le lecteur source peut lire un fichier vidéo, mais il n’affiche pas la vidéo à l’écran. En outre, le lecteur source ne gère pas une horloge de présentation, ne gère pas les problèmes de minutage ou ne synchronise pas les vidéos avec l’audio.

Envisagez d’utiliser le lecteur source dans les cas suivants :

-   Vous souhaitez obtenir des données à partir d’un fichier multimédia sans vous soucier de la structure de fichiers sous-jacente.
-   Vous souhaitez obtenir des données à partir d’un périphérique de capture audio ou vidéo.
-   Vos tâches de traitement de données ne sont pas sensibles au temps ou vous n’avez pas besoin d’une horloge de présentation.
-   Vous avez déjà un pipeline multimédia qui n’est pas basé sur Media Foundation et vous souhaitez incorporer les sources de média Media Foundation dans votre propre Pipeline.

Le lecteur source n’est pas recommandé dans les cas suivants :

-   Pour le contenu protégé. Le lecteur source ne prend pas en charge la gestion des droits numériques (DRM).
-   Si vous vous souciez des détails de la structure de fichier sous-jacente. Le lecteur source masque ce type de détail.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                        | Description                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Utilisation du lecteur source pour traiter les données multimédias](processing-media-data-with-the-source-reader.md)<br/> | Cette rubrique explique comment utiliser le lecteur source pour traiter les données multimédias.<br/>                                               |
| [Utilisation du lecteur source en mode asynchrone](using-the-source-reader-in-asynchronous-mode.md)<br/>  | Cette rubrique explique comment utiliser le lecteur source en mode asynchrone.<br/>                                                |
| [Didacticiel : décodage de l’audio](tutorial--decoding-audio.md)<br/>                                          | Ce didacticiel montre comment utiliser le lecteur source pour décoder l’audio d’un fichier multimédia et écrire l’audio dans un fichier WAVE.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Architecture Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Guide de programmation Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




