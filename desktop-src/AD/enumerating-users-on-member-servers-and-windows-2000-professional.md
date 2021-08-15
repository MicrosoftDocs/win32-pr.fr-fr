---
title: énumération des utilisateurs sur les serveurs membres et les Windows 2000 Professional
description: cette rubrique montre comment énumérer tous les utilisateurs, dans une base de données de sécurité locale, sur des serveurs membres et des ordinateurs s’exécutant sur Windows 2000 Professional.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- énumération des utilisateurs sur les serveurs membres et Windows 2000 Professional AD
- utilisateurs active directory, énumération des utilisateurs sur les serveurs membres et Windows 2000 Professional
- Active Directory, utilisation de, utilisateurs, énumération des utilisateurs sur les serveurs membres et Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f72e38a00e0fcc4310f7b8498b0dda28d71231df7e65fcf2de9945f5feef2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694876"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>énumération des utilisateurs sur les serveurs membres et les Windows 2000 Professional

cette rubrique montre comment énumérer tous les utilisateurs, dans une base de données de sécurité locale, sur des serveurs membres et des ordinateurs s’exécutant sur Windows 2000 Professional.

**Pour énumérer les utilisateurs**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ». Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom de l’ordinateur pour lequel les groupes doivent accéder. Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.
    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Ajoutez « user » à la propriété [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) . L’énumération ne contient alors que les objets qui ont la classe d’objet « User ».
3.  Énumérez les objets. Pour chaque objet utilisateur, utilisez les méthodes de l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) pour lire les propriétés de l’utilisateur.

 

 