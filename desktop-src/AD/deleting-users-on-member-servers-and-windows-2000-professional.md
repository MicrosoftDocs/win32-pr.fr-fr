---
title: suppression des utilisateurs sur les serveurs membres et les Windows 2000 Professional
description: cette rubrique montre comment supprimer un utilisateur d’un serveur membre ou d’un ordinateur s’exécutant sur Windows 2000 Professional.
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- utilisateurs active directory, suppression d’un utilisateur sur les serveurs membres et Windows 2000 Professional
- Active Directory, utilisation de, utilisateurs, suppression d’utilisateurs sur les serveurs membres et Windows 2000 Professional
- suppression d’un utilisateur
- serveur, suppression d’un utilisateur
- suppression d’utilisateurs sur les serveurs membres et la publicité Windows 2000 professionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e366356696c1e8b11a53b45aae3860600fc6555
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881457"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>suppression des utilisateurs sur les serveurs membres et les Windows 2000 Professional

cette rubrique montre comment supprimer un utilisateur d’un serveur membre ou d’un ordinateur s’exécutant sur Windows 2000 Professional.

**Pour supprimer un utilisateur**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> , &lt; Computer &gt; ». Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom de l’ordinateur dont vous souhaitez accéder aux groupes. Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.
    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Spécifiez « User » comme classe à l’aide de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) pour supprimer l’utilisateur.

    N’oubliez pas que vous n’avez pas besoin d’appeler [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) pour valider la modification apportée au conteneur. L’appel de [**IADsContainer. Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) valide la suppression de l’utilisateur directement dans le répertoire.

 

 
