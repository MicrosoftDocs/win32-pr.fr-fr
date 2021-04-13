---
description: Présentation des services de modification DirectShow
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Présentation des services de modification DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481616"
---
# <a name="introduction-to-directshow-editing-services"></a>Présentation des services de modification DirectShow

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Le cœur de DirectShow est une architecture puissante pour gérer le contenu multimédia en continu. Une application peut l’utiliser pour lire du contenu multimédia créé dans un grand nombre de formats, sans que le développeur ait à se soucier de la compression de fichiers et d’autres détails fastidieux. Avant les [services de modification DirectShow](directshow-editing-services.md) , toutefois, DirectShow n’avait pas la flexibilité nécessaire pour la modification non linéaire.

Par exemple, supposons que vous souhaitiez créer une séquence vidéo composée de 4 secondes à partir de la source A, puis de 10 secondes à partir de la source B et se terminant à 5 secondes de la source C. Cela peut être très simple à utiliser uniquement l’API de base DirectShow.

Mais que se passe-vous si vous avez décidé que la source C doit être antérieure à la source B, pas après ; que la séquence doit utiliser 8 secondes de la source A, et non 4 ; et que l’ensemble de la production nécessitait la lecture d’une piste audio distincte en arrière-plan ? Même les modifications mineures, telles que celles-ci, peuvent être difficiles à implémenter. Toutefois, le scénario qui vient d’être décrit est un projet de modification trivial dans DES. vous pouvez le faire avec quelques appels de méthode.

Voici quelques-unes des fonctionnalités offertes par DirectShow :

-   Modèle de chronologie qui organise les pistes audio et vidéo en couches imbriquées, ce qui facilite la manipulation de la production finale
-   La possibilité d’afficher un aperçu d’un projet vidéo à la volée
-   Persistance de projet via un format XML
-   Prise en charge des effets audio et vidéo, ainsi que des transitions entre les pistes vidéo (comme les fondus et les effaces)
-   Plus de 100 réinitialisations standard, telles que définies par la société des ingénieurs d’images animées et de télévision (SMPTE)
-   Incrustation basée sur la teinte, la luminance, la valeur RVB ou la valeur alpha
-   Conversion automatique des fréquences d’images et des taux d’échantillonnage audio, ce qui permet à une production d’utiliser des sources hétérogènes
-   Redimensionnement ou rognage de la vidéo

Limites :

-   DES ne prend pas en charge les sources vidéo MPEG-2 ou H. 264.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Services d’édition DirectShow](directshow-editing-services.md)
</dt> </dl>

 

 



