---
description: La fonction GetCaptureMacType retourne le type MAC d’une capture donnée.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: GetCaptureMacType, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750093"
---
# <a name="getcapturemactype-function"></a><span data-ttu-id="2c7db-103">GetCaptureMacType fonction)</span><span class="sxs-lookup"><span data-stu-id="2c7db-103">GetCaptureMacType function</span></span>

<span data-ttu-id="2c7db-104">La fonction **GetCaptureMacType** retourne le type Mac d’une capture donnée.</span><span class="sxs-lookup"><span data-stu-id="2c7db-104">The **GetCaptureMacType** function returns the MAC type of a given capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c7db-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c7db-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="2c7db-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c7db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c7db-107">*hCapture* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c7db-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c7db-108">Handle de la capture.</span><span class="sxs-lookup"><span data-stu-id="2c7db-108">Handle to the capture.</span></span> <span data-ttu-id="2c7db-109">Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes de cette rubrique **GetCaptureMacType** .</span><span class="sxs-lookup"><span data-stu-id="2c7db-109">For information about obtaining the capture handle, see the Remarks section in this **GetCaptureMacType** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c7db-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c7db-110">Return value</span></span>

<span data-ttu-id="2c7db-111">Si la fonction réussit, la valeur de retour est l’un des types MAC suivants.</span><span class="sxs-lookup"><span data-stu-id="2c7db-111">If the function is successful, the return value is one of the following MAC types.</span></span>

-   <span data-ttu-id="2c7db-112">\_type Mac \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="2c7db-112">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="2c7db-113">MAC \_ type \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="2c7db-113">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="2c7db-114">\_type Mac \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="2c7db-114">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="2c7db-115">\_type Mac \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="2c7db-115">MAC\_TYPE\_FDDI</span></span>

<span data-ttu-id="2c7db-116">Si la fonction échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="2c7db-116">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="2c7db-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2c7db-117">Return code</span></span>                                                                                              | <span data-ttu-id="2c7db-118">Description</span><span class="sxs-lookup"><span data-stu-id="2c7db-118">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="2c7db-119"><dt>**\_type Mac \_ NMERR \_ inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="2c7db-119"><dt>**NMERR\_MAC\_TYPE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="2c7db-120">Moniteur réseau n’a pas pu trouver un type MAC connu.</span><span class="sxs-lookup"><span data-stu-id="2c7db-120">Network Monitor could not find a known MAC type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c7db-121">Notes</span><span class="sxs-lookup"><span data-stu-id="2c7db-121">Remarks</span></span>

<span data-ttu-id="2c7db-122">Le descripteur de la capture peut être obtenu de plusieurs façons, en fonction de la personne qui effectue l’appel.</span><span class="sxs-lookup"><span data-stu-id="2c7db-122">The handle of the capture can be obtained in several ways, depending on who makes the call.</span></span> <span data-ttu-id="2c7db-123">Pour les experts, le descripteur est spécifié dans le membre **hCapture** de la structure [EXPERTSTARTUPINFO](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2c7db-123">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="2c7db-124">Pour les analyseurs, le handle de capture peut être obtenu en appelant la fonction [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="2c7db-124">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="2c7db-125">Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureMacType** .</span><span class="sxs-lookup"><span data-stu-id="2c7db-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c7db-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c7db-126">Requirements</span></span>



| <span data-ttu-id="2c7db-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c7db-127">Requirement</span></span> | <span data-ttu-id="2c7db-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c7db-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2c7db-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c7db-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2c7db-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c7db-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2c7db-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c7db-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2c7db-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c7db-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2c7db-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c7db-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c7db-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c7db-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2c7db-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c7db-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="2c7db-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c7db-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2c7db-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2c7db-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c7db-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c7db-138"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




