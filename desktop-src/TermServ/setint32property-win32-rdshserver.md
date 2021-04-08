---
title: Méthode SetInt32Property de la classe Win32_RDSHServer
description: Met à jour une valeur de propriété entière d’un \_ objet Win32 RDSHServer.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetInt32Property
- Services Bureau à distance de la méthode SetInt32Property, classe Win32_RDSHServer
- Win32_RDSHServer de la classe Services Bureau à distance, méthode SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741300"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="7413b-106">Méthode SetInt32Property de la \_ classe Win32 RDSHServer</span><span class="sxs-lookup"><span data-stu-id="7413b-106">SetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="7413b-107">Met à jour une valeur de propriété entière d’un objet [**Win32 \_ RDSHServer**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="7413b-107">Updates an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7413b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7413b-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="7413b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7413b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7413b-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7413b-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7413b-111">Clé qui identifie la propriété à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="7413b-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="7413b-112">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7413b-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7413b-113">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7413b-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7413b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7413b-114">Return value</span></span>

<span data-ttu-id="7413b-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="7413b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7413b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7413b-116">Requirements</span></span>



| <span data-ttu-id="7413b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7413b-117">Requirement</span></span> | <span data-ttu-id="7413b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7413b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7413b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7413b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7413b-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7413b-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7413b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7413b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7413b-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7413b-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7413b-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7413b-123">Namespace</span></span><br/>                | <span data-ttu-id="7413b-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="7413b-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7413b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7413b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7413b-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7413b-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7413b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7413b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7413b-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7413b-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7413b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7413b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7413b-130">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="7413b-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





