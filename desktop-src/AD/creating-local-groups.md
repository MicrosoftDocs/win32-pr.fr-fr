---
title: Création de groupes locaux
description: Seuls les groupes locaux peuvent être créés pour les serveurs membres et Windows 2000 professionnel.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Création de groupes locaux Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314639"
---
# <a name="creating-local-groups"></a>Création de groupes locaux

Seuls les groupes locaux peuvent être créés pour les serveurs membres et Windows 2000 professionnel.

**Pour créer un groupe local pour un serveur membre ou un ordinateur exécutant Windows 2000 professionnel**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ».

        Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom des groupes d’ordinateurs auxquels accéder.

        Dans la chaîne de liaison, le &lt; paramètre « Computer &gt; » indique à ADSI qu’il est lié à un ordinateur. ADSI met ces données à la disposition de l’analyseur du fournisseur Winnt afin qu’il puisse ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.

    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Spécifiez « localGroup » en tant que classe à l’aide de [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) pour ajouter le groupe.
    > [!Note]  
    > Si vous spécifiez « Group » comme classe, ADSI utilise « localGroup ». Ne spécifiez pas la classe en tant que « globalGroup ». Les groupes de la classe « globalGroup » ne peuvent pas être créés sur des serveurs membres ou sur un ordinateur exécutant Windows NT Workstation ou Windows 2000 professionnel. Si vous spécifiez « globalGroup », [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) crée le groupe dans le cache de propriétés, mais [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) n’écrit pas le groupe dans la base de données de sécurité et ne retourne pas d’erreur.

     

3.  Écrivez le groupe dans la base de données de sécurité de l’ordinateur à l’aide de [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 