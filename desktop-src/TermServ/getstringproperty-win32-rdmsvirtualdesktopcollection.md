---
title: Méthode GetStringProperty de la classe Win32_RDMSVirtualDesktopCollection
description: Récupère une propriété de type chaîne à partir d’une collection de bureaux virtuels.
ms.assetid: 4a122fc5-1635-4d74-a90d-2347c0714fc7
ms.tgt_platform: multiple
keywords:
- GetStringProperty, méthode Services Bureau à distance
- Méthode GetStringProperty Services Bureau à distance, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242d973d7ec8d320ed589933567b337a035f0e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512364"
---
# <a name="getstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="d4112-106">Méthode GetStringProperty de la \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="d4112-106">GetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="d4112-107">Récupère une propriété de type chaîne à partir d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="d4112-107">Retrieves a string property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4112-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4112-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="d4112-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4112-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4112-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d4112-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4112-111">Clé qui identifie la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="d4112-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d4112-112">*Valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d4112-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4112-113">Chaîne qui reçoit la valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="d4112-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4112-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4112-114">Return value</span></span>

<span data-ttu-id="d4112-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="d4112-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4112-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4112-116">Requirements</span></span>



| <span data-ttu-id="d4112-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4112-117">Requirement</span></span> | <span data-ttu-id="d4112-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4112-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4112-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4112-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d4112-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4112-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d4112-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4112-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d4112-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4112-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d4112-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d4112-123">Namespace</span></span><br/>                | <span data-ttu-id="d4112-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="d4112-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d4112-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d4112-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4112-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4112-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4112-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d4112-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4112-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4112-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d4112-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4112-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4112-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="d4112-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





