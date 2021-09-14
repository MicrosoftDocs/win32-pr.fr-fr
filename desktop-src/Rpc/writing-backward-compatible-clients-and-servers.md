---
title: Écriture de clients et de serveurs à compatibilité descendante
description: En théorie, le schéma de contrôle de version de RPC permet d’éviter une communication inversée entre les serveurs et les clients modifiés et leurs homologues déployés.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- RPC appel de procédure distante, meilleures pratiques, compatibilité descendante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011365"
---
# <a name="writing-backward-compatible-clients-and-servers"></a>Écriture de clients et de serveurs à compatibilité descendante

En théorie, le schéma de contrôle de version de RPC permet d’éviter une communication inversée entre les serveurs et les clients modifiés et leurs homologues déployés. En pratique, toutefois, les développeurs doivent souvent introduire des modifications dans les interfaces existantes sans modifier la version, car les clients et les serveurs précédents doivent être en mesure de communiquer avec eux. Il s’agit d’un problème plus important pour RPC standard que pour COM ; l’interrogation est un moyen naturel de rechercher des interfaces prises en charge dans COM, tandis que dans la gestion des exceptions RPC doit être utilisé pour une couverture équivalente.

Cette section décrit les meilleures pratiques de programmation RPC pour traiter ces situations. Cette section est composée des rubriques suivantes :

-   [La théorie de la gestion des versions pour RPC et COM](the-versioning-theory-for-rpc-and-com.md)
-   [Modification des interfaces d’une manière à compatibilité descendante](changing-interfaces-in-a-backward-compatible-manner.md)
-   [Exemples de modifications incompatibles](examples-of-incompatible-changes.md)

 

 




