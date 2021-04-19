---
description: Exemple de filtre métronome
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Exemple de filtre métronome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514718"
---
# <a name="metronome-filter-sample"></a>Exemple de filtre métronome

## <a name="description"></a>Description

Cet exemple de filtre montre comment implémenter une horloge de référence. Le filtre utilise votre entrée de microphone par défaut pour écouter les pics audio (tels que les clics, les clapss de main ou les toux) qu’il utilise pour déterminer une fréquence d’horloge.

## <a name="usage"></a>Utilisation

Générez l’exemple de projet et copiez la DLL de filtre (Metronom.ax) dans le répertoire système de Windows. Exécutez le fichier métronome. reg pour inscrire la DLL.

Pour utiliser le filtre :

1.  Générez un graphique de filtre dans GraphEdit qui restitue un flux vidéo.
2.  Supprimez tous les flux audio rendus.
3.  Ajoutez le filtre métronome au graphique. Il apparaît dans la catégorie filtres DirectShow.
4.  Exécutez le graphique. La vidéo commence à s’exécuter à la vitesse normale.
5.  Clap vos mains ou utilisez un métronome pour définir une nouvelle vitesse.

## <a name="programming-notes"></a>Notes de programmation

Ce filtre fonctionne uniquement pour la vidéo. Le convertisseur audio ne peut pas se synchroniser à des fréquences d’horloge radicalement différentes.

Si vous Clap 92 fois par minute (une fois toutes les ~ 652 ms), la vidéo est lue au taux normal. Vous pouvez modifier ce paramètre par défaut en modifiant la valeur de la constante `BPM` dans métronome. cpp.

Si vous arrêtez applaudissements pendant un certain temps, puis redémarrez applaudissements, vous devez redémarrer à peu près la même vitesse ou le filtre l’ignore. En outre, la vitesse de lecture de la vidéo est limitée par la vitesse du processeur. Si vous dépassez la limite pour une durée quelconque, le filtre ne répondra plus aux changements de taux. Dans ce cas, arrêtez le graphique et redémarrez.

Si vous implémentez votre propre horloge, les règles les plus importantes sont que les horloges de référence ne doivent pas revenir en arrière. Autrement dit, ils ne doivent jamais signaler une valeur d’heure inférieure à la valeur d’heure précédente.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] SDK* \\ exemples de \\ \\ filtres DirectShow multimédias \\ \\ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> <dt>

[Exemples DirectShow](directshow-samples.md)
</dt> </dl>

 

 



