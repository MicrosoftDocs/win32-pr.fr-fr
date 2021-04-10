---
title: Suppression d’utilisateurs sur les serveurs membres et Windows 2000 professionnel
description: Cette rubrique montre comment supprimer un utilisateur d’un serveur membre ou d’un ordinateur exécutant Windows 2000 professionnel.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- utilisateurs Active Directory, suppression d’un utilisateur sur les serveurs membres et Windows 2000 professionnel
- Active Directory, utilisation de, utilisateurs, suppression d’utilisateurs sur les serveurs membres et Windows 2000 professionnel
- suppression d’un utilisateur
- serveur, suppression d’un utilisateur
- suppression d’utilisateurs sur les serveurs membres et la publicité Windows 2000 professionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae4287c8b7d32e15e7df3e73f365409d7fe49a0
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031020"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>Suppression d’utilisateurs sur les serveurs membres et Windows 2000 professionnel

Cette rubrique montre comment supprimer un utilisateur d’un serveur membre ou d’un ordinateur exécutant Windows 2000 professionnel.

**Pour supprimer un utilisateur**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ». Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom de l’ordinateur dont vous souhaitez accéder aux groupes. Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.
    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Spécifiez « User » comme classe à l’aide de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) pour supprimer l’utilisateur.

    N’oubliez pas que vous n’avez pas besoin d’appeler [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider la modification apportée au conteneur. L’appel de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) valide la suppression de l’utilisateur directement dans le répertoire.

 

 