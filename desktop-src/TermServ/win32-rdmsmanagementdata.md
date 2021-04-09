---
title: Classe Win32_RDMSManagementData
description: Synchronise les données de publication pour les services de gestion de Bureau à distance (RDMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Win32_RDMSManagementData de la classe Services Bureau à distance
- Win32_RDMSManagementData de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032452"
---
# <a name="win32_rdmsmanagementdata-class"></a><span data-ttu-id="c60f5-105">\_Classe RDMSManagementData Win32</span><span class="sxs-lookup"><span data-stu-id="c60f5-105">Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="c60f5-106">Synchronise les données de publication pour les services de gestion de Bureau à distance (RDMS).</span><span class="sxs-lookup"><span data-stu-id="c60f5-106">Synchronizes publishing data for Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="c60f5-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c60f5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c60f5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c60f5-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a><span data-ttu-id="c60f5-109">Membres</span><span class="sxs-lookup"><span data-stu-id="c60f5-109">Members</span></span>

<span data-ttu-id="c60f5-110">La classe **Win32 \_ RDMSManagementData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c60f5-110">The **Win32\_RDMSManagementData** class has these types of members:</span></span>

-   [<span data-ttu-id="c60f5-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c60f5-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c60f5-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c60f5-112">Methods</span></span>

<span data-ttu-id="c60f5-113">La classe **Win32 \_ RDMSManagementData** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c60f5-113">The **Win32\_RDMSManagementData** class has these methods.</span></span>



| <span data-ttu-id="c60f5-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="c60f5-114">Method</span></span>                                                                                        | <span data-ttu-id="c60f5-115">Description</span><span class="sxs-lookup"><span data-stu-id="c60f5-115">Description</span></span>                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="c60f5-116">**SynchronizeAllPublishingData**</span><span class="sxs-lookup"><span data-stu-id="c60f5-116">**SynchronizeAllPublishingData**</span></span>](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | <span data-ttu-id="c60f5-117">Synchronise toutes les données de publication pour les RDM.</span><span class="sxs-lookup"><span data-stu-id="c60f5-117">Synchronizes all publishing data for RDMS.</span></span><br/>                  |
| [<span data-ttu-id="c60f5-118">**SynchronizePublishingData**</span><span class="sxs-lookup"><span data-stu-id="c60f5-118">**SynchronizePublishingData**</span></span>](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | <span data-ttu-id="c60f5-119">Synchronise le jeu de données de publication spécifié pour les RDMS.</span><span class="sxs-lookup"><span data-stu-id="c60f5-119">Synchronizes the specified set of publishing data for RDMS.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c60f5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c60f5-120">Requirements</span></span>



| <span data-ttu-id="c60f5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c60f5-121">Requirement</span></span> | <span data-ttu-id="c60f5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c60f5-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c60f5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c60f5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c60f5-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c60f5-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c60f5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c60f5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c60f5-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c60f5-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c60f5-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c60f5-127">Namespace</span></span><br/>                | <span data-ttu-id="c60f5-128">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="c60f5-128">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c60f5-129">MOF</span><span class="sxs-lookup"><span data-stu-id="c60f5-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c60f5-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c60f5-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c60f5-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c60f5-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c60f5-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c60f5-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c60f5-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c60f5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60f5-134">Fournisseur de services de gestion Bureau à distance</span><span class="sxs-lookup"><span data-stu-id="c60f5-134">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





