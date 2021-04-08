---
title: Conversion des formats de nom de compte de domaine
description: Les fonctions Microsoft Win32 permettant d’utiliser le gestionnaire de contrôle des services (SCM) sur un serveur hôte utilisent le \ 0034 ; \\ nom d’utilisateur de domaine \ 0034 ; format pour les comptes de service.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724605"
---
# <a name="converting-domain-account-name-formats"></a><span data-ttu-id="e9cae-103">Conversion des formats de nom de compte de domaine</span><span class="sxs-lookup"><span data-stu-id="e9cae-103">Converting Domain Account Name Formats</span></span>

<span data-ttu-id="e9cae-104">Les fonctions Microsoft Win32 permettant d’utiliser le gestionnaire de contrôle des services (SCM) sur un serveur hôte utilisent le <domain> \\ <username> format «» pour les comptes de service.</span><span class="sxs-lookup"><span data-stu-id="e9cae-104">The Microsoft Win32 functions for working with the service control manager (SCM) on a host server use the "<domain>\\<username>" format for service accounts.</span></span> <span data-ttu-id="e9cae-105">Par exemple, si vous appelez la fonction [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) pour récupérer le compte d’utilisateur sous lequel votre service s’exécute, la fonction retourne le nom dans le format « Fabrikam \\ JeffSmith ».</span><span class="sxs-lookup"><span data-stu-id="e9cae-105">For example, if you call the [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) function to retrieve the user account under which your service runs, the function returns the name in "Fabrikam\\jeffsmith" format.</span></span> <span data-ttu-id="e9cae-106">Pour effectuer une liaison au compte d’utilisateur dans l’annuaire, par exemple pour modifier le mot de passe du compte, le nom unique du compte est requis, dont le format est « CN = Jeff Smith, CN = Users, DC = fabrikam, DC = COM ».</span><span class="sxs-lookup"><span data-stu-id="e9cae-106">To bind to the user account in the directory, for example to change the account password, the distinguished name of the account is required, which has the format "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM".</span></span>

<span data-ttu-id="e9cae-107">Pour effectuer une conversion entre les différents formats de noms, utilisez la fonction [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) , qui peut convertir un nom dans d’autres formats, par exemple un nom d’utilisateur principal (UPN).</span><span class="sxs-lookup"><span data-stu-id="e9cae-107">To convert between the various name formats, use the [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) function, which can convert a name to other formats, such as a user principal name (UPN).</span></span>

 

 