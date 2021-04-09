---
description: La méthode Seek remplace le pointeur de recherche par un nouvel emplacement relatif au début de la mémoire tampon, à la fin de la mémoire tampon ou au pointeur de recherche actuel.
ms.assetid: 3541f3dd-7b92-4f72-89b7-4e04e007aaa3
title: 'IByteBuffer :: Seek, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Seek
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eacfedc3ed23a7a4cf1f60e6c6ac21936c3c94f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867870"
---
# <a name="ibytebufferseek-method"></a><span data-ttu-id="30c91-103">IByteBuffer :: Seek, méthode</span><span class="sxs-lookup"><span data-stu-id="30c91-103">IByteBuffer::Seek method</span></span>

<span data-ttu-id="30c91-104">\[La méthode **Seek** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="30c91-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="30c91-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="30c91-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="30c91-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="30c91-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="30c91-107">La méthode **Seek** remplace le pointeur de recherche par un nouvel emplacement relatif au début de la mémoire tampon, à la fin de la mémoire tampon ou au pointeur de recherche actuel.</span><span class="sxs-lookup"><span data-stu-id="30c91-107">The **Seek** method changes the seek pointer to a new location relative to the beginning of the buffer, to the end of the buffer, or to the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c91-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30c91-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in]  LONG dlibMove,
  [in]  LONG dwOrigin,
  [out] LONG *plibNewPosition
);
```



## <a name="parameters"></a><span data-ttu-id="30c91-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30c91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c91-110">*dlibMove* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30c91-110">*dlibMove* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c91-111">Déplacement à ajouter à l’emplacement indiqué par *dwOrigin*.</span><span class="sxs-lookup"><span data-stu-id="30c91-111">Displacement to be added to the location indicated by *dwOrigin*.</span></span> <span data-ttu-id="30c91-112">Si *dwOrigin* est \_ défini pour la recherche de flux \_ , il est interprété comme une valeur non signée plutôt que comme étant signé.</span><span class="sxs-lookup"><span data-stu-id="30c91-112">If *dwOrigin* is STREAM\_SEEK\_SET, this is interpreted as an unsigned value rather than signed.</span></span>

</dd> <dt>

<span data-ttu-id="30c91-113">*dwOrigin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30c91-113">*dwOrigin* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c91-114">Spécifie l’origine du déplacement spécifié dans *dlibMove*.</span><span class="sxs-lookup"><span data-stu-id="30c91-114">Specifies the origin for the displacement specified in *dlibMove*.</span></span> <span data-ttu-id="30c91-115">L’origine peut être l’une des valeurs du tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="30c91-115">The origin can be one of the values in the following table.</span></span>



| <span data-ttu-id="30c91-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="30c91-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="30c91-117">Signification</span><span class="sxs-lookup"><span data-stu-id="30c91-117">Meaning</span></span>                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STREAM_SEEK_SET"></span><span id="stream_seek_set"></span><dl> <span data-ttu-id="30c91-118"><dt>**\_jeu de recherche de flux \_**</dt></span><span class="sxs-lookup"><span data-stu-id="30c91-118"><dt>**STREAM\_SEEK\_SET**</dt></span></span> </dl> | <span data-ttu-id="30c91-119">Le nouveau pointeur de recherche est un décalage par rapport au début du flux.</span><span class="sxs-lookup"><span data-stu-id="30c91-119">The new seek pointer is an offset relative to the beginning of the stream.</span></span> <span data-ttu-id="30c91-120">Dans ce cas, le paramètre *dlibMove* est la nouvelle position de recherche par rapport au début du flux.</span><span class="sxs-lookup"><span data-stu-id="30c91-120">In this case, the *dlibMove* parameter is the new seek position relative to the beginning of the stream.</span></span><br/> |
| <span id="STREAM_SEEK_CUR"></span><span id="stream_seek_cur"></span><dl> <span data-ttu-id="30c91-121"><dt>**STREAM \_ Seek \_ cur**</dt></span><span class="sxs-lookup"><span data-stu-id="30c91-121"><dt>**STREAM\_SEEK\_CUR**</dt></span></span> </dl> | <span data-ttu-id="30c91-122">Le nouveau pointeur de recherche est un décalage par rapport à l’emplacement du pointeur de recherche actuel.</span><span class="sxs-lookup"><span data-stu-id="30c91-122">The new seek pointer is an offset relative to the current seek pointer location.</span></span> <span data-ttu-id="30c91-123">Dans ce cas, le paramètre *dlibMove* est le déplacement signé de la position de la recherche actuelle.</span><span class="sxs-lookup"><span data-stu-id="30c91-123">In this case, the *dlibMove* parameter is the signed displacement from the current seek position.</span></span><br/>  |
| <span id="STREAM_SEEK_END"></span><span id="stream_seek_end"></span><dl> <span data-ttu-id="30c91-124"><dt>**fin de la recherche de flux \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="30c91-124"><dt>**STREAM\_SEEK\_END**</dt></span></span> </dl> | <span data-ttu-id="30c91-125">Le nouveau pointeur de recherche est un décalage par rapport à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="30c91-125">The new seek pointer is an offset relative to the end of the stream.</span></span> <span data-ttu-id="30c91-126">Dans ce cas, le paramètre *dlibMove* est la nouvelle position de recherche par rapport à la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="30c91-126">In this case, the *dlibMove* parameter is the new seek position relative to the end of the stream.</span></span><br/>             |



 

</dd> <dt>

<span data-ttu-id="30c91-127">*plibNewPosition* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="30c91-127">*plibNewPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30c91-128">Pointeur vers l’emplacement où cette méthode écrit la valeur du nouveau pointeur de recherche à partir du début du flux.</span><span class="sxs-lookup"><span data-stu-id="30c91-128">Pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream.</span></span> <span data-ttu-id="30c91-129">Vous pouvez définir ce pointeur sur **null** pour indiquer que vous n’êtes pas intéressé par cette valeur.</span><span class="sxs-lookup"><span data-stu-id="30c91-129">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="30c91-130">Dans ce cas, cette méthode ne fournit pas le nouveau pointeur de recherche.</span><span class="sxs-lookup"><span data-stu-id="30c91-130">In this case, this method does not provide the new seek pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c91-131">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30c91-131">Return value</span></span>

<span data-ttu-id="30c91-132">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="30c91-132">The return value is an **HRESULT**.</span></span> <span data-ttu-id="30c91-133">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="30c91-133">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="30c91-134">Notes</span><span class="sxs-lookup"><span data-stu-id="30c91-134">Remarks</span></span>

<span data-ttu-id="30c91-135">La méthode **Seek** modifie le pointeur de recherche, de sorte que les opérations de lecture et d’écriture suivantes peuvent avoir lieu à un emplacement différent dans l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="30c91-135">The **Seek** method changes the seek pointer so subsequent read and write operations can take place at a different location in the stream object.</span></span> <span data-ttu-id="30c91-136">Il s’agit d’une erreur de recherche avant le début du flux.</span><span class="sxs-lookup"><span data-stu-id="30c91-136">It is an error to seek before the beginning of the stream.</span></span> <span data-ttu-id="30c91-137">Toutefois, il ne s’agit pas d’une erreur de recherche au-delà de la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="30c91-137">It is not, however, an error to seek past the end of the stream.</span></span> <span data-ttu-id="30c91-138">La recherche au-delà de la fin du flux est utile pour les opérations d’écriture suivantes, car le flux à ce moment sera étendu à la position de recherche immédiatement avant la fin de l’opération d’écriture.</span><span class="sxs-lookup"><span data-stu-id="30c91-138">Seeking past the end of the stream is useful for subsequent write operations, as the stream will at that time be extended to the seek position immediately before the write operation is done.</span></span>

<span data-ttu-id="30c91-139">Vous pouvez également utiliser cette méthode pour obtenir la valeur actuelle du pointeur de recherche en appelant cette méthode avec le paramètre *dwOrigin* défini sur Stream \_ Seek \_ cur et le paramètre *dlibMove* défini sur zéro, de sorte que le pointeur de recherche n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="30c91-139">You can also use this method to obtain the current value of the seek pointer by calling this method with the *dwOrigin* parameter set to STREAM\_SEEK\_CUR and the *dlibMove* parameter set to zero so the seek pointer is not changed.</span></span> <span data-ttu-id="30c91-140">Le pointeur de recherche actuel est retourné dans le paramètre *plibNewPosition* .</span><span class="sxs-lookup"><span data-stu-id="30c91-140">The current seek pointer is returned in the *plibNewPosition* parameter.</span></span>

## <a name="examples"></a><span data-ttu-id="30c91-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="30c91-141">Examples</span></span>

<span data-ttu-id="30c91-142">L’exemple suivant illustre le positionnement du pointeur de recherche vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="30c91-142">The following example shows positioning the seek pointer to a new location.</span></span>


```C++
LONG     lNewPos;
HRESULT  hr;

