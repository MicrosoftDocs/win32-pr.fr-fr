---
description: Récupère le PROPVARIANT et la chaîne d’entrée qui représente un segment de données. L’appel de cette méthode est identique à l’appel de GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'IRichChunk :: RemoteGetData, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112390"
---
# <a name="irichchunkremotegetdata-method"></a><span data-ttu-id="df727-104">IRichChunk :: RemoteGetData, méthode</span><span class="sxs-lookup"><span data-stu-id="df727-104">IRichChunk::RemoteGetData method</span></span>

<span data-ttu-id="df727-105">Récupère le [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) et la chaîne d’entrée qui représente un segment de données.</span><span class="sxs-lookup"><span data-stu-id="df727-105">Retrieves the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) and input string that represents a chunk of data.</span></span> <span data-ttu-id="df727-106">L’appel de cette méthode est identique à l’appel de [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span><span class="sxs-lookup"><span data-stu-id="df727-106">Calling this method is the same as calling [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span></span>

## <a name="syntax"></a><span data-ttu-id="df727-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df727-107">Syntax</span></span>


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="df727-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df727-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df727-109">*pFirstPos* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="df727-109">*pFirstPos* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df727-110">Reçoit la position de départ de base zéro de la plage.</span><span class="sxs-lookup"><span data-stu-id="df727-110">Receives the zero-based starting position of the range.</span></span> <span data-ttu-id="df727-111">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="df727-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="df727-112">*PLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="df727-112">*pLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df727-113">Reçoit la longueur de la plage.</span><span class="sxs-lookup"><span data-stu-id="df727-113">Receives the length of the range.</span></span> <span data-ttu-id="df727-114">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="df727-114">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="df727-115">*ppsz* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="df727-115">*ppsz* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df727-116">Reçoit la valeur de chaîne Unicode associée, ou **null** si elle n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="df727-116">Receives the associated Unicode string value, or **NULL** if not available.</span></span>

</dd> <dt>

<span data-ttu-id="df727-117">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="df727-117">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df727-118">Reçoit la valeur [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) associée, ou **VT \_ vide** s’il n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="df727-118">Receives the associated [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value, or **VT\_EMPTY** if not available.</span></span> <span data-ttu-id="df727-119">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="df727-119">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df727-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df727-120">Return value</span></span>

<span data-ttu-id="df727-121">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="df727-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="df727-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="df727-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="df727-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df727-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df727-124">**IRichChunk**</span><span class="sxs-lookup"><span data-stu-id="df727-124">**IRichChunk**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
