---
description: La méthode GetCurrentDir retourne un chemin d’accès absolu au répertoire actuellement sélectionné.
ms.assetid: 12196143-a98a-4772-a803-d0c9b95a66e4
title: 'ISCardFileAccess :: GetCurrentDir, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetCurrentDir
api_type:
- COM
api_location: ''
ms.openlocfilehash: a779dca10a94250bf4b500585b8b50238b0267dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210755"
---
# <a name="iscardfileaccessgetcurrentdir-method"></a><span data-ttu-id="1b1d4-103">ISCardFileAccess :: GetCurrentDir, méthode</span><span class="sxs-lookup"><span data-stu-id="1b1d4-103">ISCardFileAccess::GetCurrentDir method</span></span>

<span data-ttu-id="1b1d4-104">\[La méthode **GetCurrentDir** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-104">\[The **GetCurrentDir** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1b1d4-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1b1d4-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1b1d4-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="1b1d4-107">La méthode **GetCurrentDir** retourne un chemin d’accès absolu au répertoire actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-107">The **GetCurrentDir** method returns an absolute path to the currently selected directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b1d4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b1d4-108">Syntax</span></span>


```C++
HRESULT GetCurrentDir(
  [out] BSTR *pbstrPathSpec
);
```



## <a name="parameters"></a><span data-ttu-id="1b1d4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b1d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b1d4-110">*pbstrPathSpec* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b1d4-110">*pbstrPathSpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b1d4-111">Pointeur vers un BSTR qui contiendra le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-111">Pointer to a BSTR that will contain the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b1d4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b1d4-112">Return value</span></span>

<span data-ttu-id="1b1d4-113">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="1b1d4-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1b1d4-114">Return code</span></span>                                                                                   | <span data-ttu-id="1b1d4-115">Description</span><span class="sxs-lookup"><span data-stu-id="1b1d4-115">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1b1d4-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1b1d4-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1b1d4-117">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-117">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="1b1d4-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1b1d4-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1b1d4-119">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-119">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="1b1d4-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="1b1d4-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1b1d4-121">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-121">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="1b1d4-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="1b1d4-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1b1d4-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-123">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="1b1d4-124">Notes</span><span class="sxs-lookup"><span data-stu-id="1b1d4-124">Remarks</span></span>

<span data-ttu-id="1b1d4-125">Pour modifier le répertoire actif, appelez [**ChangeDir**](iscardfileaccess-changedir.md).</span><span class="sxs-lookup"><span data-stu-id="1b1d4-125">To change the current directory, call [**ChangeDir**](iscardfileaccess-changedir.md).</span></span>

<span data-ttu-id="1b1d4-126">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="1b1d4-126">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="1b1d4-127">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="1b1d4-127">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="1b1d4-128">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="1b1d4-128">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b1d4-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b1d4-129">Requirements</span></span>



| <span data-ttu-id="1b1d4-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b1d4-130">Requirement</span></span> | <span data-ttu-id="1b1d4-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b1d4-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1b1d4-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b1d4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1b1d4-133">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b1d4-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1b1d4-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b1d4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1b1d4-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b1d4-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="1b1d4-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="1b1d4-136">End of client support</span></span><br/>    | <span data-ttu-id="1b1d4-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1b1d4-137">Windows XP</span></span><br/>                                |
| <span data-ttu-id="1b1d4-138">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="1b1d4-138">End of server support</span></span><br/>    | <span data-ttu-id="1b1d4-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1b1d4-139">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="1b1d4-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b1d4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b1d4-141">**ChangeDir**</span><span class="sxs-lookup"><span data-stu-id="1b1d4-141">**ChangeDir**</span></span>](iscardfileaccess-changedir.md)
</dt> <dt>

[<span data-ttu-id="1b1d4-142">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="1b1d4-142">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
