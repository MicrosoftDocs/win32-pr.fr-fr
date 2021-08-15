---
description: Une entrée de contrôle d’accès (ACE) est un élément dans une liste de contrôle d’accès (ACL).
ms.assetid: 9cf4d796-3955-456b-9db9-ae9fa83752f6
title: Entrées Access Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8adcc382da130c57c55b869c47c8837c7780a7cff4e6dbdd881e55aa7b724dc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785649"
---
# <a name="access-control-entries"></a>Entrées Access Control

Une [*entrée de contrôle*](/windows/desktop/SecGloss/a-gly) d’accès (ACE) est un élément dans une [*liste de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACL). Une liste de contrôle d’accès peut avoir zéro ou plusieurs entrées de contrôle d’accès. Chaque ACE contrôle ou surveille l’accès à un objet par un tiers de confiance spécifié. Pour plus d’informations sur l’ajout, la suppression ou la modification des entrées du contrôle d’accès dans les listes de contrôle d’accès d’un objet, consultez [modification des listes de contrôle d’accès d’un objet en C++](modifying-the-acls-of-an-object-in-c--.md).

Il existe six types d’ACE, dont trois sont pris en charge par tous les objets sécurisables. Les trois autres types sont des [ACE spécifiques](object-specific-aces.md) aux objets pris en charge par les objets de service d’annuaire.

Tous les types d’ACE contiennent les informations de contrôle d’accès suivantes :

-   [Identificateur de sécurité](security-identifiers.md) (SID) qui identifie le [tiers de confiance](trustees.md) auquel l’entrée du contrôle d’accès s’applique.
-   [*Masque d’accès*](/windows/desktop/SecGloss/a-gly) qui spécifie les [droits d’accès](access-rights-and-access-masks.md) contrôlés par l’entrée du contrôle d’accès.
-   Indicateur qui spécifie le type d’entrée du contrôle d’accès.
-   Jeu d’indicateurs de bits qui déterminent si les conteneurs enfants ou les objets peuvent hériter de l’entrée du contrôle d’accès de l’objet principal auquel la liste ACL est attachée.

Le tableau suivant répertorie les trois types d’entrées du contrôle d’accès pris en charge par tous les objets sécurisables.



| Type               | Description                                                                                                                                                                                                                                      |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACE accès refusé  | Utilisé dans une [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) pour refuser les droits d’accès à un tiers de confiance.                                       |
| Accès-ACE autorisé | Utilisé dans une liste DACL pour autoriser les droits d’accès à un tiers de confiance.                                                                                                                                                                                              |
| ACE système-audit   | Utilisé dans une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL) pour générer un enregistrement d’audit lorsque le tiers de confiance tente d’exercer les droits d’accès spécifiés. |



 

Pour obtenir une table des ACE spécifiques aux objets, consultez [ACE spécifiques aux objets](object-specific-aces.md).

> [!Note]  
> Les ACE de l’objet System-Alarm ne sont pas prises en charge actuellement.

 

 

 
