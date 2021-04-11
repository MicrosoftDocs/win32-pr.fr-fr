---
title: Considérations relatives à la sauvegarde Active Directory Domain Services
description: Les données du service d’annuaire peuvent être répliquées. Un plan de récupération doit être créé avant la restauration.
ms.assetid: b03215db-1b8d-45b0-85e8-c325b225c6eb
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, planification de la récupération
- Active Directory Domain Services Active Directory, sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52bf284804ba5a8882ecee6f6e03ae95249e5435
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031042"
---
# <a name="considerations-for-active-directory-domain-services-backup"></a>Considérations relatives à la sauvegarde Active Directory Domain Services

Les données du service d’annuaire peuvent être répliquées. Un plan de récupération doit être créé avant la restauration. L’une des options consiste à restaurer un réplica d’un répertoire, puis à propager les modifications qui se sont produites depuis la sauvegarde à partir d’autres réplicas dans le domaine.

Dans certains cas, vous souhaiterez peut-être que le réplica restauré soit prioritaire sur les autres réplicas du domaine. Par exemple, si un objet est supprimé par inadvertance et que la suppression est répliquée sur tous les contrôleurs de domaine, vous pouvez restaurer l’objet en restaurant un réplica à partir d’une sauvegarde effectuée avant la suppression de l’objet. Vous devez ensuite utiliser l’utilitaire NTDSUtil pour marquer l’objet restauré comme restauré en faisant autorité. L’objet restauré sera ensuite répliqué sur les autres contrôleurs de contrôle, et le réplica restauré recevra les mises à jour de tous les autres objets qui se sont produits depuis le moment où la sauvegarde a été effectuée. Le résultat final de tous les réplicas est le même que celui utilisé avant la restauration, sauf que l’objet restauré faisant autorité n’est plus supprimé.

Toutes les modifications qui se produisent pendant la sauvegarde sont stockées dans un journal temporaire et ajoutées à la fin du jeu de sauvegarde lorsque la sauvegarde est terminée.

Tout plan de récupération doit s’assurer que l’ancienneté de la sauvegarde ne doit pas dépasser la durée de vie de désactivation de Active Directory. Pour plus d’informations sur la durée de vie de la désactivation, consultez la rubrique TechNet- [Introduction à l’administration de Active Directory sauvegarde et récupération](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc816677(v=ws.10)). La restauration d’une sauvegarde antérieure à la durée de vie de l’objet tombstone peut entraîner l’ajout d’objets qui ne seront pas répliqués sur d’autres contrôleurs de domaine dans le contrôleur de domaine restauré. Cela se produit si un objet est supprimé après la sauvegarde et si la restauration a lieu après la suppression définitive de la désactivation de l’objet supprimé. Le contrôleur de périphérique restauré aurait l’objet tel qu’il existait avant la suppression, et les autres contrôleurs de service n’auraient pas d’enregistrement que l’objet existait déjà. Dans ce cas, un administrateur devra supprimer manuellement chaque objet non répliqué sur le contrôleur de domaine restauré.

Les sauvegardes incrémentielles de Active Directory Domain Services ne sont pas prises en charge ; des sauvegardes complètes sont requises.

 

 