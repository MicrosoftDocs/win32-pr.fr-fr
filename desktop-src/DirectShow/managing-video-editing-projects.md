---
description: Gestion des projets de montage vidéo
ms.assetid: f8d74807-562f-429b-93a1-e65d0f15163b
title: Gestion des projets de montage vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491cfcb9a6e94874d2cae43567b61666bbd43cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516543"
---
# <a name="managing-video-editing-projects"></a>Gestion des projets de montage vidéo

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Les conseils suivants vous aideront à gérer les projets dans les [services de modification DirectShow](directshow-editing-services.md).

Modifications apportées à la chronologie

-   Si vous modifiez la chronologie après avoir généré le graphique de filtre, appelez [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) à nouveau pour reconstruire le serveur frontal. En règle générale, cela n’affecte pas le reste du graphique. Toutefois, le moteur de rendu doit parfois supprimer l’intégralité du graphique avant de regénérer le serveur frontal. (Cela se produit, par exemple, si vous ajoutez ou supprimez un groupe.) La méthode **ConnectFrontEnd** retourne S \_ WARN \_ OUTPUTRESET pour signaler qu’il a supprimé le graphique. Dans ce cas, votre application doit reconstruire la section de rendu du graphique.
-   Pour supprimer complètement tous les objets de la chronologie, appelez la méthode [**IAMTimeline :: ClearAllGroups**](iamtimeline-clearallgroups.md) .

**Nettoyage**

-   Lorsque vous avez terminé d’utiliser un moteur de rendu, appelez la méthode [**IRenderEngine :: ScrapIt**](irenderengine-scrapit.md) . Comme pour tout objet COM, veillez à libérer chaque pointeur d’interface lorsque vous avez fini de l’utiliser.
-   Le moteur de rendu ne conserve pas un décompte de références sur la chronologie. Ne libérez pas la chronologie avant de l’utiliser, et appelez toujours **ScrapIt** sur le moteur de rendu en premier.
-   Si vous publiez toutes les références à une chronologie, n’utilisez pas les objets de cette chronologie, même si vous y avez des décomptes de références.

**Plusieurs instances de chronologie**

-   Ne déplacez pas les objets Timeline entre les chronologies. Chaque objet d’une chronologie doit être créé par cette chronologie. La chronologie contient un cache interne avec des informations sur les objets qu’il crée ; le déplacement d’objets de chronologie peut perturber le cache.
-   N’utilisez jamais la même instance d’un moteur de rendu avec plusieurs chronologies. Le moteur de rendu contient un cache contenant des informations sur la chronologie. Plusieurs chronologies interrompent le cache et entraînent des résultats imprévisibles. Si vous avez besoin de deux chronologies actives, créez des instances distinctes des moteurs de rendu pour chaque chronologie.
-   Une chronologie peut utiliser plusieurs moteurs de rendu, mais pas en même temps. Supprimez l’ancien moteur de rendu avant d’utiliser un autre moteur de rendu. (C’est généralement le cas lorsque vous passez de l’utilisation du moteur de rendu de base à la version préliminaire au moteur de rendu intelligent pour l’écriture de fichiers.)

**Persistance**

-   Le graphique de filtre n’est pas persistant lorsque vous enregistrez le projet dans un fichier XML. Par conséquent, vous perdez toutes les informations relatives à la recompression intelligente, au format de compression ou aux paramètres de compression. Il revient à l’application de restaurer ces paramètres après le chargement d’un projet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des services de modification DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



