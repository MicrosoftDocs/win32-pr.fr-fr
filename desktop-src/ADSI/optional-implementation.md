---
title: Implémentation facultative
description: Les fonctionnalités suivantes sont facultatives, mais recommandées
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Implémentation facultative d’ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3074f3ef6b4d36713d483937ad0f6ef10167777a7c36f8d21427d7df2b0485a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838949"
---
# <a name="optional-implementation"></a>Implémentation facultative

Les fonctionnalités suivantes sont facultatives, mais recommandées :

-   Interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pour les clients non-Automation. Étant donné que le fournisseur d’OLE DB ADSI utilise **IDirectorySearch** pour présenter des requêtes et collecter les résultats du service d’annuaire sous-jacent, les fournisseurs qui implémentent cette interface fournissent automatiquement l’accès aux bases de données de style OLE DB sans avoir à implémenter d’interfaces supplémentaires.
-   Interfaces [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)et [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) . Les fournisseurs de services d’annuaire qui prennent en charge la sécurité des objets basés sur les listes de contrôle d’accès sont encouragés à implémenter ces fonctionnalités supplémentaires.

 

 




