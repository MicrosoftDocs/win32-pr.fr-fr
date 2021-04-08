---
title: Méthode GetInt32Property de la classe Win32_RDSHCollection (Microsoft. Diagnostics. appanalysis. h)
description: Récupère une valeur de propriété entière d’un \_ objet Win32 RDSHCollection.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetInt32Property
- Services Bureau à distance de la méthode GetInt32Property, classe Win32_RDSHCollection
- Win32_RDSHCollection de la classe Services Bureau à distance, méthode GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5cc29234fe3bb1b92e68e728423931da965391f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740405"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="dfa5c-106">Méthode GetInt32Property de la \_ classe Win32 RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="dfa5c-106">GetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="dfa5c-107">Récupère une valeur de propriété entière d’un objet [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="dfa5c-107">Retrieves an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa5c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfa5c-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="dfa5c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfa5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa5c-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfa5c-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa5c-111">Clé qui identifie la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="dfa5c-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="dfa5c-112">*Valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dfa5c-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa5c-113">Reçoit la valeur de la propriété récupérée.</span><span class="sxs-lookup"><span data-stu-id="dfa5c-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa5c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfa5c-114">Return value</span></span>

<span data-ttu-id="dfa5c-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="dfa5c-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa5c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfa5c-116">Requirements</span></span>



| <span data-ttu-id="dfa5c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfa5c-117">Requirement</span></span> | <span data-ttu-id="dfa5c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfa5c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa5c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfa5c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dfa5c-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfa5c-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="dfa5c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfa5c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dfa5c-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dfa5c-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="dfa5c-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dfa5c-123">Namespace</span></span><br/>                | <span data-ttu-id="dfa5c-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="dfa5c-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="dfa5c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfa5c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfa5c-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5c-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="dfa5c-127">MOF</span><span class="sxs-lookup"><span data-stu-id="dfa5c-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfa5c-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5c-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="dfa5c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dfa5c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfa5c-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5c-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="dfa5c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfa5c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa5c-132">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="dfa5c-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





