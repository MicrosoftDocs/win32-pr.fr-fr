---
description: Lorsque vous fournissez une miniature, les instructions suivantes doivent être suivies.
title: Instructions du gestionnaire de miniatures
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a1d29992-1347-4574-81b9-b90e2b0938f1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 062c363b4faea9fd07888a55e2dd3896b138c599
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522308"
---
# <a name="thumbnail-handler-guidelines"></a>Instructions du gestionnaire de miniatures

Lorsque vous fournissez une miniature, les instructions suivantes doivent être suivies.

-   Fournissez des miniatures qui s’affichent correctement à une résolution de 256x256 pixels en couleur 32 bits. une miniature de cette taille est utilisée par le volet de lecture Windows Vista en l’absence d’un gestionnaire d’aperçus inscrit. Toutefois, un gestionnaire d’aperçus est l’option recommandée et doit être fourni dans la mesure du possible.
-   Lorsque vous créez plusieurs images de différentes tailles, ne créez pas les images plus petites à partir de la plus grande en rognant la page, le cadre ou l’image. Mettre à l’échelle la totalité de l’image.
-   Ne pas afficher plusieurs pages, images ou images à la fois ; Utilisez simplement un. Si un document se compose de plusieurs pages, telles qu’un document texte ou une feuille de calcul composée de plusieurs feuilles de calcul, la page de couverture est souvent le meilleur choix, mais quel que soit l’usage que vous utilisez, n’en utilisez qu’une seule. Ne pas agréger différentes pages, ce qui donne un aspect encombré.
-   Windows Vista est responsable de la mise à l’échelle des images d’échantillonnage. Si votre gestionnaire est invité à fournir une image plus grande que celle que vous avez disponible, indiquez la taille la plus proche. N’essayez pas de redimensionner dynamiquement votre propre image.
-   Retournez toujours une image miniature de votre gestionnaire au lieu d’effectuer une logique spéciale pour retourner les icônes traditionnelles. en dessous d’une certaine taille, Windows Vista affiche automatiquement une icône traditionnelle à la place de la miniature. Pour plus d’informations, consultez la section *cache des miniatures et dimensionnement* des [gestionnaires de miniatures](thumbnail-providers.md) .
-   Retourne toujours une miniature avec les proportions de la page, du cadre ou de l’image. N’utilisez pas alpha pour terminer un carré. Windows Vista est chargé de positionner correctement une image non carrée.
-   N’ajoutez pas d’ornements à vos miniatures. Windows Vista applique automatiquement des ombres portées et d’autres ornements, le cas échéant. Elle applique également des ornements spéciaux pour des types de fichiers spécifiques, tels que des images ou des vidéos.
-   Ne pas superposer le type de fichier ou les informations sur l’application sur votre miniature. Windows Vista affiche une superposition de type pour vous dans le coin inférieur droit de l’image. Cette superposition est basée sur le type perçu, mais peut être définie pour des types de fichier individuels.
-   Pour de meilleures performances, lorsque votre miniature est basée sur le contenu d’un fichier (par exemple, une page d’un document), stockez l’image d’aperçu lorsque le fichier est enregistré (et donc probablement modifié) au lieu de le calculer en temps réel. Cela doit être fait si le calcul est gourmand en mémoire (plus d’une ou deux secondes). Si ce n’est pas le cas, les vues qui affichent un grand nombre de fichiers dont les miniatures sont gérées par différents gestionnaires vont prendre un certain temps à s’afficher, une expérience utilisateur incorrecte. Windows Vista met en cache les miniatures et fait référence à l’heure de la dernière modification pour déterminer si une miniature doit être mise à jour.
-   N’oubliez pas que l’Explorateur peut choisir de ne pas afficher une miniature, même si un fournisseur est disponible. Par exemple, un fichier qui a été archivé sur bande n’est pas rappelé pour obtenir sa miniature.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestionnaires de miniatures](thumbnail-providers.md)
</dt> <dt>

[Création de gestionnaires de miniatures](building-thumbnail-providers.md)
</dt> </dl>

 

 



