---
description: Le flux d’informations de synthèse contient des informations sur le package qui peuvent être consultées via l’Explorateur Microsoft Windows.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: À propos du flux d’informations de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115394"
---
# <a name="about-the-summary-information-stream"></a>À propos du flux d’informations de synthèse

Le flux d’informations de synthèse contient des informations sur le package qui peuvent être consultées via l’Explorateur Microsoft Windows. Ces informations sont accessibles via l’interface **IStream** . Il revient à l’auteur de fournir les valeurs de chacune de ces propriétés.

Le flux d’informations de synthèse utilise COM pour fournir un stockage structuré des bases de données. COM prend en charge le concept de stockage structuré accessible via l’interface **IStream** . Le stockage structuré, à son tour, prend en charge le concept de jeux de propriétés comme méthode flexible pour sérialiser pratiquement toutes les informations. La spécification COM définit un jeu de propriétés standard unique, des informations de synthèse, qui est utilisé pour remplir les feuilles de propriétés visibles à partir de l’Explorateur Windows. Par conséquent, les utilisateurs peuvent afficher les informations stockées dans le flux d’informations de résumé lorsqu’ils cliquent avec le bouton droit sur une base de données du programme d’installation ou qu’ils sélectionnent [Propriétés](about-properties.md).

Pour obtenir la liste des propriétés de résumé, consultez [jeu de propriétés de flux d’informations résumées](summary-information-stream-property-set.md).

Pour obtenir une brève description des propriétés des informations de résumé utilisées avec les bases de données, les transformations et les correctifs, consultez [descriptions des propriétés récapitulatives](summary-property-descriptions.md).

 

 



