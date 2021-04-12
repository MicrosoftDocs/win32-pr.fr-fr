---
title: Méthode SetInt32Property de la classe Win32_RDMSVirtualDesktopCollection
description: Met à jour une propriété entière d’une collection de bureaux virtuels.
ms.assetid: 2ea27385-5100-4e88-ad11-df5e439d0815
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetInt32Property
- Services Bureau à distance de la méthode SetInt32Property, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c2a93a52ce79bc185cd37dd9ac93e5b420b5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105844"
---
# <a name="setint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="d27a4-106">Méthode SetInt32Property de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="d27a4-106">SetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="d27a4-107">Met à jour une propriété entière d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="d27a4-107">Updates an integer property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d27a4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d27a4-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="d27a4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d27a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27a4-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d27a4-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d27a4-111">Clé qui identifie la propriété à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="d27a4-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="d27a4-112">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d27a4-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d27a4-113">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d27a4-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27a4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d27a4-114">Return value</span></span>

<span data-ttu-id="d27a4-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="d27a4-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d27a4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d27a4-116">Requirements</span></span>



| <span data-ttu-id="d27a4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d27a4-117">Requirement</span></span> | <span data-ttu-id="d27a4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d27a4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d27a4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d27a4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d27a4-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d27a4-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d27a4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d27a4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d27a4-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d27a4-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d27a4-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d27a4-123">Namespace</span></span><br/>                | <span data-ttu-id="d27a4-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="d27a4-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d27a4-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d27a4-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d27a4-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d27a4-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d27a4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d27a4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d27a4-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d27a4-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d27a4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d27a4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d27a4-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="d27a4-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





