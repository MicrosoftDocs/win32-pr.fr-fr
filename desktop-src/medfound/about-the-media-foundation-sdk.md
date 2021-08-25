---
description: Microsoft Media Foundation est la plateforme multimédia de nouvelle génération pour Windows qui permet aux développeurs, aux consommateurs et aux fournisseurs de contenu d’adopter la nouvelle vague de contenus premium avec une robustesse améliorée, une qualité inégalée et une interopérabilité transparente.
ms.assetid: 3f933e39-8f9b-4c62-b528-4f1bba4b45d1
title: À propos de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2f8510cc6d967f7a3a809d395f032e277290074002399f9b54e6c54025c312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959649"
---
# <a name="about-media-foundation"></a>À propos de Media Foundation

Microsoft Media Foundation est la plateforme multimédia de nouvelle génération pour Windows qui permet aux développeurs, aux consommateurs et aux fournisseurs de contenu d’adopter la nouvelle vague de contenus premium avec une robustesse améliorée, une qualité inégalée et une interopérabilité transparente.

Media Foundation nécessite Windows Vista ou version ultérieure. Elle utilise le modèle COM (Component Object Model) et requiert C/C++. Microsoft ne fournit pas d’API gérée pour Media Foundation.

les api Media Foundation font partie du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx). pour développer une application Media Foundation, installez la version la plus récente du SDK Windows.

## <a name="audio-and-video-quality"></a>Qualité audio et vidéo

Media Foundation a été conçu pour répondre aux défis posés par le contenu haute définition. Les améliorations apportées à la qualité audio et vidéo dans l’ensemble de la plate-forme vous permettent désormais de bénéficier d’une expérience remarquable pour le contenu haute définition de la prochaine génération.

-   DirectX Video Acceleration (DXVA) 2,0 offre une accélération vidéo plus efficace, par rapport à DXVA 1,0, avec un décodage vidéo plus robuste et rationalisé et une utilisation étendue du matériel dans le traitement vidéo. avec DXVA 2,0, Windows pouvez gérer certains des contenus haute définition les plus exigeants, avec une haute qualité et une meilleure résilience des problèmes.

-   Les informations sur l’espace colorimétrique sont conservées dans l’ensemble du pipeline vidéo. Les utilisateurs peuvent profiter d’un contenu vidéo avec une fidélité complète. Les informations de couleur et les images entrelacées sont désormais transmises au matériel pour les compositions à passage unique. La préservation des informations sur l’espace colorimétrique réduit également les conversions d’espace colorimétrique inutiles, ce qui libère davantage de cycles pour traiter le contenu HD exigeant.
-   Le convertisseur vidéo amélioré (EVR) offre une meilleure prise en charge de la synchronisation, un traitement vidéo amélioré et une meilleure résilience des problèmes. La prise en charge de la lecture plein écran a été améliorée et la suppression de vidéo en mode fenêtre a été réduite.
-   Media Foundation utilise le service planificateur de classes multimédias (MMCSS), un nouveau service système dans Windows Vista. MMCSS permet aux applications multimédias de s’assurer que leur traitement qui respecte le temps reçoit un accès prioritaire aux ressources du processeur.

## <a name="content-access"></a>Accès au contenu

Étant donné que le divertissement numérique passe dans l’ère haute définition et que le contenu devient plus portable et omniprésent, la protection du contenu devient partie intégrante des produits multimédias numériques. L’extensibilité de Media Foundation s’assure qu’elle peut prendre en charge ces tendances.

En outre, Media Foundation extensibilité permet à différents systèmes de protection de contenu de fonctionner ensemble.

## <a name="about-media-foundation"></a>À propos de Media Foundation

Cette section contient des informations générales sur les API Media Foundation. Vous trouverez des informations de programmation détaillées dans le [Guide de programmation Media Foundation](media-foundation-programming-guide.md).



| Section                                                                              | Description                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Nouveautés de Media Foundation](whats-new-for-media-foundation.md)                | Décrit les nouvelles fonctionnalités de Media Foundation.                               |
| [Media Foundation en-têtes et bibliothèques](media-foundation-headers-and-libraries.md) | Répertorie les fichiers d’en-tête et de bibliothèque qui définissent les API Media Foundation. |
| [Outils de Media Foundation](media-foundation-tools.md)                                 | Décrit les outils de développement disponibles pour Media Foundation.  |



 

Media Foundation n’est pas inclus avec les éditions N et KN de Windows 8. pour plus d’informations, consultez [Microsoft Windows Media feature Pack pour les Versions N et KN de toutes les éditions de Windows 8](https://support.microsoft.com/kb/2703761).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Microsoft Media Foundation](microsoft-media-foundation-sdk.md)
</dt> </dl>

 

 



