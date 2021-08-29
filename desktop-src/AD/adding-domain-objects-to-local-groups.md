---
title: Ajout d’objets de domaine aux groupes locaux
description: Les utilisateurs et les groupes qui appartiennent au domaine peuvent être ajoutés à des groupes sur l’ordinateur local pour accorder des droits à l’utilisateur ou au groupe de domaine sur cet ordinateur particulier.
ms.assetid: 07287190-88a1-4d4d-a91c-1e95d9903a4d
ms.tgt_platform: multiple
keywords:
- Active Directory exemples Active Directory, ajout d’objets de domaine aux groupes locaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fee2a90569b7a0d41db6e0654b675e7eb768ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880302"
---
# <a name="adding-domain-objects-to-local-groups"></a>Ajout d’objets de domaine aux groupes locaux

lorsqu’un serveur membre ou un ordinateur qui s’exécute sur Windows 2000 Professional est membre d’un domaine Windows 2000, les utilisateurs et les groupes qui appartiennent au domaine peuvent être ajoutés à des groupes sur l’ordinateur local pour accorder des droits à l’utilisateur ou au groupe de domaine sur cet ordinateur particulier.

lorsque vous gérez des groupes locaux de domaine sur un domaine Windows 2000 à l’aide d’ADSI, le fournisseur LDAP est normalement utilisé. toutefois, lorsque vous gérez des groupes locaux sur des serveurs membres et un ordinateur exécutant Windows 2000 Professional, le fournisseur winnt doit être utilisé.

seuls les groupes locaux peuvent être créés sur les serveurs membres et Windows Professional 2000. Toutefois, les groupes locaux peuvent contenir :

-   Groupes universels et globaux de la forêt qui contient le domaine dont l’ordinateur est membre.
-   Groupes locaux de domaine de ce domaine d’ordinateur.
-   Utilisateurs de n’importe quel domaine de la forêt.

**Pour ajouter un objet de domaine à un groupe local**

1.  Liez à l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) de l’ordinateur qui contient le groupe local auquel ajouter un membre. La liaison doit être effectuée à l’aide d’un compte disposant des droits suffisants pour accéder à cet ordinateur. La chaîne de liaison doit prendre la forme « WinNT:// <computer name> , Computer », où « &lt; Computer Name &gt; » est le nom du groupe d’ordinateurs auquel ajouter un membre. Le paramètre « ordinateur » indique à ADSI qu’il est lié à un ordinateur. ADSI expose ces données à l’analyseur du fournisseur Winnt afin qu’il puisse ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez. Cela permet à l’utilisateur d’attendre 5 à 20 secondes d’attendre la résolution de l’ambiguïté.
2.  Utilisez la méthode [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) avec « Group » comme classe et le nom du groupe local comme nom de l’objet à lier au groupe.
3.  Crée une liaison avec l’interface [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) du groupe local auquel un membre sera ajouté.
4.  Construisez l’ADsPath de l’objet à ajouter au groupe local sous la forme « Winnt:// &lt; Domain &gt; / &lt; name &gt; », où « &lt; Domain &gt; » est le nom du domaine qui contient l’objet à ajouter et « &lt; name &gt; » est le nom de l’objet à ajouter.
5.  Ajoutez l’utilisateur ou le groupe au groupe local à l’aide de la méthode [**IADsGroup. Add**](/windows/desktop/api/iads/nf-iads-iadsgroup-add) , en passant l’ADsPath créé à l’étape 4.

Pour plus d’informations et pour obtenir un exemple de code qui montre comment ajouter un objet de groupe ou d’utilisateur de domaine à un groupe local, consultez l' [exemple de code pour l’ajout d’un groupe ou d’un utilisateur de domaine à un groupe local](example-code-for-adding-a-domain-user-or-group-to-a-local-group.md).

 

 
