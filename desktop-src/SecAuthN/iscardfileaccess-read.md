---
description: La méthode Read lit et retourne les données spécifiées à partir d’un fichier donné.
ms.assetid: 697b8dfa-754b-46cf-ab5c-1ac1d8ae47f2
title: 'ISCardFileAccess :: Read, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: b3d66b5c6e314a4ef7a00a76fabc8660f3bf65eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203051"
---
# <a name="iscardfileaccessread-method"></a><span data-ttu-id="d38cc-103">ISCardFileAccess :: Read, méthode</span><span class="sxs-lookup"><span data-stu-id="d38cc-103">ISCardFileAccess::Read method</span></span>

<span data-ttu-id="d38cc-104">\[La méthode de **lecture** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="d38cc-104">\[The **Read** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d38cc-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d38cc-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d38cc-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d38cc-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d38cc-107">La méthode **Read** lit et retourne les données spécifiées à partir d’un fichier donné.</span><span class="sxs-lookup"><span data-stu-id="d38cc-107">The **Read** method reads and returns the specified data from a given file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38cc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d38cc-108">Syntax</span></span>


```C++
HRESULT Read(
  [in]  HSCARD_FILE  hFile,
  [in]  LONG         *lBytesToRead,
  [in]  SCARD_FLAGS  flags,
  [out] LPBYTEBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="d38cc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d38cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d38cc-110">*hFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d38cc-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d38cc-111">Handle du fichier ouvert auquel accéder.</span><span class="sxs-lookup"><span data-stu-id="d38cc-111">Handle of the open file to access.</span></span>

</dd> <dt>

<span data-ttu-id="d38cc-112">*lBytesToRead* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d38cc-112">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d38cc-113">Longueur des données à lire (en) ou nombre d’octets lus (out).</span><span class="sxs-lookup"><span data-stu-id="d38cc-113">Length of data to be read (in) or number of bytes read (out).</span></span> <span data-ttu-id="d38cc-114">Retourne la liste des fichiers sous la forme d’un tableau de BSTR.</span><span class="sxs-lookup"><span data-stu-id="d38cc-114">Returns list of files as an array of BSTRs.</span></span>

</dd> <dt>

<span data-ttu-id="d38cc-115">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d38cc-115">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d38cc-116">Spécifie si la messagerie sécurisée doit être utilisée.</span><span class="sxs-lookup"><span data-stu-id="d38cc-116">Specifies whether secure messaging should be used.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="d38cc-117">**\_ \_ messagerie sécurisée SC FL \_**</span><span class="sxs-lookup"><span data-stu-id="d38cc-117">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="d38cc-118">*ppBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d38cc-118">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d38cc-119">Objet [**IByteBuffer**](ibytebuffer.md) contenant les données lues.</span><span class="sxs-lookup"><span data-stu-id="d38cc-119">An [**IByteBuffer**](ibytebuffer.md) object containing the read data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d38cc-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d38cc-120">Return value</span></span>

<span data-ttu-id="d38cc-121">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="d38cc-121">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d38cc-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d38cc-122">Return code</span></span>                                                                                   | <span data-ttu-id="d38cc-123">Description</span><span class="sxs-lookup"><span data-stu-id="d38cc-123">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d38cc-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d38cc-124"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d38cc-125">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="d38cc-125">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d38cc-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d38cc-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d38cc-127">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="d38cc-127">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="d38cc-128"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="d38cc-128"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d38cc-129">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="d38cc-129">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="d38cc-130"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d38cc-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d38cc-131">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d38cc-131">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="d38cc-132">Notes</span><span class="sxs-lookup"><span data-stu-id="d38cc-132">Remarks</span></span>

<span data-ttu-id="d38cc-133">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="d38cc-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="d38cc-134">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="d38cc-134">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d38cc-135">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d38cc-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d38cc-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d38cc-136">Requirements</span></span>



| <span data-ttu-id="d38cc-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d38cc-137">Requirement</span></span> | <span data-ttu-id="d38cc-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="d38cc-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d38cc-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d38cc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d38cc-140">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d38cc-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d38cc-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d38cc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d38cc-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d38cc-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d38cc-143">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d38cc-143">End of client support</span></span><br/>    | <span data-ttu-id="d38cc-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d38cc-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d38cc-145">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d38cc-145">End of server support</span></span><br/>    | <span data-ttu-id="d38cc-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d38cc-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="d38cc-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d38cc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d38cc-148">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="d38cc-148">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
