---
description: La méthode Configure modifie la taille de l’objet de flux.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'IByteBuffer :: Assets, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952792"
---
# <a name="ibytebuffersetsize-method"></a><span data-ttu-id="8df4e-103">IByteBuffer :: deinstalle, méthode</span><span class="sxs-lookup"><span data-stu-id="8df4e-103">IByteBuffer::SetSize method</span></span>

<span data-ttu-id="8df4e-104">\[La méthode **configure** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="8df4e-104">\[The **SetSize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8df4e-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8df4e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8df4e-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8df4e-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="8df4e-107">La méthode **configure** modifie la taille de l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="8df4e-107">The **SetSize** method changes the size of the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df4e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8df4e-108">Syntax</span></span>


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a><span data-ttu-id="8df4e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8df4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df4e-110">*libNewSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8df4e-110">*libNewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df4e-111">Nouvelle taille du flux sous la forme d’un nombre d’octets</span><span class="sxs-lookup"><span data-stu-id="8df4e-111">New size of the stream as a number of bytes</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df4e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8df4e-112">Return value</span></span>

<span data-ttu-id="8df4e-113">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8df4e-113">The return value is an **HRESULT**.</span></span> <span data-ttu-id="8df4e-114">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="8df4e-114">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8df4e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8df4e-115">Remarks</span></span>

<span data-ttu-id="8df4e-116">La méthode **IByteBuffer :: configure** modifie la taille de l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="8df4e-116">The **IByteBuffer::SetSize** method changes the size of the stream object.</span></span> <span data-ttu-id="8df4e-117">Appelez cette méthode pour préallouer de l’espace pour le flux.</span><span class="sxs-lookup"><span data-stu-id="8df4e-117">Call this method to preallocate space for the stream.</span></span> <span data-ttu-id="8df4e-118">Si le paramètre *libNewSize* est plus grand que la taille de flux actuelle, le flux est étendu à la taille indiquée en remplissant l’espace intermédiaire avec des octets de valeur non définie.</span><span class="sxs-lookup"><span data-stu-id="8df4e-118">If the *libNewSize* parameter is larger than the current stream size, the stream is extended to the indicated size by filling the intervening space with bytes of undefined value.</span></span> <span data-ttu-id="8df4e-119">Cette opération est semblable à la méthode [**IByteBuffer :: Write**](ibytebuffer-write.md) si le pointeur de recherche se trouve au-delà de la fin de flux actuelle.</span><span class="sxs-lookup"><span data-stu-id="8df4e-119">This operation is similar to the [**IByteBuffer::Write**](ibytebuffer-write.md) method if the seek pointer is past the current end-of-stream.</span></span>

<span data-ttu-id="8df4e-120">Si le paramètre *libNewSize* est plus petit que le flux actuel, le flux est tronqué à la taille indiquée.</span><span class="sxs-lookup"><span data-stu-id="8df4e-120">If the *libNewSize* parameter is smaller than the current stream, then the stream is truncated to the indicated size.</span></span>

<span data-ttu-id="8df4e-121">Le pointeur de recherche n’est pas affecté par la modification de la taille du flux.</span><span class="sxs-lookup"><span data-stu-id="8df4e-121">The seek pointer is not affected by the change in stream size.</span></span>

<span data-ttu-id="8df4e-122">L’appel de **IByteBuffer :: assets** peut être un moyen efficace d’obtenir un grand bloc d’espace contigu.</span><span class="sxs-lookup"><span data-stu-id="8df4e-122">Calling **IByteBuffer::SetSize** can be an effective way of trying to obtain a large chunk of contiguous space.</span></span>

## <a name="examples"></a><span data-ttu-id="8df4e-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="8df4e-123">Examples</span></span>

<span data-ttu-id="8df4e-124">L’exemple suivant illustre la définition de la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8df4e-124">The following example shows setting the buffer size.</span></span>


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
```



## <a name="requirements"></a><span data-ttu-id="8df4e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8df4e-125">Requirements</span></span>



| <span data-ttu-id="8df4e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8df4e-126">Requirement</span></span> | <span data-ttu-id="8df4e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8df4e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8df4e-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8df4e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8df4e-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8df4e-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8df4e-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8df4e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8df4e-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8df4e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8df4e-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8df4e-132">End of client support</span></span><br/>    | <span data-ttu-id="8df4e-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8df4e-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8df4e-134">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8df4e-134">End of server support</span></span><br/>    | <span data-ttu-id="8df4e-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8df4e-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8df4e-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="8df4e-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8df4e-137"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8df4e-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8df4e-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8df4e-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="8df4e-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8df4e-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8df4e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8df4e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8df4e-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8df4e-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8df4e-142">IID</span><span class="sxs-lookup"><span data-stu-id="8df4e-142">IID</span></span><br/>                      | <span data-ttu-id="8df4e-143">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="8df4e-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

