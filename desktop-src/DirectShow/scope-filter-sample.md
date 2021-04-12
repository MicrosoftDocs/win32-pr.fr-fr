---
description: Exemple de filtre d’étendue
ms.assetid: f967d4c7-94d2-440b-9e52-423feefec66d
title: Exemple de filtre d’étendue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74ba823e68da1cd1faadd3e1e3acc4e613e2f42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481520"
---
# <a name="scope-filter-sample"></a>Exemple de filtre d’étendue

## <a name="description"></a>Description

Le filtre d’étendue est un filtre de convertisseur qui affiche des données audio sous forme de formes Wave.

## <a name="usage"></a>Utilisation

Pour utiliser ce filtre, ouvrez GraphEdit et affichez un fichier audio (ou un fichier vidéo avec un flux audio). Déconnectez le convertisseur audio temporairement et insérez l’exemple de filtre Infinite-Pin tee ([exemple de filtre InfTee](inftee-filter-sample.md)). Reconnectez le convertisseur audio. Connectez ensuite la deuxième broche de sortie du filtre de l' Infinite-Pin tee au filtre d’étendue. Exécutez maintenant le graphique.

La fenêtre d’étendue est implémentée en tant que boîte de dialogue, et non en tant que fenêtre réelle. Les développeurs qui créent des panneaux de contrôle pour modifier les paramètres de filtre en temps réel peuvent souhaiter utiliser une technique comme celle-ci plutôt que des pages de propriétés.

Le filtre d’étendue illustre la configuration d’un thread distinct pour traiter les données. Dans ce cas, les données sont simplement copiées dans une mémoire tampon distincte sur la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) , puis sont dessinées dans la fenêtre d’étendue sur le thread distinct.

Le filtre d’étendue vous permet également de surveiller la sortie audio pour déterminer si vous découpez, afin de pouvoir ajuster le gain.

Ce filtre apparaît dans GraphEdit sous le titre « oscilloscope ».

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] SDK* \\ étendue des \\ \\ \\ filtres DirectShow \\ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples DirectShow](directshow-samples.md)
</dt> </dl>

 

 



