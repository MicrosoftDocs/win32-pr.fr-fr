---
title: création d’utilisateurs sur des serveurs membres et Windows 2000 Professional
description: cette rubrique décrit les étapes permettant de créer un utilisateur sur un serveur membre ou sur un ordinateur exécutant Windows 2000 Professional.
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- création d’utilisateurs sur des serveurs membres et Windows 2000 Professional AD
- utilisateurs active directory, création d’un utilisateur sur les serveurs membres et Windows 2000 Professional
- Active Directory, utilisation de, utilisateurs, création d’un utilisateur sur des serveurs membres et Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21490302b025e20f836cbbc957d0f86824b3456d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881581"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>création d’utilisateurs sur des serveurs membres et Windows 2000 Professional

**Pour créer un utilisateur**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> , &lt; Computer &gt; ». L' &lt; ordinateur « nom &gt; de l’ordinateur » est le nom de l’ordinateur dont vous souhaitez accéder aux groupes. Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.
    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Spécifiez « User » comme classe à l’aide de [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) pour ajouter l’utilisateur.
3.  Écrivez l’utilisateur dans la base de données de sécurité de l’ordinateur à l’aide de [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 
