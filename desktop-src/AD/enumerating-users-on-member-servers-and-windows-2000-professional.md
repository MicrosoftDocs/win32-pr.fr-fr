---
title: Énumération des utilisateurs sur les serveurs membres et Windows 2000 professionnel
description: Cette rubrique montre comment énumérer tous les utilisateurs, dans une base de données de sécurité locale, sur des serveurs membres et des ordinateurs s’exécutant sur Windows 2000 professionnel.
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- Énumération des utilisateurs sur les serveurs membres et la publicité Windows 2000 professionnel
- utilisateurs Active Directory, énumération des utilisateurs sur les serveurs membres et Windows 2000 professionnel
- Active Directory, utilisation de, utilisateurs, énumération des utilisateurs sur les serveurs membres et Windows 2000 professionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664af51b7feb2e0b9a683664659eefda11c9cb9d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724549"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>Énumération des utilisateurs sur les serveurs membres et Windows 2000 professionnel

Cette rubrique montre comment énumérer tous les utilisateurs, dans une base de données de sécurité locale, sur des serveurs membres et des ordinateurs s’exécutant sur Windows 2000 professionnel.

**Pour énumérer les utilisateurs**

1.  Connectez-vous à l’ordinateur à l’aide des règles suivantes :
    1.  Utilisez un compte disposant des droits suffisants pour accéder à cet ordinateur.
    2.  Utilisez le format de chaîne de liaison suivant à l’aide du fournisseur WinNT, du nom d’ordinateur et d’un paramètre supplémentaire pour indiquer à ADSI qu’il est lié à un ordinateur : « WinNT:// <computer name> <computer> ». Le &lt; paramètre « nom &gt; de l’ordinateur » est le nom de l’ordinateur pour lequel les groupes doivent accéder. Ce paramètre indique à ADSI qu’il est lié à un ordinateur et permet à l’analyseur du fournisseur Winnt d’ignorer certaines requêtes de résolution d’ambiguïté pour déterminer le type d’objet auquel vous vous liez.
    3.  Crée une liaison avec l’interface [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .
2.  Ajoutez « user » à la propriété [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) . L’énumération ne contient alors que les objets qui ont la classe d’objet « User ».
3.  Énumérez les objets. Pour chaque objet utilisateur, utilisez les méthodes de l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) ou [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) pour lire les propriétés de l’utilisateur.

 

 