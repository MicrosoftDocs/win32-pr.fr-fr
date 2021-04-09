---
title: Méthode KeyValueGet de la classe Win32_RDSHCollection
description: Récupère la valeur associée à la clé spécifiée dans la collection.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode KeyValueGet
- Services Bureau à distance de la méthode KeyValueGet, classe Win32_RDSHCollection
- Win32_RDSHCollection de la classe Services Bureau à distance, méthode KeyValueGet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843393"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="bf423-106">Méthode KeyValueGet de la \_ classe Win32 RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="bf423-106">KeyValueGet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="bf423-107">Récupère la valeur associée à la clé spécifiée dans la collection.</span><span class="sxs-lookup"><span data-stu-id="bf423-107">Retrieves the value associated with the specified key in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf423-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf423-108">Syntax</span></span>


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="bf423-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf423-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf423-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf423-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf423-111">Clé qui identifie la valeur que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="bf423-111">The key that identifies the value you wish to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="bf423-112">*Valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bf423-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf423-113">En cas de réussite, retourne la valeur associée à la clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bf423-113">On success, returns the value associated with the specified key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf423-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf423-114">Requirements</span></span>



| <span data-ttu-id="bf423-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf423-115">Requirement</span></span> | <span data-ttu-id="bf423-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf423-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf423-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf423-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bf423-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf423-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="bf423-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf423-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bf423-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bf423-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="bf423-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bf423-121">Namespace</span></span><br/>                | <span data-ttu-id="bf423-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="bf423-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="bf423-123">MOF</span><span class="sxs-lookup"><span data-stu-id="bf423-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf423-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf423-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf423-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bf423-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf423-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf423-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="bf423-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf423-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf423-128">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="bf423-128">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





