---
description: La méthode Read lit un nombre spécifié d’octets à partir de l’objet buffer dans la mémoire en commençant au pointeur de recherche actuel.
ms.assetid: 98c4de75-9ecf-4c57-9075-9d0e3675079f
title: 'IByteBuffer :: Read, méthode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Read
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0574fb640d60fd8af824ff54abce5d109675ba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210022"
---
# <a name="ibytebufferread-method"></a><span data-ttu-id="fb2cf-103">IByteBuffer :: Read, méthode</span><span class="sxs-lookup"><span data-stu-id="fb2cf-103">IByteBuffer::Read method</span></span>

<span data-ttu-id="fb2cf-104">\[La méthode de **lecture** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fb2cf-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fb2cf-106">L’interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="fb2cf-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="fb2cf-107">La méthode **Read** lit un nombre spécifié d’octets à partir de l’objet buffer dans la mémoire en commençant au pointeur de recherche actuel.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-107">The **Read** method reads a specified number of bytes from the buffer object into memory starting at the current seek pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb2cf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb2cf-108">Syntax</span></span>


```C++
HRESULT Read(
  [out] BYTE *pByte,
  [in]  LONG cb,
  [out] LONG *pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="fb2cf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb2cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb2cf-110">*pByte* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb2cf-110">*pByte* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2cf-111">Pointe vers la mémoire tampon dans laquelle les données de flux sont lues.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-111">Points to the buffer into which the stream data is read.</span></span> <span data-ttu-id="fb2cf-112">Si une erreur se produit, cette valeur est **null**.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-112">If an error occurs, this value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="fb2cf-113">*CB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb2cf-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2cf-114">Nombre d’octets de données à tenter de lire à partir de l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-114">Number of bytes of data to attempt to read from the stream object.</span></span>

</dd> <dt>

<span data-ttu-id="fb2cf-115">*pcbRead* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb2cf-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb2cf-116">Adresse d’une variable de **type long** qui reçoit le nombre réel d’octets lus à partir de l’objet de flux.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-116">Address of a **LONG** variable that receives the actual number of bytes read from the stream object.</span></span> <span data-ttu-id="fb2cf-117">Vous pouvez définir ce pointeur sur **null** pour indiquer que vous n’êtes pas intéressé par cette valeur.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="fb2cf-118">Dans ce cas, cette méthode ne fournit pas le nombre réel d’octets lus.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb2cf-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb2cf-119">Return value</span></span>

<span data-ttu-id="fb2cf-120">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-120">The return value is an **HRESULT**.</span></span> <span data-ttu-id="fb2cf-121">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-121">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb2cf-122">Notes</span><span class="sxs-lookup"><span data-stu-id="fb2cf-122">Remarks</span></span>

<span data-ttu-id="fb2cf-123">Cette méthode lit les octets de cet objet de flux dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-123">This method reads bytes from this stream object into memory.</span></span> <span data-ttu-id="fb2cf-124">L’objet de flux doit être ouvert en \_ mode de lecture STGM.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-124">The stream object must be opened in STGM\_READ mode.</span></span> <span data-ttu-id="fb2cf-125">Cette méthode ajuste le pointeur de recherche par le nombre réel d’octets lus.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-125">This method adjusts the seek pointer by the actual number of bytes read.</span></span>

<span data-ttu-id="fb2cf-126">Le nombre d’octets réellement lus est également retourné dans le paramètre *pcbRead* .</span><span class="sxs-lookup"><span data-stu-id="fb2cf-126">The number of bytes actually read is also returned in the *pcbRead* parameter.</span></span>

<span data-ttu-id="fb2cf-127">Notes pour les appelants</span><span class="sxs-lookup"><span data-stu-id="fb2cf-127">Notes to Callers</span></span>

<span data-ttu-id="fb2cf-128">Le nombre réel d’octets lus peut être inférieur au nombre d’octets demandés si une erreur se produit ou si la fin du flux est atteinte pendant l’opération de lecture.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-128">The actual number of bytes read can be fewer than the number of bytes requested if an error occurs or if the end of the stream is reached during the read operation.</span></span>

<span data-ttu-id="fb2cf-129">Certaines implémentations peuvent retourner une erreur si la fin du flux est atteinte pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-129">Some implementations might return an error if the end of the stream is reached during the read.</span></span> <span data-ttu-id="fb2cf-130">Vous devez être prêt à gérer les valeurs de retour des erreurs return ou S \_ OK à la fin des lectures de flux.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-130">You must be prepared to deal with the error return or S\_OK return values on end of stream reads.</span></span>

## <a name="examples"></a><span data-ttu-id="fb2cf-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="fb2cf-131">Examples</span></span>

<span data-ttu-id="fb2cf-132">L’exemple suivant illustre la lecture d’octets à partir de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="fb2cf-132">The following example shows reading bytes from the buffer.</span></span>


```C++
BYTE     byAtr[32];
long     lBytesRead, i;
HRESULT  hr;

// pAtr is a pointer to a previously instantiated IByteBuffer.
// It was used in an earlier call by ISCard::get_Atr.
// Use IByteBuffer::Read to access the retrieved ATR bytes.
hr = pAtr->Read(byAtr, 32, &lBytesRead);
// Use the ATR value. (This example merely displays the bytes.)
for ( i = 0; i < lBytesRead; i++)
    printf("%c", *(byAtr + i));
printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="fb2cf-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb2cf-133">Requirements</span></span>



| <span data-ttu-id="fb2cf-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb2cf-134">Requirement</span></span> | <span data-ttu-id="fb2cf-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb2cf-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2cf-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb2cf-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fb2cf-137">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb2cf-137">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fb2cf-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb2cf-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fb2cf-139">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb2cf-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb2cf-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="fb2cf-140">End of client support</span></span><br/>    | <span data-ttu-id="fb2cf-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb2cf-141">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="fb2cf-142">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="fb2cf-142">End of server support</span></span><br/>    | <span data-ttu-id="fb2cf-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb2cf-143">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="fb2cf-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb2cf-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb2cf-145"><dt>Scardssp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb2cf-145"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb2cf-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fb2cf-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb2cf-147"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fb2cf-147"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fb2cf-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fb2cf-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb2cf-149"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb2cf-149"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb2cf-150">IID</span><span class="sxs-lookup"><span data-stu-id="fb2cf-150">IID</span></span><br/>                      | <span data-ttu-id="fb2cf-151">IID \_ IByteBuffer est défini en tant que E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span><span class="sxs-lookup"><span data-stu-id="fb2cf-151">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

