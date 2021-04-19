---
title: Problèmes de liaison pour les environnements mixtes
description: Problèmes de liaison pour les environnements mixtes
ms.assetid: d9f9a6bc-7733-4269-99c8-61a84b37d487
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, avec, problèmes de liaison pour les environnements mixtes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65135e0562f387ee9b70e2395d807b639a48e37
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509059"
---
# <a name="binding-issues-for-mixed-environments"></a><span data-ttu-id="4698d-104">Problèmes de liaison pour les environnements mixtes</span><span class="sxs-lookup"><span data-stu-id="4698d-104">Binding Issues for Mixed Environments</span></span>

<span data-ttu-id="4698d-105">Pour les environnements dans lesquels le domaine qui contient Active Directory a une relation d’approbation avec un domaine Windows NT 4,0, il peut y avoir un problème avec l’utilisation de la liaison sans serveur pour la liaison à des objets Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4698d-105">For environments in which the domain that contains Active Directory has a trust relationship with a Windows NT 4.0 domain, there may be a problem with using serverless binding to bind to Active Directory objects.</span></span>

<span data-ttu-id="4698d-106">Dans certains environnements réseau, les relations d’approbation ont été configurées entre les contrôleurs de domaine qui contiennent des Active Directory et des serveurs Windows NT 4,0 afin d’autoriser l’authentification entre les domaines.</span><span class="sxs-lookup"><span data-stu-id="4698d-106">In some networking environments, trust relationships have been set up between domain controllers that contain Active Directory and Windows NT 4.0 servers for the purpose of allowing authentication between domains.</span></span> <span data-ttu-id="4698d-107">Dans ces environnements mixtes, si un utilisateur qui est membre du Windows NT 4,0, le domaine tente d’utiliser une liaison sans serveur pour établir une liaison à un objet Active Directory sur un domaine approuvé, la liaison échoue et une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="4698d-107">In these mixed environments, if a user, who is a member of the Windows NT 4.0, domain attempts to use serverless binding to bind to an Active Directory object on a trusted domain, then the bind will fail and an error is returned.</span></span> <span data-ttu-id="4698d-108">Cela est dû au fait qu’une liaison sans serveur utilise la fonction [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) pour établir une liaison à l’objet dans Active Directory, qui dépend du DNS approprié.</span><span class="sxs-lookup"><span data-stu-id="4698d-108">This is because a serverless bind uses the [**DsGetDcName**](/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea) function to bind to the object in Active Directory, which is dependent upon the proper DNS.</span></span>

<span data-ttu-id="4698d-109">Dans ce scénario, l’utilisateur Windows NT doit fournir le nom d’un domaine spécifique auquel effectuer la liaison.</span><span class="sxs-lookup"><span data-stu-id="4698d-109">In this scenario, the Windows NT user must provide the name of a specific domain to bind to.</span></span> <span data-ttu-id="4698d-110">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="4698d-110">The following is an example.</span></span>

``` syntax
LDAP://fabrikam.com/OU=Sales
```

 

 