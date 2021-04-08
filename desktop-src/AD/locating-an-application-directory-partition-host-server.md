---
title: Localisation d’un serveur hôte de partition d’annuaire d’applications
description: Cette rubrique explique comment localiser un serveur hôte de partition de l’annuaire d’applications.
ms.assetid: 636e8bc2-136c-42be-aa64-1b059dedf775
ms.tgt_platform: multiple
keywords:
- Recherche d’un serveur hôte de partition d’annuaire d’applications AD
- Partitions de l’annuaire d’applications Active Directory, localisation d’un serveur hôte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c9e8f80ccf4b1549af9a76e7b588685d38c297
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671270"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Localisation d’un serveur hôte de partition d’annuaire d’applications

Le service Netlogon inscrit la liste suivante d’enregistrements SRV pour une partition de l’annuaire d’applications :

-   \_LDAP. \_ protocoles.<partition name>
-   \_LDAP. \_ TCP. <site name> . \_ sites.<partition name>

Pour localiser un contrôleur de domaine qui héberge un réplica d’une partition d’annuaire d’applications spécifiée, appelez la fonction [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) avec le paramètre *domainname* défini sur le nom DNS de la partition de l’annuaire d’applications et l’indicateur **DS \_ uniquement \_ LDAP \_ requis** défini dans le paramètre *Flags* . Pour plus d’informations et pour obtenir un exemple de code qui montre, à l’aide de la fonction **DsGetDcName** , comment localiser un contrôleur de domaine qui héberge un réplica d’une partition d’annuaire d’applications, consultez l' [exemple de code pour localiser un serveur hôte de partition d’annuaire d’applications](example-code-for-locating-an-application-directory-partition-host-server.md).

 

 




