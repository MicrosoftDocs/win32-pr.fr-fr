---
title: Méthode GetStringProperty de la classe Win32_RDSHCollection
description: Récupère une valeur de propriété de type chaîne d’un \_ objet Win32 RDSHCollection.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- GetStringProperty, méthode Services Bureau à distance
- Méthode GetStringProperty Services Bureau à distance, classe Win32_RDSHCollection
- Win32_RDSHCollection de la classe Services Bureau à distance, méthode GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941817"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="2d494-106">Méthode GetStringProperty de la \_ classe RDSHCollection Win32</span><span class="sxs-lookup"><span data-stu-id="2d494-106">GetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="2d494-107">Récupère une valeur de propriété de type chaîne d’un objet [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="2d494-107">Retrieves a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d494-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d494-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="2d494-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d494-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d494-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d494-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d494-111">Clé qui identifie la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="2d494-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="2d494-112">*Valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2d494-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d494-113">Reçoit la valeur de la propriété récupérée.</span><span class="sxs-lookup"><span data-stu-id="2d494-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d494-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d494-114">Return value</span></span>

<span data-ttu-id="2d494-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="2d494-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d494-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d494-116">Requirements</span></span>



| <span data-ttu-id="2d494-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d494-117">Requirement</span></span> | <span data-ttu-id="2d494-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d494-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d494-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d494-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d494-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d494-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2d494-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d494-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d494-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d494-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2d494-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2d494-123">Namespace</span></span><br/>                | <span data-ttu-id="2d494-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="2d494-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2d494-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2d494-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d494-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d494-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d494-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2d494-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d494-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d494-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2d494-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d494-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d494-130">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="2d494-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





