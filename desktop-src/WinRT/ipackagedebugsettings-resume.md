---
description: Reprend les processus du package s’ils sont actuellement suspendus.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'IPackageDebugSettings :: Resume, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514438"
---
# <a name="ipackagedebugsettingsresume-method"></a><span data-ttu-id="73edc-103">IPackageDebugSettings :: Resume, méthode</span><span class="sxs-lookup"><span data-stu-id="73edc-103">IPackageDebugSettings::Resume method</span></span>

<span data-ttu-id="73edc-104">Reprend les processus du package s’ils sont actuellement suspendus.</span><span class="sxs-lookup"><span data-stu-id="73edc-104">Resumes the processes of the package if they are currently suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="73edc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73edc-105">Syntax</span></span>


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="73edc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73edc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73edc-107">*packageFullName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="73edc-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73edc-108">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="73edc-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="73edc-109">Nom complet du package.</span><span class="sxs-lookup"><span data-stu-id="73edc-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73edc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73edc-110">Return value</span></span>

<span data-ttu-id="73edc-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="73edc-111">Type: **HRESULT**</span></span>

<span data-ttu-id="73edc-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="73edc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73edc-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73edc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73edc-114">Notes</span><span class="sxs-lookup"><span data-stu-id="73edc-114">Remarks</span></span>

<span data-ttu-id="73edc-115">Chaque processus reçoit l’événement de [**reprise**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="73edc-115">Each process receives the [**Resuming**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="73edc-116">Il peut être utile pour les développeurs d’effectuer un pas à pas détaillé de la façon dont leurs applications répondent à cet événement.</span><span class="sxs-lookup"><span data-stu-id="73edc-116">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="73edc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73edc-117">Requirements</span></span>



| <span data-ttu-id="73edc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73edc-118">Requirement</span></span> | <span data-ttu-id="73edc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="73edc-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73edc-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73edc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="73edc-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="73edc-121">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="73edc-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73edc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="73edc-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73edc-123">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="73edc-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="73edc-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="73edc-125"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="73edc-125"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73edc-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73edc-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="73edc-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="73edc-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
