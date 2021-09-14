---
description: Définition des propriétés sur les sources
ms.assetid: fa1c7c40-915b-4577-aa33-6bd06707d93a
title: Définition des propriétés sur les sources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de58e25cc9fdec34ed285ebbfc2e9cfd3dcdf95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999578"
---
# <a name="setting-properties-on-sources"></a>Définition des propriétés sur les sources

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Lorsque vous créez un nouvel objet source, vous devez définir quelques propriétés et d’autres que vous pouvez éventuellement définir. Vous devez définir les propriétés suivantes.

-   Heures de début et de fin, par rapport au reste de la chronologie. Appelez la méthode [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md) . Ne définissez pas les heures qui se chevauchent sur les objets sources au sein d’une même piste, sans quoi cela entraînera un comportement indéfini.
-   Fichier multimédia à utiliser comme clip source. Appelez [**IAMTimelineSrc :: SetMediaName**](iamtimelinesrc-setmedianame.md).
-   Heures de début et de fin du média, par rapport au fichier source d’origine. Appelez la méthode [**IAMTimelineSrc :: SetMediaTimes**](iamtimelinesrc-setmediatimes.md) . Exception : si la source est une image continue, ne spécifiez pas les heures de support. pour plus d’informations sur les temps de support, consultez [l’heure dans DirectShow Services d’édition](time-in-directshow-editing-services.md).

Un objet source hérite son type de média du groupe parent. il n’est donc pas nécessaire de spécifier un type de média.

Les propriétés facultatives sont les suivantes :

-   Mode Stretch. le mode stretch spécifie la manière dont Microsoft® DirectShow les Services de modification® (DES) génèrent une source dont la taille ne correspond pas aux dimensions de sortie. Par défaut, DES étire une image sans conserver les proportions. Ou bien, les peuvent rogner une image ou créer DES bandes. Appelez la méthode [**IAMTimelineSrc :: SetStretchMode**](iamtimelinesrc-setstretchmode.md) pour spécifier le mode Stretch.
-   Durée du fichier source. Si vous définissez cette propriété avant de définir les heures de support, l’algorithme DES valide l’heure d’arrêt du support et tronque l’heure d’arrêt si elle dépasse la durée du fichier. Cela peut aider à éviter les erreurs de rendu ultérieurement. Vous pouvez obtenir la durée du fichier à l’aide du détecteur de média, comme décrit dans [utilisation du détecteur de média](using-the-media-detector.md). Appelez la méthode [**IAMTimelineSrc :: SetMediaLength**](iamtimelinesrc-setmedialength.md) pour spécifier la durée du fichier.
-   Numéro du flux. Par défaut, un objet source utilise le premier flux du fichier qui correspond au type de média du groupe parent. Si un fichier contient au moins deux flux du même type de média, sélectionnez le flux à utiliser en appelant [**IAMTimelineSrc :: SetStreamNumber**](iamtimelinesrc-setstreamnumber.md). Vous pouvez utiliser le détecteur de média pour rechercher le nombre de flux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des sources](working-with-sources.md)
</dt> </dl>

 

 



