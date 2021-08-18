---
description: les packages d’authentification Windows fournissent des services d’authentification en implémentant des fonctionnalités spécifiques aux packages pour les fonctions LsaLogonUser et LsaCallAuthenticationPackage fournies par l’autorité LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Windows Packages d’authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8288e54398702994938627b13c745a67f96fbc44dc710e2e5a7ac65a8620685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915078"
---
# <a name="windows-authentication-packages"></a>Windows Packages d’authentification

les packages d’authentification Windows fournissent des services d’authentification en implémentant des fonctionnalités spécifiques aux packages pour les fonctions [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) et [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) fournies par l’autorité LSA.

MSV1 \_ 0 est un exemple de package d' [*authentification*](../secgloss/a-gly.md)Windows. Le \_ package MSV1 0 accepte un nom d’utilisateur et un mot de passe [*haché*](../secgloss/h-gly.md) , qu’il recherche dans la base de données du gestionnaire de [*comptes de sécurité*](../secgloss/s-gly.md) (Sam). En fonction des résultats de la recherche, le \_ package d’authentification MSV1 0 accepte ou rejette la tentative d’authentification.

pour obtenir la liste des fonctions de prise en charge que le LSA fournit pour une utilisation par Windows les packages d’authentification qui requièrent des services système, consultez [lsa, fonctions appelées par les packages d’authentification](authentication-functions.md).

Windows les packages d’authentification doivent implémenter un ensemble de fonctions qui sont appelées par le LSA. Pour obtenir la liste complète des fonctions, consultez [fonctions implémentées par les packages d’authentification](authentication-functions.md).

 

 