// Change the seek pointer.
hr = pIByteBuff->Seek(5, STREAM_SEEK_SET, &lNewPos);
if (FAILED(hr))
  printf("Failed IByteBuffer::Seek\n");
else
  printf("New position is %x\n", lNewPos);
```



## <a name="requirements"></a><span data-ttu-id="30c91-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30c91-143">Requirements</span></span>



| <span data-ttu-id="30c91-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30c91-144">Requirement</span></span> | <span data-ttu-id="30c91-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="30c91-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30c91-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c91-146">Minimum supported client</span></span><br/> | <span data-ttu-id="30c91-147">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30c91-147">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="30c91-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c91-148">Minimum supported server</span></span><br/> | <span data-ttu-id="30c91-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30c91-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="30c91-150">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="30c91-150">End of client support</span></span><br/>    | <span data-ttu-id="30c91-151">Windows XP</span><span class="sxs-lookup"><span data-stu-id="30c91-151">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="30c91-152">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="30c91-152">End of server support</span></span><br/>    | <span data-ttu-id="30c91-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="30c91-153">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="30c91-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="30c91-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c91-155"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="30c91-155"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="30c91-156">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="30c91-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="30c91-157"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="30c91-157"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="30c91-158">DLL</span><span class="sxs-lookup"><span data-stu-id="30c91-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30c91-159"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30c91-159"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="30c91-160">IID</span><span class="sxs-lookup"><span data-stu-id="30c91-160">IID</span></span><br/>                      | <span data-ttu-id="30c91-161">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="30c91-161">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

