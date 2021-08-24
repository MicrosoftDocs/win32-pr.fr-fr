---
title: Tri (ADSI)
description: Un client peut demander à un serveur de trier le jeu de résultats.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555b4b6f1868b2e4fddc1891cdf349ef6f44bc47dca6eb80e021ec49cb91b5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082223"
---
# <a name="sorting-adsi"></a>Tri (ADSI)

Un client peut demander à un serveur de trier le jeu de résultats. Vous pouvez spécifier les valeurs suivantes :

-   Ordre de tri : l’ordre de tri croissant ou décroissant peut être spécifié.
-   Attributs de tri : plusieurs attributs peuvent être spécifiés dans une chaîne de tri. Par exemple, triez par nom, puis par prénom.

Lorsque vous spécifiez l’ordre de tri, vous devez essayer d’utiliser l’un des attributs indexés. Dans le cas contraire, le serveur doit calculer un jeu de résultats complet avant de l’envoyer au client. Cela est vrai même si vous avez demandé une recherche paginée et spécifié une taille de page.

> [!Note]  
> Tous les serveurs d’annuaire ne prennent pas en charge plusieurs tris d’attribut ou ordre de tri.

 

 

 




