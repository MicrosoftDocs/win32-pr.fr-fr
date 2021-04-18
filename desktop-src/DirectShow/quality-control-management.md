---
description: Gestion des Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Gestion des Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68aff4f8c054f9f649801e1b9829ccd7daaff35
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516330"
---
# <a name="quality-control-management"></a>Gestion des Quality-Control

Le contrôle de la qualité est un mécanisme permettant d’ajuster le taux de transmission de données via le graphique de filtre en réponse aux performances d’exécution. Si un filtre de convertisseur reçoit trop de données ou trop peu de données, il peut envoyer un *message de qualité*. Le message de qualité demande un ajustement dans le débit des données. Par défaut, les messages de qualité voyagent en amont du convertisseur jusqu’à ce qu’ils atteignent un filtre qui peut répondre (le cas échéant). Une application peut également implémenter un gestionnaire de qualité personnalisé. Dans ce cas, le convertisseur transmet les messages de qualité directement au gestionnaire de qualité de l’application.

Cet article contient les rubriques suivantes.

-   [Messages de qualité](quality-messages.md)
-   [Contrôle qualité par défaut](default-quality-control.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transmission de données pour les développeurs de filtres](data-flow-for-filter-developers.md)
</dt> <dt>

[Écriture de filtres DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



