---
description: Quand une application utilise l’API de gestion des informations d’identification pour demander des informations d’identification, l’utilisateur doit entrer des informations qui peuvent être validées, soit par le système d’exploitation, soit par l’application.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formats de nom d’utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518815"
---
# <a name="user-name-formats"></a><span data-ttu-id="052a8-103">Formats de nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="052a8-103">User Name Formats</span></span>

<span data-ttu-id="052a8-104">Quand une application utilise l’API de gestion des informations d’identification pour demander des informations d’identification, l’utilisateur doit entrer des informations qui peuvent être validées, soit par le système d’exploitation, soit par l’application.</span><span class="sxs-lookup"><span data-stu-id="052a8-104">When an application uses the Credentials Management API to prompt for credentials, the user is expected to enter information that can be validated, either by the operating system or by the application.</span></span> <span data-ttu-id="052a8-105">L’utilisateur peut spécifier les informations d’identification de domaine dans l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="052a8-105">The user can specify domain credentials information in one of the following formats:</span></span>

-   [<span data-ttu-id="052a8-106">Nom d'utilisateur principal</span><span class="sxs-lookup"><span data-stu-id="052a8-106">User Principal Name</span></span>](#user-principal-name)
-   [<span data-ttu-id="052a8-107">Nom d’ouverture de session de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="052a8-107">Down-Level Logon Name</span></span>](#down-level-logon-name)

## <a name="user-principal-name"></a><span data-ttu-id="052a8-108">Nom d’utilisateur principal</span><span class="sxs-lookup"><span data-stu-id="052a8-108">User Principal Name</span></span>

<span data-ttu-id="052a8-109">Le format UPN ( [*user principal name*](../secgloss/u-gly.md) ) est utilisé pour spécifier un nom de style Internet, tel que <b>UserName@Example.Microsoft.com</b> .</span><span class="sxs-lookup"><span data-stu-id="052a8-109">[*User principal name*](../secgloss/u-gly.md) (UPN) format is used to specify an Internet-style name, such as <b>UserName@Example.Microsoft.com</b>.</span></span> <span data-ttu-id="052a8-110">Le tableau suivant récapitule les parties d’un UPN.</span><span class="sxs-lookup"><span data-stu-id="052a8-110">The following table summarizes the parts of a UPN.</span></span>



| <span data-ttu-id="052a8-111">Partie</span><span class="sxs-lookup"><span data-stu-id="052a8-111">Part</span></span>                                                        | <span data-ttu-id="052a8-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="052a8-112">Example</span></span>                                |
|-------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="052a8-113">Nom du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="052a8-113">User account name.</span></span> <span data-ttu-id="052a8-114">Également appelé nom d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="052a8-114">Also known as the logon name.</span></span><br/> | <span data-ttu-id="052a8-115">*UserName*</span><span class="sxs-lookup"><span data-stu-id="052a8-115">*UserName*</span></span><br/>                  |
| <span data-ttu-id="052a8-116">Séparateur.</span><span class="sxs-lookup"><span data-stu-id="052a8-116">Separator.</span></span> <span data-ttu-id="052a8-117">Un littéral de caractère, le signe arobase (@).</span><span class="sxs-lookup"><span data-stu-id="052a8-117">A character literal, the at sign (@).</span></span><br/> | @<br/>                           |
| <span data-ttu-id="052a8-118">Suffixe UPN.</span><span class="sxs-lookup"><span data-stu-id="052a8-118">UPN suffix.</span></span> <span data-ttu-id="052a8-119">Également appelé nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="052a8-119">Also known as the domain name.</span></span><br/>       | <span data-ttu-id="052a8-120">*Example.Microsoft.com*</span><span class="sxs-lookup"><span data-stu-id="052a8-120">*Example.Microsoft.com*</span></span> <br/> |



 

<span data-ttu-id="052a8-121">Un UPN peut être défini implicitement ou explicitement.</span><span class="sxs-lookup"><span data-stu-id="052a8-121">A UPN can be implicitly or explicitly defined.</span></span> <span data-ttu-id="052a8-122">Un UPN implicite est de la forme <b>UserName@DNSDomainName.com</b> .</span><span class="sxs-lookup"><span data-stu-id="052a8-122">An implicit UPN is of the form <b>UserName@DNSDomainName.com</b>.</span></span> <span data-ttu-id="052a8-123">Un UPN implicite est toujours associé au compte de l’utilisateur, même si un UPN explicite n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="052a8-123">An implicit UPN is always associated with the user's account, even if an explicit UPN is not defined.</span></span> <span data-ttu-id="052a8-124">Un UPN explicite est de la forme <i><b>Name@Suffix</b></i> , où les chaînes de nom et de suffixe sont définies explicitement par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="052a8-124">An explicit UPN is of the form <i><b>Name@Suffix</b></i>, where both the name and suffix strings are explicitly defined by the administrator.</span></span>

## <a name="down-level-logon-name"></a><span data-ttu-id="052a8-125">Nom d’ouverture de session Down-Level</span><span class="sxs-lookup"><span data-stu-id="052a8-125">Down-Level Logon Name</span></span>

<span data-ttu-id="052a8-126">Le format du nom d’ouverture de session de niveau supérieur est utilisé pour spécifier un domaine et un compte d’utilisateur dans ce domaine, par exemple <i><b>domaine \\ NomUtilisateur</b></i>.</span><span class="sxs-lookup"><span data-stu-id="052a8-126">The down-level logon name format is used to specify a domain and a user account in that domain, for example, <i><b>DOMAIN\\UserName</b></i>.</span></span> <span data-ttu-id="052a8-127">Le tableau suivant récapitule les parties d’un nom d’ouverture de session de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="052a8-127">The following table summarizes the parts of a down-level logon name.</span></span>



| <span data-ttu-id="052a8-128">Partie</span><span class="sxs-lookup"><span data-stu-id="052a8-128">Part</span></span>                                                           | <span data-ttu-id="052a8-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="052a8-129">Example</span></span>               |
|----------------------------------------------------------------|-----------------------|
| <span data-ttu-id="052a8-130">Nom de domaine NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="052a8-130">NetBIOS domain name.</span></span><br/>                                | <span data-ttu-id="052a8-131">*DOMAIN*</span><span class="sxs-lookup"><span data-stu-id="052a8-131">*DOMAIN*</span></span><br/>   |
| <span data-ttu-id="052a8-132">Séparateur.</span><span class="sxs-lookup"><span data-stu-id="052a8-132">Separator.</span></span> <span data-ttu-id="052a8-133">Littéral de caractère, la barre oblique inverse ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="052a8-133">A character literal, the backslash (\\).</span></span><br/> | **\\**<br/>     |
| <span data-ttu-id="052a8-134">Nom du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="052a8-134">User account name.</span></span> <span data-ttu-id="052a8-135">Également appelé nom d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="052a8-135">Also known as the logon name.</span></span><br/>    | <span data-ttu-id="052a8-136">*UserName*</span><span class="sxs-lookup"><span data-stu-id="052a8-136">*UserName*</span></span><br/> |



 

 

 
