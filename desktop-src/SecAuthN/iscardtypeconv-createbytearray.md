---
description: Crée un tableau d’octets C/C++ standard.
ms.assetid: 915e8cca-2a0f-409e-a6df-54fa73bdc305
title: 'ISCardTypeConv :: CreateByteArray, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae253af1b24433987baf66364519a3761f7e0365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115611"
---
# <a name="iscardtypeconvcreatebytearray-method"></a><span data-ttu-id="6dfb9-103">ISCardTypeConv :: CreateByteArray, méthode</span><span class="sxs-lookup"><span data-stu-id="6dfb9-103">ISCardTypeConv::CreateByteArray method</span></span>

<span data-ttu-id="6dfb9-104">\[La méthode **CreateByteArray** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-104">\[The **CreateByteArray** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6dfb9-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6dfb9-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6dfb9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6dfb9-107">La méthode **CreateByteArray** crée un tableau d’octets C/C++ standard.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-107">The **CreateByteArray** method creates a typical C/C++ byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dfb9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6dfb9-108">Syntax</span></span>


```C++
HRESULT CreateByteArray(
  [in]  DWORD  dwAllocSize,
  [out] LPBYTE *ppbyArray
);
```



## <a name="parameters"></a><span data-ttu-id="6dfb9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6dfb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dfb9-110">*dwAllocSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6dfb9-110">*dwAllocSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfb9-111">Taille (en octets) de la mémoire à allouer au tableau.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-111">Size (in bytes) of the memory to be allocated for the array.</span></span>

</dd> <dt>

<span data-ttu-id="6dfb9-112">*ppbyArray* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6dfb9-112">*ppbyArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dfb9-113">Pointeur vers le tableau d’octets à retourner.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-113">Pointer to the byte array to be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dfb9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6dfb9-114">Return value</span></span>

<span data-ttu-id="6dfb9-115">La méthode retourne l’une des valeurs possibles suivantes :</span><span class="sxs-lookup"><span data-stu-id="6dfb9-115">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="6dfb9-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6dfb9-116">Return code</span></span>                                                                                   | <span data-ttu-id="6dfb9-117">Description</span><span class="sxs-lookup"><span data-stu-id="6dfb9-117">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6dfb9-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6dfb9-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6dfb9-119">Mémoire allouée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-119">Memory allocated successfully.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6dfb9-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6dfb9-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6dfb9-121">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-121">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |
| <dl> <span data-ttu-id="6dfb9-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="6dfb9-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6dfb9-123">Mémoire libre insuffisante pour satisfaire la demande.</span><span class="sxs-lookup"><span data-stu-id="6dfb9-123">Not enough free memory to satisfy request.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="6dfb9-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6dfb9-124">Remarks</span></span>

<span data-ttu-id="6dfb9-125">Pour créer une mémoire tampon universelle d’octets mappés dans un objet **IStream** ([**IByteBuffer**](ibytebuffer.md)), appelez [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="6dfb9-125">To create a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object, call [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md).</span></span>

<span data-ttu-id="6dfb9-126">Pour créer un SAFEARRAY Automation de caractères non signés (octets), appelez [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span><span class="sxs-lookup"><span data-stu-id="6dfb9-126">To create an Automation SAFEARRAY of unsigned characters (bytes), call [**CreateSafeArray**](iscardtypeconv-createsafearray.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6dfb9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6dfb9-127">Requirements</span></span>



| <span data-ttu-id="6dfb9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6dfb9-128">Requirement</span></span> | <span data-ttu-id="6dfb9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6dfb9-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfb9-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dfb9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6dfb9-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6dfb9-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6dfb9-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dfb9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6dfb9-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6dfb9-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6dfb9-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6dfb9-134">End of client support</span></span><br/>    | <span data-ttu-id="6dfb9-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6dfb9-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6dfb9-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="6dfb9-136">End of server support</span></span><br/>    | <span data-ttu-id="6dfb9-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6dfb9-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6dfb9-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="6dfb9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dfb9-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dfb9-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="6dfb9-140">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6dfb9-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="6dfb9-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6dfb9-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6dfb9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6dfb9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dfb9-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dfb9-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6dfb9-144">IID</span><span class="sxs-lookup"><span data-stu-id="6dfb9-144">IID</span></span><br/>                      | <span data-ttu-id="6dfb9-145">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6dfb9-145">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="6dfb9-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dfb9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dfb9-147">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="6dfb9-147">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="6dfb9-148">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="6dfb9-148">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> <dt>

[<span data-ttu-id="6dfb9-149">**CreateByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="6dfb9-149">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)
</dt> <dt>

[<span data-ttu-id="6dfb9-150">**CreateSafeArray**</span><span class="sxs-lookup"><span data-stu-id="6dfb9-150">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
