---
title: Méthode KeyValueCompareAndSet de la classe Win32_RDSHCollection
description: Compare la clé spécifiée dans la collection avec un comparand ; Si elles correspondent, la nouvelle valeur est affectée à la clé. Si la clé n’existe pas, la méthode insère la clé dans la collection.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode KeyValueCompareAndSet
- Services Bureau à distance de la méthode KeyValueCompareAndSet, classe Win32_RDSHCollection
- Win32_RDSHCollection de la classe Services Bureau à distance, méthode KeyValueCompareAndSet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843394"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="75126-107">Méthode KeyValueCompareAndSet de la \_ classe Win32 RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="75126-107">KeyValueCompareAndSet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="75126-108">Compare la clé spécifiée dans la collection avec un comparand ; Si elles correspondent, la nouvelle valeur est affectée à la clé.</span><span class="sxs-lookup"><span data-stu-id="75126-108">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="75126-109">Si la clé n’existe pas, la méthode insère la clé dans la collection.</span><span class="sxs-lookup"><span data-stu-id="75126-109">If the key does not exist, the method will insert the key into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="75126-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75126-110">Syntax</span></span>


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a><span data-ttu-id="75126-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75126-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75126-112">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75126-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75126-113">Clé à comparer.</span><span class="sxs-lookup"><span data-stu-id="75126-113">The key to compare.</span></span>

</dd> <dt>

<span data-ttu-id="75126-114">*NewValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75126-114">*NewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75126-115">Nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="75126-115">The new value.</span></span>

</dd> <dt>

<span data-ttu-id="75126-116">*Comparand* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75126-116">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75126-117">Chaîne à laquelle comparer la clé.</span><span class="sxs-lookup"><span data-stu-id="75126-117">The string to compare the key to.</span></span>

</dd> <dt>

<span data-ttu-id="75126-118">*InitialValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="75126-118">*InitialValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75126-119">En cas de réussite ou d’échec, contient la valeur initiale de la clé.</span><span class="sxs-lookup"><span data-stu-id="75126-119">On success or failure, contains the initial value of the key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75126-120">Notes</span><span class="sxs-lookup"><span data-stu-id="75126-120">Remarks</span></span>

<span data-ttu-id="75126-121">Notez que cette méthode peut récupérer la valeur de la clé et, par conséquent, encapsule les fonctionnalités de [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span><span class="sxs-lookup"><span data-stu-id="75126-121">Note that this method can retrieve the value of the key, and as such encapsulates the functionality of [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75126-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75126-122">Requirements</span></span>



| <span data-ttu-id="75126-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75126-123">Requirement</span></span> | <span data-ttu-id="75126-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="75126-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="75126-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75126-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75126-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="75126-126">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="75126-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75126-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75126-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="75126-128">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="75126-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="75126-129">Namespace</span></span><br/>                | <span data-ttu-id="75126-130">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="75126-130">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="75126-131">MOF</span><span class="sxs-lookup"><span data-stu-id="75126-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75126-132"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75126-132"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="75126-133">DLL</span><span class="sxs-lookup"><span data-stu-id="75126-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75126-134"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75126-134"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="75126-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75126-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75126-136">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="75126-136">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





