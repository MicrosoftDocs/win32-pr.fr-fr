---
description: Exemple de filtre dump
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Exemple de filtre dump
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324909"
---
# <a name="dump-filter-sample"></a>Exemple de filtre dump

## <a name="description"></a>Description

Le filtre de vidage est un filtre de convertisseur qui écrit les exemples de supports qu’il reçoit dans un fichier texte.

Cet exemple illustre l’utilisation de la classe de filtre de base [**CBaseFilter**](cbasefilter.md) et de la classe de code confidentiel d’entrée rendue [**CRenderedInputPin**](crenderedinputpin.md). Il montre également comment implémenter l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) . Le filtre de vidage a une seule broche d’entrée, qui écrit chaque exemple qu’il reçoit directement dans un fichier.

## <a name="usage"></a>Usage

Ce filtre est un outil de débogage utile. Par exemple, vous pouvez vérifier, bit par bit, les résultats d’un filtre de transformation. Vous pouvez créer un graphique manuellement à l’aide de GraphEdit et connecter le filtre de vidage à la sortie d’un filtre de transformation ou de toute autre broche de sortie. Vous pouvez également connecter un filtre tee et placer le filtre de vidage sur une des jambes du filtre tee et la sortie standard sur une autre jambe pour analyser les résultats dans un scénario en temps réel.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ fichiers de DirectShow de filtres de \\ \\ \\ \\ vidage.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Extraits](directshow-samples.md)
</dt> </dl>

 

 



