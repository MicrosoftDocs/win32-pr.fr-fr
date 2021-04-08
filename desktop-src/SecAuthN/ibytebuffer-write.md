---
description: La méthode Write écrit un nombre spécifié d’octets dans l’objet de flux, en commençant au pointeur de recherche actuel.
ms.assetid: 0019cd10-8f8a-4190-bae4-e134e7b76882
title: 'IByteBuffer :: Write, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Write
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: b5f9b60a296041a18fbd850f1405088f5b0da2ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867869"
---
# <a name="ibytebufferwrite-method"></a><span data-ttu-id="1c1bb-103">IByteBuffer :: Write, méthode</span><span class="sxs-lookup"><span data-stu-id="1c1bb-103">IByteBuffer::Write method</span></span>

<span data-ttu-id="1c1bb-104">\[La méthode **Write** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-104">\[The **Write** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1c1bb-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1c1bb-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1c1bb-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="1c1bb-107">La méthode **Write** écrit un nombre spécifié d’octets dans l’objet de flux, en commençant au pointeur de recherche actuel.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-107">The **Write** method writes a specified number from bytes into the stream object starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1bb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c1bb-108">Syntax</span></span>


```C++
HRESULT Write(
  [in]  BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="1c1bb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c1bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c1bb-110">*pByte* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c1bb-110">*pByte* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1bb-111">Adresse de la mémoire tampon contenant les données à écrire dans le flux.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-111">Address of the buffer containing the data that is to be written to the stream.</span></span> <span data-ttu-id="1c1bb-112">Un pointeur valide doit être fourni pour ce paramètre même quand *CB* est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-112">A valid pointer must be provided for this parameter even when *cb* is zero.</span></span>

</dd> <dt>

<span data-ttu-id="1c1bb-113">*CB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c1bb-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1bb-114">Nombre d’octets de données à tenter d’écrire dans le flux.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-114">Number of bytes of data to attempt to write into the stream.</span></span> <span data-ttu-id="1c1bb-115">Ce paramètre peut être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-115">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1c1bb-116">*pcbWritten* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1c1bb-116">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1bb-117">Adresse d’une variable de **type long** où cette méthode écrit le nombre réel d’octets écrits dans l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-117">Address of a **LONG** variable where this method writes the actual number of bytes written to the stream object.</span></span> <span data-ttu-id="1c1bb-118">L’appelant peut affecter la **valeur null** à ce pointeur, auquel cas cette méthode ne fournit pas le nombre réel d’octets écrits.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-118">The caller can set this pointer to **NULL**, in which case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c1bb-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c1bb-119">Return value</span></span>

<span data-ttu-id="1c1bb-120">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="1c1bb-121">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c1bb-122">Notes</span><span class="sxs-lookup"><span data-stu-id="1c1bb-122">Remarks</span></span>

<span data-ttu-id="1c1bb-123">La méthode **IByteBuffer :: Write** écrit les données spécifiées dans un objet de flux.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-123">The **IByteBuffer::Write** method writes the specified data to a stream object.</span></span> <span data-ttu-id="1c1bb-124">Le pointeur de recherche est ajusté pour le nombre d’octets réellement écrits.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-124">The seek pointer is adjusted for the number of bytes actually written.</span></span> <span data-ttu-id="1c1bb-125">Le nombre d’octets réellement écrits est retourné dans le paramètre *pcbWritten* .</span><span class="sxs-lookup"><span data-stu-id="1c1bb-125">The number of bytes actually written is returned in the *pcbWritten* parameter.</span></span> <span data-ttu-id="1c1bb-126">Si le nombre d’octets est de zéro octet, l’opération d’écriture n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-126">If the byte count is zero bytes, the write operation has no effect.</span></span>

<span data-ttu-id="1c1bb-127">Si le pointeur de recherche se trouve actuellement au-delà de la fin du flux et que le nombre d’octets est différent de zéro, cette méthode augmente la taille du flux au pointeur de recherche et écrit les octets spécifiés à partir du pointeur de recherche.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-127">If the seek pointer is currently past the end of the stream and the byte count is nonzero, this method increases the size of the stream to the seek pointer and writes the specified bytes starting at the seek pointer.</span></span> <span data-ttu-id="1c1bb-128">Les octets de remplissage écrits dans le flux de données ne sont pas initialisés à une valeur particulière.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-128">The fill bytes written to the stream are not initialized to any particular value.</span></span> <span data-ttu-id="1c1bb-129">Il s’agit du même comportement que celui de la fin du fichier dans le système de fichiers FAT MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-129">This is the same as the end-of-file behavior in the MS-DOS FAT file system.</span></span>

<span data-ttu-id="1c1bb-130">Avec un nombre zéro octet et un pointeur de recherche au-delà de la fin du flux, cette méthode ne crée pas les octets de remplissage pour augmenter le flux vers le pointeur de recherche.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-130">With a zero byte count and a seek pointer past the end of the stream, this method does not create the fill bytes to increase the stream to the seek pointer.</span></span> <span data-ttu-id="1c1bb-131">Dans ce cas, vous devez appeler la méthode [**IByteBuffer :: assets**](ibytebuffer-setsize.md) pour augmenter la taille du flux et écrire les octets de remplissage.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-131">In this case, you must call the [**IByteBuffer::SetSize**](ibytebuffer-setsize.md) method to increase the size of the stream and write the fill bytes.</span></span>

<span data-ttu-id="1c1bb-132">Le paramètre *pcbWritten* peut avoir une valeur même si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-132">The *pcbWritten* parameter can have a value even if an error occurs.</span></span>

<span data-ttu-id="1c1bb-133">Dans l’implémentation fournie par COM, les objets de flux ne sont pas éparpillés.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-133">In the COM-provided implementation, stream objects are not sparse.</span></span> <span data-ttu-id="1c1bb-134">Tout octet de remplissage est finalement alloué sur le disque et affecté au flux.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-134">Any fill bytes are eventually allocated on the disk and assigned to the stream.</span></span>

## <a name="examples"></a><span data-ttu-id="1c1bb-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="1c1bb-135">Examples</span></span>

<span data-ttu-id="1c1bb-136">L’exemple suivant illustre l’écriture d’octets dans l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="1c1bb-136">The following example shows writing bytes into the stream object.</span></span>


```C++
LONG     lWrite;
HRESULT  hr;

// Write to the buffer.
// byData is an array of 64 bytes.
hr = pIByteBuff->Write(byData,
                       64,
                       &lWrite);
if (FAILED(hr))
  printf("Failed IByteBuffer::Write\n");
```



## <a name="requirements"></a><span data-ttu-id="1c1bb-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c1bb-137">Requirements</span></span>



| <span data-ttu-id="1c1bb-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c1bb-138">Requirement</span></span> | <span data-ttu-id="1c1bb-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c1bb-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1bb-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c1bb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1c1bb-141">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c1bb-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1c1bb-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c1bb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1c1bb-143">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c1bb-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1c1bb-144">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1c1bb-144">End of client support</span></span><br/>    | <span data-ttu-id="1c1bb-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1c1bb-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1c1bb-146">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1c1bb-146">End of server support</span></span><br/>    | <span data-ttu-id="1c1bb-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1c1bb-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1c1bb-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c1bb-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c1bb-149"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c1bb-149"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c1bb-150">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1c1bb-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c1bb-151"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1c1bb-151"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1c1bb-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1c1bb-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c1bb-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c1bb-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c1bb-154">IID</span><span class="sxs-lookup"><span data-stu-id="1c1bb-154">IID</span></span><br/>                      | <span data-ttu-id="1c1bb-155">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="1c1bb-155">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

