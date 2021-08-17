---
description: L’enregistreur de Active Directory ne requiert aucune action spéciale pendant les opérations de sauvegarde.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: Sauvegarde et restauration VSS du Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8312e974d705cd193eaaecdaa163a2d408836aedfb14c21ff97f72486efbf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751482"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>Sauvegarde et restauration VSS du Active Directory

L’enregistreur de Active Directory ne requiert aucune action spéciale pendant les opérations de sauvegarde. Le rédacteur fournit au demandeur des informations sur les composants et les jeux de fichiers, et le demandeur utilise ces informations pour décider quels fichiers copier sur le support de sauvegarde. Il n’est pas nécessaire d’utiliser des API spéciales pour sauvegarder le Active Directory.

La façon dont une restauration est effectuée varie selon que la Active Directory est restaurée dans le cadre d’une opération de récupération d’urgence ou si la restauration s’effectue sur un système sur lequel le Active Directory s’exécute. En outre, l’ancienneté de la copie de sauvegarde de l’état de Active Directory peut être un problème en raison de la Active Directory des objets tombstone.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Active Directory la restauration après une récupération d’urgence

Suite à un incident nécessitant une récupération d’urgence, le Active Directory peut être restauré dans le cadre de la restauration de l’état du système d’exploitation.

Cette opération de restauration est essentiellement une restauration en toute écriture.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Active Directory de la restauration sur le système sur lequel il s’exécute

Le système doit être redémarré en mode de restauration des services d’annuaire si le Active Directory est en cours d’exécution sur le serveur.

Le système d’exploitation s’exécute alors sans la Active Directory, et toute la validation de l’utilisateur se produit par le biais du gestionnaire de comptes de sécurité (SAM) dans le registre. Seul l’administrateur a l’autorisation de récupérer les Active Directory.

Une fois en mode de restauration du service d’annuaire, une restauration VSS peut se poursuivre normalement. Il n’y a aucune raison d’utiliser des API de Active Directory Win32 non-VSS pour restaurer l’état de Active Directory.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Active Directory restaure et Active Directory les objets tombstone

Tout plan de récupération doit s’assurer que l’ancienneté de la sauvegarde ne doit pas dépasser la durée de vie de désactivation Active Directory (60 jours par défaut).

La restauration d’une sauvegarde antérieure à l’objet tombstone entraînera un contrôleur de domaine à avoir des objets qui ne sont pas répliqués sur les autres serveurs.

Les objets qui ne sont pas répliqués ne sont pas supprimés automatiquement sur ce contrôleur de domaine (restauré), car les objets tombstone de ces objets sur les autres réplicas ont déjà été supprimés.

Un administrateur doit supprimer manuellement chacun des objets sur le contrôleur de domaine restauré qui ne sont pas répliqués. Les sauvegardes incrémentielles des Active Directory ne sont pas prises en charge ; une sauvegarde complète est nécessaire.

 

 



