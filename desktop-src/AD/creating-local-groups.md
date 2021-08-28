---
title: Création de groupes locaux
description: seuls les groupes locaux peuvent être créés pour les serveurs membres et Windows Professional 2000.
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- Création de groupes locaux Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06410572e6e5897280b2a03c99b387dbf81b3cca
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881590"
---
# <a name="creating-local-groups"></a>Création de groupes locaux

seuls les groupes locaux peuvent être créés pour les serveurs membres et Windows Professional 2000.

**pour créer un groupe local pour un serveur membre ou un ordinateur exécutant Windows 2000 Professional**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> , &lt; Computer &gt; ».

        Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom des groupes d’ordinateurs auxquels accéder.

        Dans la chaîne de liaison, le &lt; paramètre « Computer &gt; » indique à ADSI qu’il est lié à un ordinateur. ADSI met ces données à la disposition de l’analyseur du fournisseur Winnt afin qu’il puisse ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.

    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .

2.  Spécifiez « localGroup » en tant que classe à l’aide de [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) pour ajouter le groupe.
    > [!Note]  
    > Si vous spécifiez « Group » comme classe, ADSI utilise « localGroup ». Ne spécifiez pas la classe en tant que « globalGroup ». les groupes de la classe « globalGroup » ne peuvent pas être créés sur des serveurs membres ou sur un ordinateur exécutant Windows NT Workstation/Windows 2000 Professional. Si vous spécifiez « globalGroup », [**IADsContainer. Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) crée le groupe dans le cache de propriétés, mais [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) n’écrit pas le groupe dans la base de données de sécurité et ne retourne pas d’erreur.

     

3.  Écrivez le groupe dans la base de données de sécurité de l’ordinateur à l’aide de [**IADs. setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).

 

 
