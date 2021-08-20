---
description: Horodatages
ms.assetid: 445fe6b9-9d5b-45fd-9c9e-8c632c5228ae
title: Horodatages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed14f0155a0bfbf209719f4aff97cbbd19501e6aa32d57e9f0c1cbb2df0964b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072313"
---
# <a name="time-stamps"></a>Horodatages

L' *horodatage* définit les heures de début et de fin d’un échantillon de support, mesurée en temps de flux. L’horodatage est parfois appelé heure de *Présentation*. Lorsque vous lisez le reste de cet article, il est important de se souvenir que tous les formats n’utilisent pas les horodatages de la même façon. Par exemple, tous les exemples MPEG ne sont pas horodatés. Dans les graphiques de filtre MPEG, l’horodatage n’est pas appliqué à chaque frame tant qu’il n’est pas sorti du décodeur.

Lorsqu’un filtre de convertisseur reçoit un exemple, il planifie le rendu en fonction de l’horodatage. Si l’exemple arrive en retard ou n’a pas d’horodatage, le filtre restitue l’exemple immédiatement. Dans le cas contraire, le filtre attend l’heure de début de l’exemple avant d’afficher l’exemple. (Elle attend l’heure de début en appelant la méthode [**IReferenceClock :: AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) .)

Les filtres sources et les filtres de l’analyseur sont chargés de définir les horodatages corrects sur les exemples qu’ils traitent. Suivez les instructions ci-dessous.

-   Lecture de fichier : le premier exemple est horodaté avec une heure de début égale à zéro. Les horodatages suivants sont déterminés par la longueur de l’échantillon et la vitesse de lecture, qui est elle-même déterminée par le format de fichier. Le filtre qui analyse le fichier est chargé de calculer les horodatages appropriés (par exemple, le [séparateur AVI](avi-splitter-filter.md)).
-   Capture vidéo et audio : chaque exemple est horodaté avec une heure de début égale à la durée du flux de données lors de la capture, avec les restrictions suivantes :
    -   Les images vidéo d’un code confidentiel d’aperçu (par opposition à un code confidentiel de capture) ne sont pas horodatées. En raison de la latence de graphique, une image vidéo qui est marquée avec le temps de capture est toujours retardée au niveau du convertisseur vidéo. Cela peut amener le convertisseur à déposer des frames, en tentant de contrôler la qualité. Pour plus d’informations sur le contrôle qualité, consultez [gestion du contrôle qualité](quality-control-management.md).
    -   Capture audio : le filtre de capture audio utilise son propre ensemble de mémoires tampons, qui sont différentes de celles utilisées par le pilote audio. Le pilote audio remplit les tampons du filtre de capture à intervalles fixes. L’intervalle dépend du pilote, mais n’est généralement pas supérieur à 10 millisecondes. Les horodatages des échantillons audio reflètent l’heure à laquelle le pilote a rempli les tampons du filtre de capture audio. Ces heures peuvent être légèrement inexactes, en particulier si l’application utilise une très petite taille de mémoire tampon. Toutefois, les temps de support reflètent avec précision le nombre d’échantillons audio dans la mémoire tampon.
-   Filtres Mux : selon le format de sortie, un filtre MUX peut avoir besoin de générer des horodatages, ou ce n’est peut-être pas le cas. Par exemple, le format de fichier AVI utilise une fréquence d’images fixe sans horodatage. le filtre [multiplex MUX](avi-mux-filter.md) suppose donc que les échantillons arrivent à peu près au bon moment. Toutefois, si les horodatages entrants indiquent un intervalle supérieur à un cadre, le multiplexeur de contrôle d’accès (AVI) enregistre une entrée d’index avec la taille zéro pour indiquer un frame déplacé. Lors de la lecture du fichier, de nouveaux horodatages sont générés au moment de l’exécution, comme décrit précédemment.

Pour définir l’horodatage sur un exemple, appelez la méthode [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .

**Temps de support**

Le cas échéant, le filtre peut également spécifier un *temps de support* pour l’exemple. Dans un flux vidéo, l’heure du média représente le numéro de la trame. Dans un flux audio, l’heure du média représente le numéro de l’échantillon dans le paquet. Par exemple, si chaque paquet contient une seconde de l’audio 44,1 kilohertz (kHz), le premier paquet a une heure de début de support de zéro et une heure d’arrêt de support de 44100. Dans un flux de recherche, l’heure du média est toujours relative à l’heure de début du flux. Supposons, par exemple, que vous recherchez 2 secondes à partir du début d’un flux vidéo de 15 i/s. Le premier exemple de support après la recherche a un horodatage de zéro, mais un temps de support de 30.

Les filtres de convertisseur et de multiplexeur peuvent utiliser l’heure du média pour déterminer si des images ou des échantillons ont été supprimés, en vérifiant les lacunes. Toutefois, les filtres ne sont pas requis pour définir l’heure du support. Pour définir l’heure du média sur un exemple, appelez la méthode [**IMediaSample :: SetMediaTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatime) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



