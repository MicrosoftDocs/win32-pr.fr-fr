---
title: Implémentation facultative
description: Les fonctionnalités suivantes sont facultatives, mais recommandées
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Implémentation facultative d’ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507027"
---
# <a name="optional-implementation"></a>Implémentation facultative

Les fonctionnalités suivantes sont facultatives, mais recommandées :

-   Interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) pour les clients non-Automation. Étant donné que le fournisseur d’OLE DB ADSI utilise **IDirectorySearch** pour présenter des requêtes et collecter les résultats du service d’annuaire sous-jacent, les fournisseurs qui implémentent cette interface fournissent automatiquement l’accès aux bases de données de style OLE DB sans avoir à implémenter d’interfaces supplémentaires.
-   Interfaces [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)et [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) . Les fournisseurs de services d’annuaire qui prennent en charge la sécurité des objets basés sur les listes de contrôle d’accès sont encouragés à implémenter ces fonctionnalités supplémentaires.

 

 




