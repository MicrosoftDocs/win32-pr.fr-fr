---
description: Interrompt les processus du package s’ils sont en cours d’exécution.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'IPackageDebugSettings :: suspend, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751493"
---
# <a name="ipackagedebugsettingssuspend-method"></a><span data-ttu-id="327de-103">IPackageDebugSettings :: suspend, méthode</span><span class="sxs-lookup"><span data-stu-id="327de-103">IPackageDebugSettings::Suspend method</span></span>

<span data-ttu-id="327de-104">Interrompt les processus du package s’ils sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="327de-104">Suspends the processes of the package if they are currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="327de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="327de-105">Syntax</span></span>


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="327de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="327de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="327de-107">*packageFullName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="327de-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="327de-108">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="327de-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="327de-109">Nom complet du package.</span><span class="sxs-lookup"><span data-stu-id="327de-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="327de-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="327de-110">Return value</span></span>

<span data-ttu-id="327de-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="327de-111">Type: **HRESULT**</span></span>

<span data-ttu-id="327de-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="327de-112">This method can return one of these values.</span></span>



| <span data-ttu-id="327de-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="327de-113">Return code</span></span>                                                                                            | <span data-ttu-id="327de-114">Description</span><span class="sxs-lookup"><span data-stu-id="327de-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="327de-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="327de-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="327de-116">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="327de-116">The operation succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="327de-117"><dt>**E \_ STATECHANGE non conforme \_**</dt></span><span class="sxs-lookup"><span data-stu-id="327de-117"><dt>**E\_ILLEGAL\_STATECHANGE**</dt></span></span> </dl> | <span data-ttu-id="327de-118">Le processus n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="327de-118">The process is not currently running.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="327de-119">Notes</span><span class="sxs-lookup"><span data-stu-id="327de-119">Remarks</span></span>

<span data-ttu-id="327de-120">Chaque processus reçoit l’événement [**suspension**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="327de-120">Each process receives the [**Suspending**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="327de-121">Il peut être utile pour les développeurs d’effectuer un pas à pas détaillé de la façon dont leurs applications répondent à cet événement.</span><span class="sxs-lookup"><span data-stu-id="327de-121">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="327de-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="327de-122">Requirements</span></span>



| <span data-ttu-id="327de-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="327de-123">Requirement</span></span> | <span data-ttu-id="327de-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="327de-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="327de-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="327de-125">Minimum supported client</span></span><br/> | <span data-ttu-id="327de-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="327de-126">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="327de-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="327de-127">Minimum supported server</span></span><br/> | <span data-ttu-id="327de-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="327de-128">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="327de-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="327de-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="327de-130"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="327de-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="327de-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="327de-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="327de-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="327de-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
