---
description: Crée un SAFEARRAY Automation de caractères non signés (octets).
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: 'ISCardTypeConv :: CreateSafeArray, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bc27a3f50f0740eca178787fd021f76c9b6729e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111979"
---
# <a name="iscardtypeconvcreatesafearray-method"></a><span data-ttu-id="04ab8-103">ISCardTypeConv :: CreateSafeArray, méthode</span><span class="sxs-lookup"><span data-stu-id="04ab8-103">ISCardTypeConv::CreateSafeArray method</span></span>

<span data-ttu-id="04ab8-104">\[La méthode **CreateSafeArray** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="04ab8-104">\[The **CreateSafeArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="04ab8-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="04ab8-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="04ab8-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="04ab8-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="04ab8-107">La méthode **CreateSafeArray** crée un SafeArray Automation de caractères non signés (octets).</span><span class="sxs-lookup"><span data-stu-id="04ab8-107">The **CreateSafeArray** method creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span>

## <a name="syntax"></a><span data-ttu-id="04ab8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04ab8-108">Syntax</span></span>


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a><span data-ttu-id="04ab8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04ab8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04ab8-110">*nAllocSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04ab8-110">*nAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04ab8-111">Taille en octets de la mémoire à allouer pour le tableau.</span><span class="sxs-lookup"><span data-stu-id="04ab8-111">Size in bytes of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="04ab8-112">*ppArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04ab8-112">*ppArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04ab8-113">Pointeur vers l’objet SAFEARRAY à retourner.</span><span class="sxs-lookup"><span data-stu-id="04ab8-113">Pointer to the SAFEARRAY object to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04ab8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04ab8-114">Return value</span></span>

<span data-ttu-id="04ab8-115">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="04ab8-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="04ab8-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="04ab8-116">Return code</span></span>                                                                                   | <span data-ttu-id="04ab8-117">Description</span><span class="sxs-lookup"><span data-stu-id="04ab8-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04ab8-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04ab8-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="04ab8-119">Mémoire allouée avec succès.</span><span class="sxs-lookup"><span data-stu-id="04ab8-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="04ab8-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="04ab8-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="04ab8-121">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="04ab8-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="04ab8-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="04ab8-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="04ab8-123">Mémoire libre insuffisante pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="04ab8-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="04ab8-124">Notes</span><span class="sxs-lookup"><span data-stu-id="04ab8-124">Remarks</span></span>

<span data-ttu-id="04ab8-125">Pour créer un tableau d’octets C/C++ classique, appelez [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span><span class="sxs-lookup"><span data-stu-id="04ab8-125">To create a typical C/C++ byte array, call [**CreateByteArray**](iscardtypeconv-createbytearray.md).</span></span>

<span data-ttu-id="04ab8-126">Pour créer une mémoire tampon universelle d’octets mappés dans un objet **IStream** ([**IByteBuffer**](ibytebuffer.md)), appelez [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="04ab8-126">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="04ab8-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04ab8-127">Requirements</span></span>



| <span data-ttu-id="04ab8-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04ab8-128">Requirement</span></span> | <span data-ttu-id="04ab8-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="04ab8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04ab8-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04ab8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="04ab8-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04ab8-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="04ab8-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04ab8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="04ab8-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04ab8-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="04ab8-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="04ab8-134">End of client support</span></span><br/>    | <span data-ttu-id="04ab8-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="04ab8-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="04ab8-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="04ab8-136">End of server support</span></span><br/>    | <span data-ttu-id="04ab8-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04ab8-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="04ab8-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="04ab8-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="04ab8-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="04ab8-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="04ab8-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="04ab8-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="04ab8-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="04ab8-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="04ab8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="04ab8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04ab8-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04ab8-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="04ab8-144">IID</span><span class="sxs-lookup"><span data-stu-id="04ab8-144">IID</span></span><br/>                      | <span data-ttu-id="04ab8-145">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="04ab8-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="04ab8-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04ab8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ab8-147">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="04ab8-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="04ab8-148">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="04ab8-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="04ab8-149">**CreateByteArray**</span><span class="sxs-lookup"><span data-stu-id="04ab8-149">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)
</dt> <dt>

[<span data-ttu-id="04ab8-150">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="04ab8-150">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
