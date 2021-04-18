---
description: La méthode Initialize prépare l’objet IByteBuffer en vue de son utilisation. Cette méthode doit être appelée avant d’appeler d’autres méthodes dans l’interface IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'IByteBuffer :: Initialize, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520125"
---
# <a name="ibytebufferinitialize-method"></a><span data-ttu-id="f7d2a-104">IByteBuffer :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="f7d2a-104">IByteBuffer::Initialize method</span></span>

<span data-ttu-id="f7d2a-105">\[La méthode **Initialize** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-105">\[The **Initialize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f7d2a-106">Elle n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later.</span></span> <span data-ttu-id="f7d2a-107">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f7d2a-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="f7d2a-108">La méthode **Initialize** prépare l’objet [**IByteBuffer**](ibytebuffer.md) en vue de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-108">The **Initialize** method prepares the [**IByteBuffer**](ibytebuffer.md) object for use.</span></span> <span data-ttu-id="f7d2a-109">Cette méthode doit être appelée avant d’appeler d’autres méthodes dans l’interface **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="f7d2a-109">This method must be called prior to calling any other methods in the **IByteBuffer** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d2a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7d2a-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a><span data-ttu-id="f7d2a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7d2a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d2a-112">*lSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7d2a-112">*lSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d2a-113">Taille initiale, en octets, des données que le flux doit contenir.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-113">Initial size, in bytes, of the data the stream is to contain.</span></span>

</dd> <dt>

<span data-ttu-id="f7d2a-114">*pData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7d2a-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d2a-115">Si la **valeur** n’est pas null, il s’agit des données initiales à écrire dans le flux.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-115">If not **NULL**, the initial data to write to the stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d2a-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7d2a-116">Return value</span></span>

<span data-ttu-id="f7d2a-117">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f7d2a-118">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="f7d2a-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d2a-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f7d2a-119">Remarks</span></span>

<span data-ttu-id="f7d2a-120">Quand vous utilisez un nouveau flux [**IByteBuffer**](ibytebuffer.md) , appelez cette méthode avant d’utiliser l’une des autres méthodes **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="f7d2a-120">When using a new [**IByteBuffer**](ibytebuffer.md) stream, call this method prior to using any of the other **IByteBuffer** methods.</span></span>

## <a name="examples"></a><span data-ttu-id="f7d2a-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="f7d2a-121">Examples</span></span>

<span data-ttu-id="f7d2a-122">L’exemple suivant illustre l’initialisation de l’objet [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="f7d2a-122">The following example shows initializing the [**IByteBuffer**](ibytebuffer.md) object.</span></span>


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a><span data-ttu-id="f7d2a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7d2a-123">Requirements</span></span>



| <span data-ttu-id="f7d2a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7d2a-124">Requirement</span></span> | <span data-ttu-id="f7d2a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7d2a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d2a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7d2a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d2a-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7d2a-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f7d2a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7d2a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d2a-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7d2a-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f7d2a-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f7d2a-130">End of client support</span></span><br/>    | <span data-ttu-id="f7d2a-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f7d2a-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f7d2a-132">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f7d2a-132">End of server support</span></span><br/>    | <span data-ttu-id="f7d2a-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f7d2a-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f7d2a-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7d2a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d2a-135"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d2a-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7d2a-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f7d2a-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7d2a-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f7d2a-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f7d2a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f7d2a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7d2a-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7d2a-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f7d2a-140">IID</span><span class="sxs-lookup"><span data-stu-id="f7d2a-140">IID</span></span><br/>                      | <span data-ttu-id="f7d2a-141">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="f7d2a-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

