---
description: La méthode CopyTo copie un nombre spécifié d’octets à partir du pointeur de recherche actuel dans l’objet vers le pointeur de recherche actuel dans un autre objet.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'IByteBuffer :: CopyTo, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210027"
---
# <a name="ibytebuffercopyto-method"></a><span data-ttu-id="ea211-103">IByteBuffer :: CopyTo, méthode</span><span class="sxs-lookup"><span data-stu-id="ea211-103">IByteBuffer::CopyTo method</span></span>

<span data-ttu-id="ea211-104">\[La méthode **CopyTo** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="ea211-104">\[The **CopyTo** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ea211-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ea211-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ea211-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="ea211-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="ea211-107">La méthode **CopyTo** copie un nombre spécifié d’octets à partir du pointeur de recherche actuel dans l’objet vers le pointeur de recherche actuel dans un autre objet.</span><span class="sxs-lookup"><span data-stu-id="ea211-107">The **CopyTo** method copies a specified number of bytes from the current seek pointer in the object to the current seek pointer in another object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea211-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea211-108">Syntax</span></span>


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="ea211-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea211-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea211-110">*pByteBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea211-110">*pByteBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea211-111">Pointe vers le flux de destination.</span><span class="sxs-lookup"><span data-stu-id="ea211-111">Points to the destination stream.</span></span> <span data-ttu-id="ea211-112">Le flux vers lequel pointe *pByteBuffer* peut être un nouveau flux ou un clone du flux source.</span><span class="sxs-lookup"><span data-stu-id="ea211-112">The stream pointed to by *pByteBuffer* can be a new stream or a clone of the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="ea211-113">*CB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea211-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea211-114">Nombre d’octets à copier à partir du flux source.</span><span class="sxs-lookup"><span data-stu-id="ea211-114">Number of bytes to copy from the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="ea211-115">*pcbRead* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ea211-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea211-116">Pointeur vers l’emplacement où cette méthode écrit le nombre réel d’octets lus à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="ea211-116">Pointer to the location where this method writes the actual number of bytes read from the source.</span></span> <span data-ttu-id="ea211-117">Vous pouvez définir ce pointeur sur **null** pour indiquer que vous n’êtes pas intéressé par cette valeur.</span><span class="sxs-lookup"><span data-stu-id="ea211-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="ea211-118">Dans ce cas, cette méthode ne fournit pas le nombre réel d’octets lus.</span><span class="sxs-lookup"><span data-stu-id="ea211-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="ea211-119">*pcbWritten* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ea211-119">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea211-120">Pointeur vers l’emplacement où cette méthode écrit le nombre réel d’octets écrits dans la destination.</span><span class="sxs-lookup"><span data-stu-id="ea211-120">Pointer to the location where this method writes the actual number of bytes written to the destination.</span></span> <span data-ttu-id="ea211-121">Vous pouvez définir ce pointeur sur **null** pour indiquer que vous n’êtes pas intéressé par cette valeur.</span><span class="sxs-lookup"><span data-stu-id="ea211-121">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="ea211-122">Dans ce cas, cette méthode ne fournit pas le nombre réel d’octets écrits.</span><span class="sxs-lookup"><span data-stu-id="ea211-122">In this case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea211-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea211-123">Return value</span></span>

<span data-ttu-id="ea211-124">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ea211-124">The return value is an **HRESULT**.</span></span> <span data-ttu-id="ea211-125">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="ea211-125">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea211-126">Notes</span><span class="sxs-lookup"><span data-stu-id="ea211-126">Remarks</span></span>

<span data-ttu-id="ea211-127">Cette méthode copie les octets spécifiés d’un flux vers un autre.</span><span class="sxs-lookup"><span data-stu-id="ea211-127">This method copies the specified bytes from one stream to another.</span></span> <span data-ttu-id="ea211-128">Elle peut également être utilisée pour copier un flux vers lui-même.</span><span class="sxs-lookup"><span data-stu-id="ea211-128">It can also be used to copy a stream to itself.</span></span> <span data-ttu-id="ea211-129">Le pointeur de recherche dans chaque instance de flux est ajusté pour le nombre d’octets lus ou écrits.</span><span class="sxs-lookup"><span data-stu-id="ea211-129">The seek pointer in each stream instance is adjusted for the number of bytes read or written.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea211-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea211-130">Requirements</span></span>



| <span data-ttu-id="ea211-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea211-131">Requirement</span></span> | <span data-ttu-id="ea211-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea211-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea211-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea211-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ea211-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea211-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ea211-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea211-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ea211-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea211-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ea211-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ea211-137">End of client support</span></span><br/>    | <span data-ttu-id="ea211-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ea211-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="ea211-139">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="ea211-139">End of server support</span></span><br/>    | <span data-ttu-id="ea211-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="ea211-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="ea211-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea211-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea211-142"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea211-142"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea211-143">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ea211-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="ea211-144"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ea211-144"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ea211-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ea211-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea211-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea211-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ea211-147">IID</span><span class="sxs-lookup"><span data-stu-id="ea211-147">IID</span></span><br/>                      | <span data-ttu-id="ea211-148">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="ea211-148">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

