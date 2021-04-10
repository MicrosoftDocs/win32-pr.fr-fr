---
title: Groupes sur les serveurs membres et Windows 2000 professionnel
description: Sur les serveurs membres et les ordinateurs qui exécutent Windows 2000 professionnel, il existe une base de données de sécurité locale.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Groupes sur les serveurs membres et Windows 2000 Professionnel AD
- groupes Active Directory, groupes sur les serveurs membres et Windows 2000 professionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309282"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a>Groupes sur les serveurs membres et Windows 2000 professionnel

Sur les serveurs membres et les ordinateurs qui exécutent Windows 2000 professionnel, il existe une base de données de sécurité locale. Cette base de données de sécurité locale peut contenir ses propres groupes locaux et d’utilisateurs locaux dont l’étendue est uniquement l’ordinateur particulier sur lequel elles sont créées. Lors de la gestion de ces types d’utilisateurs et de groupes sur les serveurs membres et les ordinateurs qui exécutent Windows NT Workstation ou Windows 2000 professionnel, utilisez le fournisseur Winnt.

Lorsqu’un serveur membre ou un ordinateur exécutant Windows 2000 Professionnel ou Windows 2000 professionnel est membre d’un domaine Windows 2000, les groupes ou les utilisateurs du domaine peuvent être utilisés dans la base de données de sécurité locale pour accorder des droits à ce groupe sur cet ordinateur particulier.

Lorsque vous gérez des groupes sur un domaine Windows 2000 à l’aide d’ADSI, utilisez le fournisseur LDAP. Lorsque vous gérez des groupes sur des serveurs membres et des ordinateurs qui exécutent Windows NT Workstation ou Windows 2000 professionnel, utilisez le fournisseur Winnt.

Vous devez lier au moins une instance à chaque fournisseur : 1) créer une liaison avec le fournisseur LDAP pour récupérer l’ADsPath du groupe ou de l’utilisateur que vous souhaitez ajouter à un groupe dans la base de données locale et 2) créer une liaison avec le fournisseur WinNT pour ajouter cet utilisateur ou ce groupe à un groupe local.

 

 




