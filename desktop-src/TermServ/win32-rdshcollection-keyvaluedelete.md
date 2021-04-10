---
title: Méthode KeyValueDelete de la classe Win32_RDSHCollection
description: Supprime la clé spécifiée (et la valeur associée) de la collection.
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode KeyValueDelete
- Services Bureau à distance de la méthode KeyValueDelete, classe Win32_RDSHCollection
- Win32_RDSHCollection de la classe Services Bureau à distance, méthode KeyValueDelete
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1b4b29aea7890817c8d3cd8599f6effceb53c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941987"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="271b1-106">Méthode KeyValueDelete de la \_ classe Win32 RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="271b1-106">KeyValueDelete method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="271b1-107">Supprime la clé spécifiée (et la valeur associée) de la collection.</span><span class="sxs-lookup"><span data-stu-id="271b1-107">Deletes the specified key (and associated value) from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="271b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="271b1-108">Syntax</span></span>


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="271b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="271b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="271b1-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="271b1-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="271b1-111">Clé à supprimer.</span><span class="sxs-lookup"><span data-stu-id="271b1-111">The key to delete.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="271b1-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="271b1-112">Requirements</span></span>



| <span data-ttu-id="271b1-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="271b1-113">Requirement</span></span> | <span data-ttu-id="271b1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="271b1-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="271b1-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="271b1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="271b1-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="271b1-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="271b1-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="271b1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="271b1-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="271b1-118">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="271b1-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="271b1-119">Namespace</span></span><br/>                | <span data-ttu-id="271b1-120">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="271b1-120">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="271b1-121">MOF</span><span class="sxs-lookup"><span data-stu-id="271b1-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="271b1-122"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="271b1-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="271b1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="271b1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="271b1-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="271b1-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="271b1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="271b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="271b1-126">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="271b1-126">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





