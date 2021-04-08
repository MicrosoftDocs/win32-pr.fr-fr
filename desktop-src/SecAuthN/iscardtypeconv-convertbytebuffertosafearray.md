---
description: Convertit une mémoire tampon universelle d’octets (objet IStream) en un SAFEARRAY de type unsigned char (Byte).
ms.assetid: b8d052e8-2f36-42cf-b88c-ace215a2fc68
title: 'ISCardTypeConv :: ConvertByteBufferToSafeArray, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteBufferToSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: eb6f646df60ab505c41c45bea34fd2d59aa3bb4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757282"
---
# <a name="iscardtypeconvconvertbytebuffertosafearray-method"></a><span data-ttu-id="df647-103">ISCardTypeConv :: ConvertByteBufferToSafeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="df647-103">ISCardTypeConv::ConvertByteBufferToSafeArray method</span></span>

<span data-ttu-id="df647-104">\[La méthode **ConvertByteBufferToSafeArray** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="df647-104">\[The **ConvertByteBufferToSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="df647-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="df647-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="df647-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="df647-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="df647-107">La méthode **ConvertByteBufferToSafeArray** convertit une mémoire tampon universelle d’octets (objet **IStream** ) en un SafeArray de type unsigned char (Byte).</span><span class="sxs-lookup"><span data-stu-id="df647-107">The **ConvertByteBufferToSafeArray** method converts a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span>

## <a name="syntax"></a><span data-ttu-id="df647-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df647-108">Syntax</span></span>


```C++
HRESULT ConvertByteBufferToSafeArray(
  [in]  LPBYTEBUFFER pbyBuffer,
  [out] LPSAFEARRAY  *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="df647-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df647-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df647-110">*pbyBuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df647-110">*pbyBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df647-111">Pointeur vers l’objet **IStream** à convertir.</span><span class="sxs-lookup"><span data-stu-id="df647-111">Pointer to the **IStream** object to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="df647-112">*ppbyArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="df647-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df647-113">Pointeur vers le SAFEARRAY à retourner.</span><span class="sxs-lookup"><span data-stu-id="df647-113">Pointer to the SAFEARRAY to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df647-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df647-114">Return value</span></span>

<span data-ttu-id="df647-115">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="df647-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="df647-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="df647-116">Return code</span></span>                                                                                   | <span data-ttu-id="df647-117">Description</span><span class="sxs-lookup"><span data-stu-id="df647-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="df647-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df647-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="df647-119">Mémoire allouée avec succès.</span><span class="sxs-lookup"><span data-stu-id="df647-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="df647-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="df647-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="df647-121">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="df647-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="df647-122"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="df647-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="df647-123">Un paramètre de type pointeur était incorrect.</span><span class="sxs-lookup"><span data-stu-id="df647-123">A parameter of pointer type was incorrect.</span></span><br/>                                            |
| <dl> <span data-ttu-id="df647-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="df647-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="df647-125">Mémoire libre insuffisante pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="df647-125">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="df647-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df647-126">Requirements</span></span>



| <span data-ttu-id="df647-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df647-127">Requirement</span></span> | <span data-ttu-id="df647-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="df647-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df647-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df647-129">Minimum supported client</span></span><br/> | <span data-ttu-id="df647-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df647-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="df647-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df647-131">Minimum supported server</span></span><br/> | <span data-ttu-id="df647-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df647-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="df647-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="df647-133">End of client support</span></span><br/>    | <span data-ttu-id="df647-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="df647-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="df647-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="df647-135">End of server support</span></span><br/>    | <span data-ttu-id="df647-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="df647-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="df647-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="df647-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="df647-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="df647-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="df647-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="df647-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="df647-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="df647-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="df647-141">DLL</span><span class="sxs-lookup"><span data-stu-id="df647-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df647-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df647-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="df647-143">IID</span><span class="sxs-lookup"><span data-stu-id="df647-143">IID</span></span><br/>                      | <span data-ttu-id="df647-144">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="df647-144">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="df647-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df647-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df647-146">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="df647-146">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="df647-147">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="df647-147">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
