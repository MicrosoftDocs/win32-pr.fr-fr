---
title: Méthode GetStringProperty de la classe Win32_RDSHServer
description: Récupère une valeur de propriété de type chaîne d’un \_ objet Win32 RDSHServer.
ms.assetid: 136cd213-86a6-472a-8853-8d05f992309a
ms.tgt_platform: multiple
keywords:
- GetStringProperty, méthode Services Bureau à distance
- Méthode GetStringProperty Services Bureau à distance, classe Win32_RDSHServer
- Win32_RDSHServer de la classe Services Bureau à distance, méthode GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619a034e0a2f89270d21bf0c4fc297b4248cef59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466907"
---
# <a name="getstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="accf3-106">Méthode GetStringProperty de la \_ classe RDSHServer Win32</span><span class="sxs-lookup"><span data-stu-id="accf3-106">GetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="accf3-107">Récupère une valeur de propriété de type chaîne d’un objet [**Win32 \_ RDSHServer**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="accf3-107">Retrieves a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="accf3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="accf3-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="accf3-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="accf3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="accf3-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="accf3-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accf3-111">Clé qui identifie la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="accf3-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="accf3-112">*Valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="accf3-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="accf3-113">Reçoit la valeur de la propriété récupérée.</span><span class="sxs-lookup"><span data-stu-id="accf3-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="accf3-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="accf3-114">Return value</span></span>

<span data-ttu-id="accf3-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="accf3-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="accf3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="accf3-116">Requirements</span></span>



| <span data-ttu-id="accf3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="accf3-117">Requirement</span></span> | <span data-ttu-id="accf3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="accf3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="accf3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="accf3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="accf3-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="accf3-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="accf3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="accf3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="accf3-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="accf3-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="accf3-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="accf3-123">Namespace</span></span><br/>                | <span data-ttu-id="accf3-124">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="accf3-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="accf3-125">MOF</span><span class="sxs-lookup"><span data-stu-id="accf3-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="accf3-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="accf3-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="accf3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="accf3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="accf3-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="accf3-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="accf3-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="accf3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accf3-130">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="accf3-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





