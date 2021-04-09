---
title: Sécurité de la partition de l’annuaire d’applications
description: Le modèle de sécurité et de contrôle d’accès pour les partitions d’annuaire d’applications est le même que pour les autres partitions dans Active Directory Domain Services.
ms.assetid: 3e14b31a-524e-4b38-957f-166e80b35b31
ms.tgt_platform: multiple
keywords:
- Sécurité de la partition de l’annuaire d’applications AD
- Partitions de l’annuaire d’applications AD, sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80da4ce1b8d4e3604b8e546d79003f4d3719223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940842"
---
# <a name="application-directory-partition-security"></a>Sécurité de la partition de l’annuaire d’applications

Le modèle de sécurité et de contrôle d’accès pour les partitions d’annuaire d’applications est le même que pour les autres partitions dans Active Directory Domain Services. Les utilisateurs normaux peuvent accéder aux objets d’une partition de l’annuaire d’applications sous réserve des listes de contrôle d’accès placées sur ces objets. Pour plus d’informations, consultez [contrôle de l’accès aux objets dans Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Toutefois, étant donné que les partitions d’annuaire d’applications peuvent s’étendre sur plusieurs domaines de sécurité dans un service d’annuaire, il est question de savoir comment interpréter les constantes de chaîne SID connues relatives au domaine dans le [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de la classe de schéma d’un objet au moment de la création de l’objet dans une partition d’annuaire d’applications. Par exemple, si « DA » fait référence au groupe administrateurs de domaine, mais dans une partition d’annuaire d’applications, il n’est pas connu du domaine auquel le groupe « DA » fait référence.

Pour résoudre ce problème, l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) d’une partition d’annuaire d’applications a un attribut [**MSDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) qui contient le nom unique du domaine de référence pour cette partition d’annuaire d’applications. Le système de sécurité utilise le domaine spécifié pour interpréter les références de domaine local pour les descripteurs de sécurité par défaut attachés aux objets créés dans cette partition d’annuaire d’applications. Le domaine de référence peut être spécifié lors de la création de l’objet **crossRef** pour une partition d’annuaire d’applications. Cela requiert, toutefois, qu’un objet **crossRef** soit créé au préalable pour la partition de l’annuaire d’applications. Si aucun domaine de référence n’est spécifié, le système définit automatiquement le domaine de référence en fonction de l’une des conditions suivantes :

-   Si le parent de l’objet de partition de l’annuaire d’applications est une autre partition de l’annuaire d’applications, l’attribut [**MSDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) de la partition de l’annuaire de l’application parente est utilisé pour le domaine de référence.
-   Si l’objet parent est un domaine, ce domaine est utilisé pour le domaine de référence.
-   S’il n’y a pas d’objet parent, le domaine racine de forêt est utilisé pour le domaine de référence.

L’attribut **crossRef** peut également être remplacé par le domaine de référence après la création de la partition, mais cela n’est pas recommandé.

Un problème similaire se produit si un groupe local est spécifié dans une liste de contrôle d’accès pour un objet dans une partition d’annuaire d’applications. Dans ce cas, l’attribut [**MSDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) ne peut pas être utilisé pour interpréter le domaine de référence d’un groupe local. Pour éviter ce problème, les groupes locaux ne doivent pas être utilisés dans les listes de contrôle d’accès des objets de partition d’annuaire d’applications.

 

 