---
title: Ajout ou suppression d’un réplica de partition d’annuaire d’applications
description: Le premier réplica d’une partition d’annuaire d’applications est créé sur le contrôleur de domaine qui lui a été lié au moment de la création.
ms.assetid: 2dafc822-d0e8-4960-9a45-cc21d1d2924c
ms.tgt_platform: multiple
keywords:
- Ajout ou suppression d’un réplica de partition d’annuaire d’applications AD
- Partitions de l’annuaire d’applications Active Directory, ajout ou suppression d’un réplica de partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c84b19e64f6abfc5e63d6e0e3d1b3a192da3e38
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101464"
---
# <a name="adding-or-deleting-an-application-directory-partition-replica"></a>Ajout ou suppression d’un réplica de partition d’annuaire d’applications

Le premier réplica d’une partition d’annuaire d’applications est créé sur le contrôleur de domaine qui lui a été lié au moment de la création. Des réplicas supplémentaires peuvent être créés sur n’importe quel contrôleur de domaine de la forêt, pas nécessairement dans le même domaine que le contrôleur de domaine initial. Un réplica de partition d’annuaire d’applications ne peut exister que sur un contrôleur de domaine qui exécute Windows Server 2003 ou une version ultérieure. Pour plus d’informations, consultez cet article TechNet sur la [gestion des partitions](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10)).

**Pour ajouter un réplica pour une partition d’annuaire d’applications, procédez comme suit :**

1.  Recherchez dans le conteneur de partitions un objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) dont la valeur d’attribut [**NCName**](/windows/desktop/ADSchema/a-ncname) est égale au nom unique de la partition d’annuaire d’applications.
2.  Crée une liaison avec l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) avec la délégation activée. Cela est nécessaire, car l’objet **crossRef** peut uniquement être modifié sur le détenteur du rôle Domain-Naming FSMO. Si la délégation est activée, le contrôleur de domaine peut contacter le détenteur du rôle Domain-Naming FSMO en utilisant les mêmes informations d’identification.
3.  Ajoutez le nom unique de l’objet [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) pour le contrôleur de domaine qui hébergera le nouveau réplica à l’attribut [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

Lorsque la nouvelle valeur de l’attribut [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) est répliquée sur le nouveau contrôleur de domaine qui hébergera un réplica de la partition de l’annuaire d’applications, le KCC sera déclenché pour répliquer la partition de l’annuaire d’applications sur le contrôleur de domaine cible.

Pour supprimer un réplica pour une partition d’annuaire d’applications, effectuez les mêmes étapes que ci-dessus pour localiser l’objet [**crossRef**](/windows/desktop/ADSchema/c-crossref) qui représente la partition de l’annuaire d’applications et supprimez la valeur qui correspond au contrôleur de domaine de l’attribut [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de l’objet **crossRef** .

Lorsque la nouvelle valeur de l’attribut [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) est répliquée sur le contrôleur de domaine qui n’hébergera plus de réplica de la partition de l’annuaire d’applications, le KCC sera déclenché pour supprimer le réplica de la partition de l’annuaire d’applications sur le contrôleur de domaine cible.

Si un contrôleur de domaine qui héberge un réplica de partition d’annuaire d’applications est supprimé ou rétrogradé, le serveur de Active Directory supprime automatiquement la valeur correspondant au contrôleur de domaine de l’attribut [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) de tous les objets [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

 

 