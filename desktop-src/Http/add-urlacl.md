---
title: add urlacl
description: Réserve l’URL spécifiée pour les comptes et les utilisateurs non-administrateurs.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Ajouter urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103953785"
---
# <a name="add-urlacl"></a><span data-ttu-id="9de20-104">add urlacl</span><span class="sxs-lookup"><span data-stu-id="9de20-104">add urlacl</span></span>

<span data-ttu-id="9de20-105">Réserve l’URL spécifiée pour les comptes et les utilisateurs non-administrateurs.</span><span class="sxs-lookup"><span data-stu-id="9de20-105">Reserves the specified URL for non-administrator users and accounts.</span></span> <span data-ttu-id="9de20-106">La liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List) peut être spécifiée à l’aide d’un nom de compte avec les paramètres Listen et Delegate ou à l’aide d’une chaîne SDDL (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="9de20-106">The discretionary access control list (DACL) can be specified by using an account name with the listen and delegate parameters or by using a security descriptor definition language (SDDL) string.</span></span>

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a><span data-ttu-id="9de20-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9de20-107">Parameters</span></span>

<dl> <span data-ttu-id="9de20-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] chaîne**
</dt> </span><span class="sxs-lookup"><span data-stu-id="9de20-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] string**
</dt> </span></span><dd>

<span data-ttu-id="9de20-109">Spécifie l’URL complète.</span><span class="sxs-lookup"><span data-stu-id="9de20-109">Specifies the fully qualified URL.</span></span>

<span data-ttu-id="9de20-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user =] chaîne**
</dt> </span><span class="sxs-lookup"><span data-stu-id="9de20-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> </span></span><dd>

<span data-ttu-id="9de20-111">Spécifie le nom d’utilisateur ou de groupe d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9de20-111">Specifies the user or user group name.</span></span>

</dd> <dt>

<span data-ttu-id="9de20-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[écouter = {oui \| non}\]**</span><span class="sxs-lookup"><span data-stu-id="9de20-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="9de20-113">Spécifie l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9de20-113">Specifies one of the following values:</span></span>

-   <span data-ttu-id="9de20-114">Oui : permet à l’utilisateur d’inscrire des URL.</span><span class="sxs-lookup"><span data-stu-id="9de20-114">yes: Allows the user to register URLs.</span></span> <span data-ttu-id="9de20-115">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9de20-115">This is the default value.</span></span>
-   <span data-ttu-id="9de20-116">non : refuse à l’utilisateur d’inscrire des URL.</span><span class="sxs-lookup"><span data-stu-id="9de20-116">no: Denies the user from registering URLs.</span></span>

</dd> <dt>

<span data-ttu-id="9de20-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[délégué = {oui \| non}\]**</span><span class="sxs-lookup"><span data-stu-id="9de20-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="9de20-118">Spécifie l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="9de20-118">Specifies one of the following values:</span></span>

-   <span data-ttu-id="9de20-119">Oui : permet à l’utilisateur de déléguer des URL.</span><span class="sxs-lookup"><span data-stu-id="9de20-119">yes: Allows the user to delegate URLs.</span></span>
-   <span data-ttu-id="9de20-120">non : refuse à l’utilisateur de déléguer des URL.</span><span class="sxs-lookup"><span data-stu-id="9de20-120">no: Denies the user from delegating URLs.</span></span> <span data-ttu-id="9de20-121">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9de20-121">This is the default value.</span></span>

<span data-ttu-id="9de20-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] chaîne**
</dt> </span><span class="sxs-lookup"><span data-stu-id="9de20-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> </span></span><dd>

<span data-ttu-id="9de20-123">Spécifie la chaîne SDDL qui décrit la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="9de20-123">Specifies the SDDL string that describes the DACL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9de20-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="9de20-124">Examples</span></span>

* <span data-ttu-id="9de20-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\ user</span><span class="sxs-lookup"><span data-stu-id="9de20-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\user</span></span>

* <span data-ttu-id="9de20-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span><span class="sxs-lookup"><span data-stu-id="9de20-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span></span>

* <span data-ttu-id="9de20-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span><span class="sxs-lookup"><span data-stu-id="9de20-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span></span>

 
## <a name="see-also"></a><span data-ttu-id="9de20-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9de20-128">See Also</span></span>

* [<span data-ttu-id="9de20-129">Commandes Netsh http</span><span class="sxs-lookup"><span data-stu-id="9de20-129">Netsh http commands</span></span>](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 