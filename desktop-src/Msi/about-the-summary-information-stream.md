---
description: le flux d’informations de synthèse contient des informations sur le package qui peuvent être consultées par le biais de Microsoft Windows Explorer.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: À propos du flux d’informations de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5178edc9fe2a94ddd2812abb8161c88423cc17cd033d228b066d5ce74b9f1694
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146032"
---
# <a name="about-the-summary-information-stream"></a>À propos du flux d’informations de synthèse

le flux d’informations de synthèse contient des informations sur le package qui peuvent être consultées par le biais de Microsoft Windows Explorer. Ces informations sont accessibles via l’interface **IStream** . Il revient à l’auteur de fournir les valeurs de chacune de ces propriétés.

Le flux d’informations de synthèse utilise COM pour fournir un stockage structuré des bases de données. COM prend en charge le concept de stockage structuré accessible via l’interface **IStream** . Le stockage structuré, à son tour, prend en charge le concept de jeux de propriétés comme méthode flexible pour sérialiser pratiquement toutes les informations. la spécification COM définit un jeu de propriétés standard unique, des informations de synthèse, qui est utilisé pour remplir les feuilles de propriétés visibles à partir de Windows Explorer. Par conséquent, les utilisateurs peuvent afficher les informations stockées dans le flux d’informations de résumé lorsqu’ils cliquent avec le bouton droit sur une base de données du programme d’installation ou qu’ils sélectionnent [Propriétés](about-properties.md).

Pour obtenir la liste des propriétés de résumé, consultez [jeu de propriétés de flux d’informations résumées](summary-information-stream-property-set.md).

Pour obtenir une brève description des propriétés des informations de résumé utilisées avec les bases de données, les transformations et les correctifs, consultez [descriptions des propriétés récapitulatives](summary-property-descriptions.md).

 

 



