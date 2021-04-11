---
description: La méthode Clone crée un nouvel objet avec son propre pointeur de recherche qui référence les mêmes octets que l’objet IByteBuffer d’origine.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'IByteBuffer :: Clone, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204172"
---
# <a name="ibytebufferclone-method"></a><span data-ttu-id="660f0-103">IByteBuffer :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="660f0-103">IByteBuffer::Clone method</span></span>

<span data-ttu-id="660f0-104">\[La méthode **clone** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="660f0-104">\[The **Clone** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="660f0-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="660f0-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="660f0-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="660f0-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="660f0-107">La méthode **clone** crée un nouvel objet avec son propre pointeur de recherche qui référence les mêmes octets que l’objet [**IByteBuffer**](ibytebuffer.md) d’origine.</span><span class="sxs-lookup"><span data-stu-id="660f0-107">The **Clone** method creates a new object with its own seek pointer that references the same bytes as the original [**IByteBuffer**](ibytebuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="660f0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="660f0-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="660f0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="660f0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="660f0-110">*ppByteBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="660f0-110">*ppByteBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="660f0-111">En cas de réussite, pointe vers l’emplacement d’un pointeur [**IByteBuffer**](ibytebuffer.md) vers le nouvel objet de flux.</span><span class="sxs-lookup"><span data-stu-id="660f0-111">When successful, points to the location of an [**IByteBuffer**](ibytebuffer.md) pointer to the new stream object.</span></span> <span data-ttu-id="660f0-112">Lorsque vous avez terminé d’utiliser le pointeur **IByteBuffer** , libérez-le en appelant la fonction [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) .</span><span class="sxs-lookup"><span data-stu-id="660f0-112">When you have finished using the **IByteBuffer** pointer, release it by calling the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) function.</span></span> <span data-ttu-id="660f0-113">Si une erreur se produit, ce paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="660f0-113">If an error occurs, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="660f0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="660f0-114">Return value</span></span>

<span data-ttu-id="660f0-115">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="660f0-115">The return value is an **HRESULT**.</span></span> <span data-ttu-id="660f0-116">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="660f0-116">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="660f0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="660f0-117">Remarks</span></span>

<span data-ttu-id="660f0-118">Cette méthode crée un nouvel objet de flux pour accéder aux mêmes octets, mais à l’aide d’un pointeur de recherche distinct.</span><span class="sxs-lookup"><span data-stu-id="660f0-118">This method creates a new stream object for accessing the same bytes but using a separate seek pointer.</span></span> <span data-ttu-id="660f0-119">Le nouvel objet de flux voit les mêmes données que l’objet de flux source.</span><span class="sxs-lookup"><span data-stu-id="660f0-119">The new stream object sees the same data as the source stream object.</span></span> <span data-ttu-id="660f0-120">Les modifications écrites dans un objet sont immédiatement visibles dans l’autre.</span><span class="sxs-lookup"><span data-stu-id="660f0-120">Changes written to one object are immediately visible in the other.</span></span> <span data-ttu-id="660f0-121">Le verrouillage de plage est partagé entre les objets de flux.</span><span class="sxs-lookup"><span data-stu-id="660f0-121">Range locking is shared between the stream objects.</span></span>

<span data-ttu-id="660f0-122">Le paramètre initial du pointeur de recherche dans l’instance de flux cloné est le même que le paramètre actuel du pointeur de recherche dans le flux d’origine au moment de l’opération de clonage.</span><span class="sxs-lookup"><span data-stu-id="660f0-122">The initial setting of the seek pointer in the cloned stream instance is the same as the current setting of the seek pointer in the original stream at the time of the clone operation.</span></span>

## <a name="examples"></a><span data-ttu-id="660f0-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="660f0-123">Examples</span></span>

<span data-ttu-id="660f0-124">L’exemple suivant illustre le clonage de l’interface [**IByteBuffer**](ibytebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="660f0-124">The following example shows cloning the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
```



## <a name="requirements"></a><span data-ttu-id="660f0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="660f0-125">Requirements</span></span>



| <span data-ttu-id="660f0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="660f0-126">Requirement</span></span> | <span data-ttu-id="660f0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="660f0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="660f0-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="660f0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="660f0-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="660f0-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="660f0-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="660f0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="660f0-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="660f0-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="660f0-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="660f0-132">End of client support</span></span><br/>    | <span data-ttu-id="660f0-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="660f0-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="660f0-134">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="660f0-134">End of server support</span></span><br/>    | <span data-ttu-id="660f0-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="660f0-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="660f0-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="660f0-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="660f0-137"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="660f0-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="660f0-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="660f0-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="660f0-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="660f0-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="660f0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="660f0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="660f0-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="660f0-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="660f0-142">IID</span><span class="sxs-lookup"><span data-stu-id="660f0-142">IID</span></span><br/>                      | <span data-ttu-id="660f0-143">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="660f0-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

