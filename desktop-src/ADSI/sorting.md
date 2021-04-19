---
title: Tri (ADSI)
description: Un client peut demander à un serveur de trier le jeu de résultats.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "106509021"
---
# <a name="sorting-adsi"></a>Tri (ADSI)

Un client peut demander à un serveur de trier le jeu de résultats. Vous pouvez spécifier les valeurs suivantes :

-   Ordre de tri : l’ordre de tri croissant ou décroissant peut être spécifié.
-   Attributs de tri : plusieurs attributs peuvent être spécifiés dans une chaîne de tri. Par exemple, triez par nom, puis par prénom.

Lorsque vous spécifiez l’ordre de tri, vous devez essayer d’utiliser l’un des attributs indexés. Dans le cas contraire, le serveur doit calculer un jeu de résultats complet avant de l’envoyer au client. Cela est vrai même si vous avez demandé une recherche paginée et spécifié une taille de page.

> [!Note]  
> Tous les serveurs d’annuaire ne prennent pas en charge plusieurs tris d’attribut ou ordre de tri.

 

 

 




