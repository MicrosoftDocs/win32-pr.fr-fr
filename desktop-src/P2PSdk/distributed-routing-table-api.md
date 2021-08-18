---
description: L’API DRT (Distributed Routing Table) permet aux applications de publier et de résoudre des clés numériques sur un réseau pair à pair.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: API Table de routage distribué
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9adabac4e2e885a7ac635daf5de2dfbacc94dafd4972a6b35f1f4649c3428e92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011607"
---
# <a name="distributed-routing-table-api"></a>API Table de routage distribué

L’API DRT (Distributed Routing Table) permet aux applications de publier et de résoudre des clés numériques sur un réseau pair à pair.

Une application utilisant DRT peut effectuer les opérations suivantes :

-   Créer des tables de routage distribuées spécifiques à l’application.
-   Enregistrez les clés et associez ces clés aux adresses IP et aux données d’application.
-   Recherchez les clés et récupérez les adresses IP et les données d’application qui leur sont associées. Cette fonctionnalité peut être utilisée pour construire des tables de hachage distribuée (DHTs), des systèmes de résolution de noms sans serveur et des réseaux de maillage de superposition de nombreuses topologies.

> [!Note]  
> Les administrateurs et les utilisateurs des applications compatibles DRT doivent rendre les utilisateurs finaux de leurs applications informés des informations publiées. Les serveurs Microsoft ne sont pas utilisés par cette technologie et les informations ne sont pas envoyées à Microsoft.

 

La documentation fournie pour cette API est divisée en trois sections.



| Section                                                                                | Description                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [À propos des tables de routage distribuées](about-distributed-routing-tables.md)               | Informations détaillant le cycle de vie et les changements d’état de l’API DRT.<br/>                                    |
| [Utilisation du API Table de routage distribué](using-the-distributed-routing-table-api.md) | Informations détaillant l’utilisation générale de l’API DRT.<br/>                                                   |
| [Référence de API Table de routage distribué](distributed-routing-table-api-reference.md) | Informations détaillant les fonctions, les structures de données et les constantes énumérées qui composent l’API DRT.<br/> |



 

 

 




