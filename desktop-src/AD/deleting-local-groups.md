---
title: Suppression de groupes locaux
description: cette rubrique montre comment supprimer un groupe local d’un serveur membre ou d’un ordinateur s’exécutant sur Windows 2000 Professional.
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- Suppression des groupes locaux Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe960804e083ecaf8ef12e412a43b7b8db4800f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881475"
---
# <a name="deleting-local-groups"></a>Suppression de groupes locaux

cette rubrique montre comment supprimer un groupe local d’un serveur membre ou d’un ordinateur s’exécutant sur Windows 2000 Professional.

**Pour supprimer un groupe local**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> , &lt; Computer &gt; ». Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom du groupe d’ordinateurs auquel accéder. Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.
    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Spécifiez « Group » comme classe à l’aide de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)pour supprimer le groupe.

    Vous n’avez pas besoin d’appeler [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider la modification apportée au conteneur. L’appel de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) valide la suppression du groupe directement dans le répertoire.

 

 
