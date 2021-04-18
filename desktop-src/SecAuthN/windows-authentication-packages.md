---
description: Les packages d’authentification Windows fournissent des services d’authentification en implémentant des fonctionnalités spécifiques aux packages pour les fonctions LsaLogonUser et LsaCallAuthenticationPackage fournies par l’autorité LSA.
ms.assetid: 71f7eccd-694d-475f-b6d0-1eaf9ac468f5
title: Packages d’authentification Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4b14f74ad466e0010f7ab5ac766af908a7b4704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525845"
---
# <a name="windows-authentication-packages"></a>Packages d’authentification Windows

Les packages d’authentification Windows fournissent des services d’authentification en implémentant des fonctionnalités spécifiques aux packages pour les fonctions [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) et [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) fournies par l’autorité LSA.

MSV1 \_ 0 est un exemple de package d' [*authentification*](../secgloss/a-gly.md)Windows. Le \_ package MSV1 0 accepte un nom d’utilisateur et un mot de passe [*haché*](../secgloss/h-gly.md) , qu’il recherche dans la base de données du gestionnaire de [*comptes de sécurité*](../secgloss/s-gly.md) (Sam). En fonction des résultats de la recherche, le \_ package d’authentification MSV1 0 accepte ou rejette la tentative d’authentification.

Pour obtenir la liste des fonctions de prise en charge que le LSA fournit pour une utilisation par les packages d’authentification Windows qui requièrent des services système, consultez [LSA, fonctions appelées par les packages d’authentification](authentication-functions.md).

Les packages d’authentification Windows doivent implémenter un ensemble de fonctions qui sont appelées par le LSA. Pour obtenir la liste complète des fonctions, consultez [fonctions implémentées par les packages d’authentification](authentication-functions.md).

 

 
