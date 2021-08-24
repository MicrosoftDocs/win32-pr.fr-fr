---
description: Gestion des Quality-Control
ms.assetid: b1def588-6c9c-4853-a69b-1ba5df8b5ba2
title: Gestion des Quality-Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824410b697a29ee73fc269748595fdcae91d054a161561b282536a05dcf92ef5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747709"
---
# <a name="quality-control-management"></a>Gestion des Quality-Control

Le contrôle de la qualité est un mécanisme permettant d’ajuster le taux de transmission de données via le graphique de filtre en réponse aux performances d’exécution. Si un filtre de convertisseur reçoit trop de données ou trop peu de données, il peut envoyer un *message de qualité*. Le message de qualité demande un ajustement dans le débit des données. Par défaut, les messages de qualité voyagent en amont du convertisseur jusqu’à ce qu’ils atteignent un filtre qui peut répondre (le cas échéant). Une application peut également implémenter un gestionnaire de qualité personnalisé. Dans ce cas, le convertisseur transmet les messages de qualité directement au gestionnaire de qualité de l’application.

Cet article contient les rubriques suivantes.

-   [Messages de qualité](quality-messages.md)
-   [Contrôle qualité par défaut](default-quality-control.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Flow de données pour les développeurs de filtres](data-flow-for-filter-developers.md)
</dt> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



