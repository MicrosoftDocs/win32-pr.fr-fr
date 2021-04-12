---
description: Convertit une mémoire tampon universelle d’octets (objet IStream) en un tableau d’octets C/C++ standard.
ms.assetid: f5b14096-d848-4de9-a5c3-bb60af9044a2
title: 'ISCardTypeConv :: ConvertByteBufferToByteArray, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 7eed6758373aebf08863669b5b81909fca1c0840
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209708"
---
# <a name="iscardtypeconvconvertbytebuffertobytearray-method"></a><span data-ttu-id="dcf5c-103">ISCardTypeConv :: ConvertByteBufferToByteArray, méthode</span><span class="sxs-lookup"><span data-stu-id="dcf5c-103">ISCardTypeConv::ConvertByteBufferToByteArray method</span></span>

<span data-ttu-id="dcf5c-104">\[La méthode **ConvertByteBufferToByteArray** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="dcf5c-104">\[The **ConvertByteBufferToByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dcf5c-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dcf5c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dcf5c-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="dcf5c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dcf5c-107">La méthode **ConvertByteBufferToByteArray** convertit une mémoire tampon universelle d’octets (objet **IStream** ) en un tableau d’octets C/C++ standard.</span><span class="sxs-lookup"><span data-stu-id="dcf5c-107">The **ConvertByteBufferToByteArray** method converts a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcf5c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dcf5c-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToByteArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPBYTEARRAY  *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="dcf5c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dcf5c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf5c-110">*pbyBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dcf5c-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf5c-111">Pointeur vers l’objet **IStream** à convertir.</span><span class="sxs-lookup"><span data-stu-id="dcf5c-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="dcf5c-112">*ppArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dcf5c-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf5c-113">Pointeur vers le tableau d’octets à retourner.</span><span class="sxs-lookup"><span data-stu-id="dcf5c-113">Pointer to the array of bytes to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf5c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dcf5c-114">Return value</span></span>

<span data-ttu-id="dcf5c-115">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="dcf5c-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="dcf5c-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dcf5c-116">Return code</span></span>                                                                                   | <span data-ttu-id="dcf5c-117">Description</span><span class="sxs-lookup"><span data-stu-id="dcf5c-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dcf5c-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5c-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dcf5c-119">Mémoire allouée avec succès.</span><span class="sxs-lookup"><span data-stu-id="dcf5c-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="dcf5c-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dcf5c-121">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="dcf5c-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="dcf5c-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5c-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dcf5c-123">Un paramètre de type pointeur était incorrect.</span><span class="sxs-lookup"><span data-stu-id="dcf5c-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="dcf5c-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5c-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dcf5c-125">Mémoire libre insuffisante pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="dcf5c-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="dcf5c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcf5c-126">Requirements</span></span>



| <span data-ttu-id="dcf5c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcf5c-127">Requirement</span></span> | <span data-ttu-id="dcf5c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcf5c-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf5c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcf5c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf5c-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcf5c-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dcf5c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcf5c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf5c-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcf5c-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dcf5c-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="dcf5c-133">End of client support</span></span><br/>    | <span data-ttu-id="dcf5c-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dcf5c-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dcf5c-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="dcf5c-135">End of server support</span></span><br/>    | <span data-ttu-id="dcf5c-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dcf5c-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dcf5c-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcf5c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcf5c-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5c-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="dcf5c-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="dcf5c-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="dcf5c-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5c-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dcf5c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="dcf5c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcf5c-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcf5c-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dcf5c-143">IID</span><span class="sxs-lookup"><span data-stu-id="dcf5c-143">IID</span></span><br/>                      | <span data-ttu-id="dcf5c-144">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="dcf5c-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="dcf5c-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dcf5c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf5c-146">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="dcf5c-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="dcf5c-147">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="dcf5c-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
