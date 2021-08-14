---
title: Modification de la configuration de la partition d’annuaire d’applications
description: Une partition d’annuaire d’applications peut être modifiée par la modification de certains attributs de l’objet crossRef qui représente la partition de l’annuaire d’applications.
ms.assetid: c4db5b3f-7d80-46a0-8a3a-9b1eb3c9f7b1
ms.tgt_platform: multiple
keywords:
- Modification de la configuration de la partition d’annuaire d’applications AD
- Partitions de l’annuaire d’applications Active Directory, modification de la configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc378536a552bb7612877fc09913fdbad9daf507adbb34b5f53f8946c946e8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186314"
---
# <a name="modifying-application-directory-partition-configuration"></a>Modification de la configuration de la partition d’annuaire d’applications

Une partition d’annuaire d’applications peut être modifiée par la modification de certains attributs de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui représente la partition de l’annuaire d’applications. Pour localiser l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui représente une partition d’annuaire d’applications particulière, recherchez dans le conteneur de partitions un objet **crossRef** dont la valeur d’attribut [**NCName**](/windows/desktop/ADSchema/a-ncname) est égale au nom unique de la partition de l’annuaire d’applications. Le nom unique de l’objet **crossRef** peut ensuite être utilisé pour établir une liaison à l’objet **crossRef** .

Le tableau suivant répertorie les attributs de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui peuvent être modifiés.

| Attribut                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**msDS-Replication-notification-First-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-first-dsa-delay)           | Spécifie le délai, en secondes, après la modification d’un objet d’origine avant que le premier partenaire de réplication soit notifié. Pour plus d’informations, consultez [réplication de la partition](application-directory-partition-replication.md)de l’annuaire d’applications.                                                                                                   |
| [**msDS-Replication-Notify-subséquent-DSA-Delay**](/windows/desktop/ADSchema/a-msds-replication-notify-subsequent-dsa-delay) | Spécifie le délai, en secondes, entre les notifications suivantes au deuxième, troisième, et ainsi de suite sur les partenaires de réplication. Pour plus d’informations, consultez [réplication de la partition](application-directory-partition-replication.md)de l’annuaire d’applications.                                                                                                 |
| [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain)                                             | Identifie le domaine que le sous-système de sécurité utilise pour interpréter les références de domaine local dans les attributs [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) des objets dans cette partition d’annuaire d’applications. Pour plus d’informations, consultez sécurité de la [partition d’annuaire d’applications](application-directory-partition-security.md). |
| [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)                                       | Contient le nom unique de l’objet [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) pour chaque contrôleur de domaine qui héberge un réplica de la partition de l’annuaire d’applications. Pour plus d’informations, consultez [Ajout ou suppression d’un réplica de partition d’annuaire d’applications](adding-or-deleting-an-application-directory-partition-replica.md).            |



 

 

 