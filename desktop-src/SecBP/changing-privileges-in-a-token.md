---
description: Explique comment modifier des privilèges dans un jeton à l’aide des fonctions AdjustTokenPrivileges et CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Modification des privilèges dans un jeton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536849"
---
# <a name="changing-privileges-in-a-token"></a><span data-ttu-id="44b75-103">Modification des privilèges dans un jeton</span><span class="sxs-lookup"><span data-stu-id="44b75-103">Changing Privileges in a Token</span></span>

<span data-ttu-id="44b75-104">Vous pouvez modifier les privilèges dans un jeton principal ou un jeton d’emprunt d’identité de deux manières :</span><span class="sxs-lookup"><span data-stu-id="44b75-104">You can change the privileges in either a primary or an impersonation token in two ways:</span></span>

-   <span data-ttu-id="44b75-105">Activez ou désactivez les privilèges à l’aide de la fonction [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="44b75-105">Enable or disable privileges by using the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>
-   <span data-ttu-id="44b75-106">Limitez ou supprimez des privilèges à l’aide de la fonction [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .</span><span class="sxs-lookup"><span data-stu-id="44b75-106">Restrict or remove privileges by using the [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) function.</span></span>

<span data-ttu-id="44b75-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) ne peut pas ajouter ou supprimer des privilèges du jeton.</span><span class="sxs-lookup"><span data-stu-id="44b75-107">[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) cannot add or remove privileges from the token.</span></span> <span data-ttu-id="44b75-108">Il peut uniquement activer des privilèges existants qui sont actuellement désactivés ou désactiver des privilèges existants actuellement activés.</span><span class="sxs-lookup"><span data-stu-id="44b75-108">It can only enable existing privileges that are currently disabled or disable existing privileges that are currently enabled.</span></span> <span data-ttu-id="44b75-109">Pour obtenir des exemples, consultez [activation et désactivation des privilèges en C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="44b75-109">For examples, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

<span data-ttu-id="44b75-110">Pour affecter des privilèges à un compte d’utilisateur, consultez [attribution de privilèges à un compte](assigning-privileges-to-an-account.md).</span><span class="sxs-lookup"><span data-stu-id="44b75-110">To assign privileges to a user account, see [Assigning Privileges to an Account](assigning-privileges-to-an-account.md).</span></span>

<span data-ttu-id="44b75-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) dispose de fonctionnalités plus étendues, comme suit :</span><span class="sxs-lookup"><span data-stu-id="44b75-111">[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) has more extensive capabilities as follows:</span></span>

-   <span data-ttu-id="44b75-112">Suppression d’un privilège.</span><span class="sxs-lookup"><span data-stu-id="44b75-112">Removing a privilege.</span></span> <span data-ttu-id="44b75-113">Notez que la suppression d’un privilège n’est pas la même que la désactivation d’un.</span><span class="sxs-lookup"><span data-stu-id="44b75-113">Note that removing a privilege is not the same as disabling one.</span></span> <span data-ttu-id="44b75-114">Une fois qu’un privilège a été supprimé d’un jeton, il ne peut pas être remis.</span><span class="sxs-lookup"><span data-stu-id="44b75-114">After a privilege is removed from a token, it cannot be put back.</span></span>
-   <span data-ttu-id="44b75-115">Attachement de l’attribut de refus uniquement aux sid dans le jeton.</span><span class="sxs-lookup"><span data-stu-id="44b75-115">Attaching the deny-only attribute to SIDs in the token.</span></span> <span data-ttu-id="44b75-116">Cela a pour effet d’interdire des groupes ou des comptes spécifiques, par exemple, en refusant au groupe tout le monde de supprimer l’accès à un fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="44b75-116">This has the effect of disallowing specific groups or accounts, for example, denying the Everyone group delete access to a particular file.</span></span> <span data-ttu-id="44b75-117">Pour plus d’informations sur la restriction des SID, consultez [attributs SID dans un jeton d’accès](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span><span class="sxs-lookup"><span data-stu-id="44b75-117">For more information on restricting SIDs, see [SID Attributes in an Access Token](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).</span></span>
-   <span data-ttu-id="44b75-118">Spécification d’une liste de sid restreints dans le jeton.</span><span class="sxs-lookup"><span data-stu-id="44b75-118">Specifying a list of restricting SIDs in the token.</span></span> <span data-ttu-id="44b75-119">Pour plus d’informations sur la restriction des SID, consultez [jetons restreints](/windows/desktop/SecAuthZ/restricted-tokens).</span><span class="sxs-lookup"><span data-stu-id="44b75-119">For information about restricting SIDs, see [Restricted Tokens](/windows/desktop/SecAuthZ/restricted-tokens).</span></span>

 

 
