---
description: Une liste de contrôle d'accès (ACL) est une liste d'entrées de contrôle d'accès (ACE).
ms.assetid: c9aff246-fe11-4d82-b944-b10c3d9ae170
title: Listes de contrôle d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7021767830dead84f2ea965c46ca205257a2f18443f352ec85becc0139e30e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785659"
---
# <a name="access-control-lists"></a>Listes de contrôle d’accès

Une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL) est une liste d' [entrées de contrôle d’accès](access-control-entries.md) (ACE). Chaque ACE dans une ACL identifie un [tiers de confiance](trustees.md) et spécifie les [droits d'accès](access-rights-and-access-masks.md) autorisés, refusés ou audités pour ce tiers de confiance. Le [descripteur de sécurité](security-descriptors.md) d’un [objet sécurisable](securable-objects.md) peut contenir deux types d’ACL : une liste DACL et une liste SACL.

Une [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) identifie les approbations qui autorisent ou refusent l’accès à un objet sécurisable. Lorsqu’un [*processus*](/windows/desktop/SecGloss/p-gly) tente d’accéder à un objet sécurisable, le système vérifie les entrées du contrôle d’accès dans la liste DACL de l’objet pour déterminer s’il doit accorder l’accès à celui-ci. Si l’objet n’a pas de liste DACL, le système accorde un accès complet à tout le monde. Si la DACL de l’objet n’a pas d’ACE, le système refuse toutes les tentatives d’accès à l’objet, car la liste DACL n’autorise pas de droits d’accès. Le système vérifie les ACE en séquence jusqu’à ce qu’il trouve une ou plusieurs entrées de contrôle d’accès qui autorisent tous les droits d’accès demandés, ou jusqu’à ce que l’un des droits d’accès demandés soit refusé. Pour plus d’informations, consultez [Comment les DACL contrôlent l’accès à un objet](how-dacls-control-access-to-an-object.md). Pour plus d’informations sur la création correcte d’une liste DACL, consultez [création d’une liste DACL](/windows/desktop/SecBP/creating-a-dacl).

Une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) permet aux administrateurs d’enregistrer les tentatives d’accès à un objet sécurisé. Chaque ACE spécifie les types de tentatives d’accès d’un tiers de confiance spécifié qui obligent le système à générer un enregistrement dans le journal des événements de sécurité. Une entrée du contrôle d’accès dans une liste SACL peut générer des enregistrements d’audit lorsqu’une tentative d’accès échoue, qu’elle réussit ou les deux. Pour plus d’informations sur les listes SACL, consultez droit [d’accès génération d’audit](audit-generation.md) et [accès SACL](sacl-access-right.md).

N’essayez pas de travailler directement avec le contenu d’une liste de contrôle d’accès. Pour vous assurer que les listes de contrôle d’accès sont sémantiquement correctes, utilisez les fonctions appropriées pour créer et manipuler des listes de contrôle d’accès. Pour plus d’informations, consultez [obtention d’informations à partir d’une liste de contrôle d’accès](getting-information-from-an-acl.md) et [création ou modification d’une liste de contrôle d’accès](creating-or-modifying-an-acl.md).

Les ACL fournissent également un contrôle d’accès aux objets du service d’annuaire Microsoft Active Directory. Les interfaces ADSI (Active Directory Service Interfaces) incluent des routines pour créer et modifier le contenu de ces listes de contrôle d’accès. Pour plus d’informations, consultez [contrôle de l’accès aux objets Active Directory](/windows/desktop/AD/controlling-access-to-objects-in-active-directory-domain-services).

 

 
