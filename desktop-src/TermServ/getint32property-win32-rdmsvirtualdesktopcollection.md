---
title: Méthode GetInt32Property de la classe Win32_RDMSVirtualDesktopCollection (Microsoft. Diagnostics. appanalysis. h)
description: Récupère une propriété entière à partir d’une collection de bureaux virtuels.
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetInt32Property
- Services Bureau à distance de la méthode GetInt32Property, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106530800"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="5a6fc-106">Méthode GetInt32Property de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="5a6fc-106">GetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="5a6fc-107">Récupère une propriété entière à partir d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="5a6fc-107">Retrieves an integer property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a6fc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a6fc-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="5a6fc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a6fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a6fc-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5a6fc-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6fc-111">Clé qui identifie la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="5a6fc-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5a6fc-112">*Valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a6fc-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a6fc-113">Entier qui reçoit la valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="5a6fc-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a6fc-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a6fc-114">Return value</span></span>

<span data-ttu-id="5a6fc-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="5a6fc-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a6fc-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a6fc-116">Requirements</span></span>



| <span data-ttu-id="5a6fc-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a6fc-117">Requirement</span></span> | <span data-ttu-id="5a6fc-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a6fc-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a6fc-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a6fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5a6fc-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a6fc-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="5a6fc-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a6fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5a6fc-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5a6fc-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="5a6fc-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5a6fc-123">Namespace</span></span><br/>                | <span data-ttu-id="5a6fc-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="5a6fc-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="5a6fc-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a6fc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a6fc-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a6fc-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="5a6fc-127">MOF</span><span class="sxs-lookup"><span data-stu-id="5a6fc-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a6fc-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a6fc-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="5a6fc-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5a6fc-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a6fc-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a6fc-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="5a6fc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a6fc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a6fc-132">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="5a6fc-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





