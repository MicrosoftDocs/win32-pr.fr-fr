---
title: Classe Win32_RDMSEnvironment
description: Gère un environnement Bureau à distance Management Services (RDMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Win32_RDMSEnvironment de la classe Services Bureau à distance
- Win32_RDMSEnvironment de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509712"
---
# <a name="win32_rdmsenvironment-class"></a><span data-ttu-id="60c7c-105">\_Classe RDMSEnvironment Win32</span><span class="sxs-lookup"><span data-stu-id="60c7c-105">Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="60c7c-106">Gère un environnement Bureau à distance Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="60c7c-106">Manages a Remote Desktop Management Services (RDMS) environment.</span></span>

<span data-ttu-id="60c7c-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="60c7c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="60c7c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60c7c-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a><span data-ttu-id="60c7c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="60c7c-109">Members</span></span>

<span data-ttu-id="60c7c-110">La classe **Win32 \_ RDMSEnvironment** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="60c7c-110">The **Win32\_RDMSEnvironment** class has these types of members:</span></span>

-   [<span data-ttu-id="60c7c-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="60c7c-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="60c7c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="60c7c-112">Methods</span></span>

<span data-ttu-id="60c7c-113">La classe **Win32 \_ RDMSEnvironment** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="60c7c-113">The **Win32\_RDMSEnvironment** class has these methods.</span></span>



| <span data-ttu-id="60c7c-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="60c7c-114">Method</span></span>                                                                   | <span data-ttu-id="60c7c-115">Description</span><span class="sxs-lookup"><span data-stu-id="60c7c-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60c7c-116">**GetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="60c7c-116">**GetActiveServer**</span></span>](getactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="60c7c-117">Récupère le nom de domaine complet (FQDN) de l’environnement RDMS.</span><span class="sxs-lookup"><span data-stu-id="60c7c-117">Retrieves the fully qualified domain name (FQDN) of the RDMS environment.</span></span><br/>                 |
| [<span data-ttu-id="60c7c-118">**GetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="60c7c-118">**GetClientAccessName**</span></span>](getclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="60c7c-119">Récupère le nom de l’enregistrement de ressource (RR) DNS (Domain Name System) de l’environnement RDMS.</span><span class="sxs-lookup"><span data-stu-id="60c7c-119">Retrieves the Domain Name System (DNS) resource record (RR) name of the RDMS environment.</span></span><br/> |
| [<span data-ttu-id="60c7c-120">**SetActiveServer**</span><span class="sxs-lookup"><span data-stu-id="60c7c-120">**SetActiveServer**</span></span>](setactiveserver-win32-rdmsenvironment.md)         | <span data-ttu-id="60c7c-121">Définit le nom de domaine complet de l’environnement RDMS sur le nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="60c7c-121">Sets the FQDN of the RDMS environment to the current node.</span></span><br/>                                |
| [<span data-ttu-id="60c7c-122">**SetClientAccessName**</span><span class="sxs-lookup"><span data-stu-id="60c7c-122">**SetClientAccessName**</span></span>](setclientaccessname-win32-rdmsenvironment.md) | <span data-ttu-id="60c7c-123">Met à jour le nom de l’enregistrement de ressource DNS de l’environnement RDMS.</span><span class="sxs-lookup"><span data-stu-id="60c7c-123">Updates the DNS RR name of the RDMS environment.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="60c7c-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60c7c-124">Requirements</span></span>



| <span data-ttu-id="60c7c-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60c7c-125">Requirement</span></span> | <span data-ttu-id="60c7c-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="60c7c-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="60c7c-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60c7c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="60c7c-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="60c7c-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="60c7c-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60c7c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="60c7c-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60c7c-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="60c7c-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60c7c-131">Namespace</span></span><br/>                | <span data-ttu-id="60c7c-132">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="60c7c-132">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="60c7c-133">MOF</span><span class="sxs-lookup"><span data-stu-id="60c7c-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60c7c-134"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60c7c-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="60c7c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="60c7c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60c7c-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60c7c-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="60c7c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60c7c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60c7c-138">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="60c7c-138">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





