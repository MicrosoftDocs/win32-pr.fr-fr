---
description: Détermine la taille, en octets, de l’interface COM IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: 'ISCardTypeConv :: SizeOfIStream, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 603a01dc6cb4727d59a7fb82c3270c08a495f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523248"
---
# <a name="iscardtypeconvsizeofistream-method"></a><span data-ttu-id="cf647-103">ISCardTypeConv :: SizeOfIStream, méthode</span><span class="sxs-lookup"><span data-stu-id="cf647-103">ISCardTypeConv::SizeOfIStream method</span></span>

<span data-ttu-id="cf647-104">\[La méthode **SizeOfIStream** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="cf647-104">\[The **SizeOfIStream** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cf647-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cf647-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cf647-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="cf647-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cf647-107">La méthode **SizeOfIStream** détermine la taille, en octets, de l’interface com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="cf647-107">The **SizeOfIStream** method determines the size, in bytes, of the **IStream** COM interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf647-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf647-108">Syntax</span></span>


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a><span data-ttu-id="cf647-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf647-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf647-110">*pStrm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cf647-110">*pStrm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf647-111">Pointeur vers l’interface com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="cf647-111">A pointer to the **IStream** COM interface.</span></span>

</dd> <dt>

<span data-ttu-id="cf647-112">*puliSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cf647-112">*puliSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf647-113">Pointeur vers l’entier non signé long qui peut contenir l’intégralité de la valeur sizeof 64 bits de l’interface com **IStream** .</span><span class="sxs-lookup"><span data-stu-id="cf647-113">A pointer to the unsigned large integer that can hold the entire 64-bit sizeof value of the **IStream** COM interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf647-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf647-114">Return value</span></span>

<span data-ttu-id="cf647-115">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="cf647-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cf647-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cf647-116">Return code</span></span>                                                                                  | <span data-ttu-id="cf647-117">Description</span><span class="sxs-lookup"><span data-stu-id="cf647-117">Description</span></span>                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf647-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf647-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cf647-119">La fonction a réussi et *\* puliSize* est la taille, en octets, de l’interface com IStream.</span><span class="sxs-lookup"><span data-stu-id="cf647-119">The function succeeded and *\*puliSize* is the size, in bytes, of the IStream COM interface.</span></span><br/> |
| <dl> <span data-ttu-id="cf647-120"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="cf647-120"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="cf647-121">Une erreur non spécifiée s’est produite.</span><span class="sxs-lookup"><span data-stu-id="cf647-121">Unspecified failure occurred.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="cf647-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cf647-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="cf647-123">Le paramètre *puliSize* est incorrect.</span><span class="sxs-lookup"><span data-stu-id="cf647-123">The *puliSize* parameter is incorrect.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="cf647-124"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="cf647-124"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="cf647-125">Le paramètre *pStrm* est incorrect.</span><span class="sxs-lookup"><span data-stu-id="cf647-125">The *pStrm* parameter is incorrect.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="cf647-126"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="cf647-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="cf647-127">Une erreur inattendue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="cf647-127">Unexpected error occurred.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="cf647-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf647-128">Requirements</span></span>



| <span data-ttu-id="cf647-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf647-129">Requirement</span></span> | <span data-ttu-id="cf647-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf647-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf647-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf647-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cf647-132">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf647-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cf647-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf647-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cf647-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf647-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf647-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="cf647-135">End of client support</span></span><br/>    | <span data-ttu-id="cf647-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cf647-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cf647-137">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="cf647-137">End of server support</span></span><br/>    | <span data-ttu-id="cf647-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cf647-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cf647-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="cf647-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf647-140"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf647-140"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf647-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cf647-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="cf647-142"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cf647-142"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cf647-143">DLL</span><span class="sxs-lookup"><span data-stu-id="cf647-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf647-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf647-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cf647-145">IID</span><span class="sxs-lookup"><span data-stu-id="cf647-145">IID</span></span><br/>                      | <span data-ttu-id="cf647-146">IID \_ ISCardTypeConv est défini en tant que 53B6AA63-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cf647-146">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cf647-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf647-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf647-148">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="cf647-148">**ISCardTypeConv**</span></span>](iscardtypeconv.md)
</dt> <dt>

[<span data-ttu-id="cf647-149">Valeurs de retour de carte à puce</span><span class="sxs-lookup"><span data-stu-id="cf647-149">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
