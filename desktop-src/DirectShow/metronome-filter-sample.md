---
description: Exemple de filtre métronome
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Exemple de filtre métronome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea1b321dd2602829697862e2716c9017573a44b6162b355e78e586e14d85003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072983"
---
# <a name="metronome-filter-sample"></a>Exemple de filtre métronome

## <a name="description"></a>Description

Cet exemple de filtre montre comment implémenter une horloge de référence. Le filtre utilise votre entrée de microphone par défaut pour écouter les pics audio (tels que les clics, les clapss de main ou les toux) qu’il utilise pour déterminer une fréquence d’horloge.

## <a name="usage"></a>Usage

générez l’exemple de projet et copiez la DLL de filtre (Metronom.ax) dans votre répertoire système Windows. Exécutez le fichier métronome. reg pour inscrire la DLL.

Pour utiliser le filtre :

1.  Générez un graphique de filtre dans GraphEdit qui restitue un flux vidéo.
2.  Supprimez tous les flux audio rendus.
3.  Ajoutez le filtre métronome au graphique. il apparaît dans la catégorie filtres de DirectShow.
4.  Exécutez le graphique. La vidéo commence à s’exécuter à la vitesse normale.
5.  Clap vos mains ou utilisez un métronome pour définir une nouvelle vitesse.

## <a name="programming-notes"></a>Notes de programmation

Ce filtre fonctionne uniquement pour la vidéo. Le convertisseur audio ne peut pas se synchroniser à des fréquences d’horloge radicalement différentes.

Si vous Clap 92 fois par minute (une fois toutes les ~ 652 ms), la vidéo est lue au taux normal. Vous pouvez modifier ce paramètre par défaut en modifiant la valeur de la constante `BPM` dans métronome. cpp.

Si vous arrêtez applaudissements pendant un certain temps, puis redémarrez applaudissements, vous devez redémarrer à peu près la même vitesse ou le filtre l’ignore. En outre, la vitesse de lecture de la vidéo est limitée par la vitesse du processeur. Si vous dépassez la limite pour une durée quelconque, le filtre ne répondra plus aux changements de taux. Dans ce cas, arrêtez le graphique et redémarrez.

Si vous implémentez votre propre horloge, les règles les plus importantes sont que les horloges de référence ne doivent pas revenir en arrière. Autrement dit, ils ne doivent jamais signaler une valeur d’heure inférieure à la valeur d’heure précédente.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] SDK* \\ exemples de filtres de \\ DirectShow multimédias \\ \\ \\ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> <dt>

[DirectShow Extraits](directshow-samples.md)
</dt> </dl>

 

 



