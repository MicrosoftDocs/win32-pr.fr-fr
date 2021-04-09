---
title: Méthode SetStringProperty de la classe Win32_RDSHServer (certenroll. h)
description: Met à jour une valeur de propriété de type chaîne d’un \_ objet Win32 RDSHServer.
ms.assetid: 9a338872-27fc-4e37-afd6-20a42c7859e5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetStringProperty
- Services Bureau à distance de la méthode SetStringProperty, classe Win32_RDSHServer
- Win32_RDSHServer de la classe Services Bureau à distance, méthode SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d30812c0df943175f96c8ae43a4fe094725c74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104599"
---
# <a name="setstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="ace20-106">Méthode SetStringProperty de la \_ classe Win32 RDSHServer</span><span class="sxs-lookup"><span data-stu-id="ace20-106">SetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="ace20-107">Met à jour une valeur de propriété de type chaîne d’un objet [**Win32 \_ RDSHServer**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="ace20-107">Updates a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ace20-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ace20-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="ace20-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ace20-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ace20-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ace20-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace20-111">Clé qui identifie la propriété à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="ace20-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="ace20-112">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ace20-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ace20-113">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ace20-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ace20-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ace20-114">Return value</span></span>

<span data-ttu-id="ace20-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="ace20-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ace20-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ace20-116">Requirements</span></span>



| <span data-ttu-id="ace20-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ace20-117">Requirement</span></span> | <span data-ttu-id="ace20-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ace20-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ace20-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace20-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ace20-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace20-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ace20-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ace20-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ace20-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ace20-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ace20-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ace20-123">Namespace</span></span><br/>                | <span data-ttu-id="ace20-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="ace20-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ace20-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ace20-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ace20-126"><dt>Certenroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="ace20-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="ace20-127">MOF</span><span class="sxs-lookup"><span data-stu-id="ace20-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ace20-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ace20-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ace20-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ace20-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ace20-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ace20-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ace20-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ace20-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ace20-132">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="ace20-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





