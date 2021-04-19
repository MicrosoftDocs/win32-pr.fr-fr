---
title: Méthode SetInt32Property de la classe Win32_RDSHCollection
description: Met à jour une valeur de propriété entière d’un \_ objet Win32 RDSHCollection.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetInt32Property
- Services Bureau à distance de la méthode SetInt32Property, classe Win32_RDSHCollection
- Win32_RDSHCollection de la classe Services Bureau à distance, méthode SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 136bb8ccf34004f747829fb43ee8080ccd1d3132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510572"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="7f868-106">Méthode SetInt32Property de la \_ classe Win32 RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="7f868-106">SetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="7f868-107">Met à jour une valeur de propriété entière d’un objet [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="7f868-107">Updates an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f868-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f868-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="7f868-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f868-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f868-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f868-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f868-111">Clé qui identifie la propriété à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="7f868-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="7f868-112">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7f868-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f868-113">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7f868-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f868-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f868-114">Return value</span></span>

<span data-ttu-id="7f868-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="7f868-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f868-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f868-116">Requirements</span></span>



| <span data-ttu-id="7f868-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f868-117">Requirement</span></span> | <span data-ttu-id="7f868-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f868-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f868-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f868-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f868-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f868-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7f868-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f868-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f868-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7f868-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7f868-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7f868-123">Namespace</span></span><br/>                | <span data-ttu-id="7f868-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="7f868-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7f868-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7f868-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f868-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f868-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f868-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7f868-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f868-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f868-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7f868-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f868-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f868-130">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="7f868-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





