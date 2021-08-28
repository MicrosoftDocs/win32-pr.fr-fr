---
title: groupes sur les serveurs membres et Windows 2000 Professional
description: sur les serveurs membres et les ordinateurs qui s’exécutent sur Windows 2000 Professional, il existe une base de données de sécurité locale.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- groupes sur les serveurs membres et Windows 2000 Professional AD
- groupes active directory, groupes sur les serveurs membres et Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e376faf96621018867e46ac021e4aeab6e7fef6cd4e304d26902cb15a4d081f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692916"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a>groupes sur les serveurs membres et Windows 2000 Professional

sur les serveurs membres et les ordinateurs qui s’exécutent sur Windows 2000 Professional, il existe une base de données de sécurité locale. Cette base de données de sécurité locale peut contenir ses propres groupes locaux et d’utilisateurs locaux dont l’étendue est uniquement l’ordinateur particulier sur lequel elles sont créées. lorsque vous gérez ces types d’utilisateurs et de groupes sur des serveurs membres et des ordinateurs s’exécutant sur Windows NT Workstation ou Windows 2000 Professional, utilisez le fournisseur winnt.

lorsqu’un serveur membre ou un ordinateur s’exécutant sur Windows 2000 Professional ou Windows 2000 Professional est membre d’un domaine Windows 2000, les groupes ou utilisateurs du domaine peuvent être utilisés dans la base de données de sécurité locale pour accorder des droits à ce groupe sur cet ordinateur particulier.

lorsque vous gérez des groupes sur un domaine Windows 2000 à l’aide d’ADSI, utilisez le fournisseur LDAP. lorsque vous gérez des groupes sur des serveurs membres et des ordinateurs s’exécutant sur Windows NT Workstation ou Windows 2000 Professional, utilisez le fournisseur winnt.

Vous devez lier au moins une instance à chaque fournisseur : 1) créer une liaison avec le fournisseur LDAP pour récupérer l’ADsPath du groupe ou de l’utilisateur que vous souhaitez ajouter à un groupe dans la base de données locale et 2) créer une liaison avec le fournisseur WinNT pour ajouter cet utilisateur ou ce groupe à un groupe local.

 

 




