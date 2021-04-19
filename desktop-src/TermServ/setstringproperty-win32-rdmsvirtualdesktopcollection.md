---
title: Méthode SetStringProperty de la classe Win32_RDMSVirtualDesktopCollection (certenroll. h)
description: Met à jour une propriété de type chaîne d’une collection de bureaux virtuels.
ms.assetid: d76d5f77-3b51-41b9-8ec5-a737ddc0a9d3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetStringProperty
- Services Bureau à distance de la méthode SetStringProperty, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fd85ef6611cd02dc80ca66816c5c4ce13f6cd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509535"
---
# <a name="setstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="60b24-106">Méthode SetStringProperty de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="60b24-106">SetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="60b24-107">Met à jour une propriété de type chaîne d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="60b24-107">Updates a string property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b24-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60b24-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="60b24-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="60b24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b24-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60b24-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b24-111">Clé qui identifie la propriété à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="60b24-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="60b24-112">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="60b24-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b24-113">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="60b24-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b24-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="60b24-114">Return value</span></span>

<span data-ttu-id="60b24-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="60b24-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b24-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60b24-116">Requirements</span></span>



| <span data-ttu-id="60b24-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60b24-117">Requirement</span></span> | <span data-ttu-id="60b24-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="60b24-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b24-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60b24-119">Minimum supported client</span></span><br/> | <span data-ttu-id="60b24-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="60b24-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="60b24-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60b24-121">Minimum supported server</span></span><br/> | <span data-ttu-id="60b24-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60b24-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="60b24-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60b24-123">Namespace</span></span><br/>                | <span data-ttu-id="60b24-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="60b24-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="60b24-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="60b24-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="60b24-126"><dt>Certenroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b24-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="60b24-127">MOF</span><span class="sxs-lookup"><span data-stu-id="60b24-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60b24-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60b24-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="60b24-129">DLL</span><span class="sxs-lookup"><span data-stu-id="60b24-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60b24-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60b24-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="60b24-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60b24-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b24-132">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="60b24-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





