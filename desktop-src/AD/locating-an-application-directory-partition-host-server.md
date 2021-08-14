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
ms.openlocfilehash: e3cef9442d694b80893f67d5530b83aa188df4d172028271117492ed221bd239
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186790"
---
# <a name="locating-an-application-directory-partition-host-server"></a>Localisation d’un serveur hôte de partition d’annuaire d’applications

Le service Netlogon inscrit la liste suivante d’enregistrements SRV pour une partition de l’annuaire d’applications :

-   \_LDAP. \_ protocoles.<partition name>
-   \_LDAP. \_ TCP. <site name> . \_ sites.<partition name>

Pour localiser un contrôleur de domaine qui héberge un réplica d’une partition d’annuaire d’applications spécifiée, appelez la fonction [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) avec le paramètre *domainname* défini sur le nom DNS de la partition de l’annuaire d’applications et l’indicateur **DS \_ uniquement \_ LDAP \_ requis** défini dans le paramètre *Flags* . Pour plus d’informations et pour obtenir un exemple de code qui montre, à l’aide de la fonction **DsGetDcName** , comment localiser un contrôleur de domaine qui héberge un réplica d’une partition d’annuaire d’applications, consultez l' [exemple de code pour localiser un serveur hôte de partition d’annuaire d’applications](example-code-for-locating-an-application-directory-partition-host-server.md).

 

 




