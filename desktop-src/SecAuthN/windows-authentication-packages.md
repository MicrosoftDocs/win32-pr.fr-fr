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
# <a name="windows-authentication-packages"></a><span data-ttu-id="6a5aa-103">Packages d’authentification Windows</span><span class="sxs-lookup"><span data-stu-id="6a5aa-103">Windows Authentication Packages</span></span>

<span data-ttu-id="6a5aa-104">Les packages d’authentification Windows fournissent des services d’authentification en implémentant des fonctionnalités spécifiques aux packages pour les fonctions [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) et [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) fournies par l’autorité LSA.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-104">Windows authentication packages provide authentication services by implementing package-specific functionality for the [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) and [**LsaCallAuthenticationPackage**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) functions provided by the LSA.</span></span>

<span data-ttu-id="6a5aa-105">MSV1 \_ 0 est un exemple de package d' [*authentification*](../secgloss/a-gly.md)Windows.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-105">MSV1\_0 is an example of a Windows [*authentication package*](../secgloss/a-gly.md).</span></span> <span data-ttu-id="6a5aa-106">Le \_ package MSV1 0 accepte un nom d’utilisateur et un mot de passe [*haché*](../secgloss/h-gly.md) , qu’il recherche dans la base de données du gestionnaire de [*comptes de sécurité*](../secgloss/s-gly.md) (Sam).</span><span class="sxs-lookup"><span data-stu-id="6a5aa-106">The MSV1\_0 package accepts a user name and a [*hashed*](../secgloss/h-gly.md) password, which it looks up in the [*Security Accounts Manager*](../secgloss/s-gly.md) (SAM) database.</span></span> <span data-ttu-id="6a5aa-107">En fonction des résultats de la recherche, le \_ package d’authentification MSV1 0 accepte ou rejette la tentative d’authentification.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-107">Depending on the results of the lookup, the MSV1\_0 authentication package accepts or rejects the authentication attempt.</span></span>

<span data-ttu-id="6a5aa-108">Pour obtenir la liste des fonctions de prise en charge que le LSA fournit pour une utilisation par les packages d’authentification Windows qui requièrent des services système, consultez [LSA, fonctions appelées par les packages d’authentification](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6a5aa-108">For a list of the support functions the LSA provides for use by Windows authentication packages that require system services, see [LSA Functions Called by Authentication Packages](authentication-functions.md).</span></span>

<span data-ttu-id="6a5aa-109">Les packages d’authentification Windows doivent implémenter un ensemble de fonctions qui sont appelées par le LSA.</span><span class="sxs-lookup"><span data-stu-id="6a5aa-109">Windows authentication packages must implement a set of functions that are called by the LSA.</span></span> <span data-ttu-id="6a5aa-110">Pour obtenir la liste complète des fonctions, consultez [fonctions implémentées par les packages d’authentification](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6a5aa-110">For the complete list of functions, see [Functions Implemented by Authentication Packages](authentication-functions.md).</span></span>

 

 
