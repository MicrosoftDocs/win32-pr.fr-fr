---
description: Exemple de filtre balle
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Exemple de filtre balle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111470"
---
# <a name="ball-filter-sample"></a>Exemple de filtre balle

## <a name="description"></a>Description

Le filtre boule est un filtre de source vidéo qui produit une image d’une balle rebondissante. Cet exemple illustre la négociation de format et l’utilisation des classes de base de filtre source [**CSource**](csource.md) et [**CSourceStream**](csourcestream.md).

Le code dans Fball. h et Fball. cpp gère les interfaces de filtre. Ces deux fichiers contiennent approximativement le code minimum requis pour un filtre source. Les fichiers ball. h et ball. cpp contiennent le code qui rebondit la balle.

Ce filtre a une seule broche de sortie, qui fournit un flux vidéo qui montre une balle dans le cadre. Le filtre boule accepte également les demandes de gestion de la qualité du filtre en aval, qui illustre une stratégie de gestion de la qualité simple. Ce filtre implémente l’interface [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) à cet effet.

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

cet exemple est installé sous le chemin d’accès suivant : \[ exemples *racine du kit de développement logiciel (SDK)* \] \\ exemples de filtres de \\ DirectShow multimédias \\ \\ \\ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Extraits](directshow-samples.md)
</dt> </dl>

 

 



