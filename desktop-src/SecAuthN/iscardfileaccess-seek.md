---
description: La méthode Seek sélectionne l’objet à partir duquel l’accès (lecture/écriture) sera effectué.
ms.assetid: 9e06df70-6415-46dd-b34f-59614d1cbee7
title: 'ISCardFileAccess :: Seek, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Seek
api_type:
- COM
api_location: ''
ms.openlocfilehash: c0d23925ba1c38a05e15bea5e6ee63b3a1c87125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756880"
---
# <a name="iscardfileaccessseek-method"></a><span data-ttu-id="2ef0d-103">ISCardFileAccess :: Seek, méthode</span><span class="sxs-lookup"><span data-stu-id="2ef0d-103">ISCardFileAccess::Seek method</span></span>

<span data-ttu-id="2ef0d-104">\[La méthode **Seek** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-104">\[The **Seek** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2ef0d-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ef0d-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="2ef0d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="2ef0d-107">La méthode **Seek** sélectionne l’objet à partir duquel l’accès (lecture/écriture) sera effectué.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-107">The **Seek** method selects the object from which (read/write) access will be done.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef0d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ef0d-108">Syntax</span></span>


```C++
HRESULT Seek(
  [in] HSCARD_FILE hFile,
  [in] SEEKTYPE    *Seek,
  [in] LONG        lOffset 
);
```



## <a name="parameters"></a><span data-ttu-id="2ef0d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ef0d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef0d-110">*hFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ef0d-110">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef0d-111">Handle du fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-111">Handle of the open file.</span></span>

</dd> <dt>

<span data-ttu-id="2ef0d-112">*Recherche* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ef0d-112">*Seek* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef0d-113">Emplacement où la recherche doit commencer.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-113">Location where the seek should begin.</span></span>



| <span data-ttu-id="2ef0d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ef0d-114">Value</span></span>                                                                                                | <span data-ttu-id="2ef0d-115">Signification</span><span class="sxs-lookup"><span data-stu-id="2ef0d-115">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="2ef0d-116"><dt>SC \_ Seek \_ depuis le \_ début</dt></span><span class="sxs-lookup"><span data-stu-id="2ef0d-116"><dt>SC\_SEEK\_FROM\_BEGINNING</dt></span></span> </dl> | <span data-ttu-id="2ef0d-117">Commencez la recherche au début.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-117">Begin search at the beginning.</span></span><br/>          |
| <dl> <span data-ttu-id="2ef0d-118"><dt>SC \_ Seek \_ à partir de \_ end </dt></span><span class="sxs-lookup"><span data-stu-id="2ef0d-118"><dt>SC\_SEEK\_FROM\_END </dt></span></span> </dl>      | <span data-ttu-id="2ef0d-119">Commencer la recherche à partir de la fin.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-119">Begin search from the end.</span></span><br/>              |
| <dl> <span data-ttu-id="2ef0d-120"><dt>SC \_ Seek \_ relative</dt></span><span class="sxs-lookup"><span data-stu-id="2ef0d-120"><dt>SC\_SEEK\_RELATIVE</dt></span></span> </dl>        | <span data-ttu-id="2ef0d-121">Commence la recherche à partir de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-121">Begin search from the current position.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2ef0d-122">*lOffset* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ef0d-122">*lOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef0d-123">Nombre d’objets de données de l’objet de référence.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-123">Number of data objects from the reference object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef0d-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ef0d-124">Return value</span></span>

<span data-ttu-id="2ef0d-125">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-125">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="2ef0d-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2ef0d-126">Return code</span></span>                                                                                   | <span data-ttu-id="2ef0d-127">Description</span><span class="sxs-lookup"><span data-stu-id="2ef0d-127">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2ef0d-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ef0d-128"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2ef0d-129">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-129">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="2ef0d-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2ef0d-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2ef0d-131">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-131">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="2ef0d-132"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="2ef0d-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2ef0d-133">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2ef0d-134">Notes</span><span class="sxs-lookup"><span data-stu-id="2ef0d-134">Remarks</span></span>

<span data-ttu-id="2ef0d-135">Pour lire ou écrire à partir d’un fichier, appelez [**en lecture ou en**](iscardfileaccess-read.md) [**écriture**](iscardfileaccess-write.md) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-135">To read to or write from a file, call [**Read**](iscardfileaccess-read.md) or [**Write**](iscardfileaccess-write.md) respectively.</span></span>

<span data-ttu-id="2ef0d-136">Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardFileAccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="2ef0d-136">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="2ef0d-137">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="2ef0d-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="2ef0d-138">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="2ef0d-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef0d-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ef0d-139">Requirements</span></span>



| <span data-ttu-id="2ef0d-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ef0d-140">Requirement</span></span> | <span data-ttu-id="2ef0d-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ef0d-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2ef0d-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ef0d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="2ef0d-143">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ef0d-143">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="2ef0d-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ef0d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="2ef0d-145">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ef0d-145">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2ef0d-146">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2ef0d-146">End of client support</span></span><br/>    | <span data-ttu-id="2ef0d-147">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2ef0d-147">Windows XP</span></span><br/>                                |
| <span data-ttu-id="2ef0d-148">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="2ef0d-148">End of server support</span></span><br/>    | <span data-ttu-id="2ef0d-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2ef0d-149">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="2ef0d-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ef0d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef0d-151">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="2ef0d-151">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> <dt>

[<span data-ttu-id="2ef0d-152">**En lecture**</span><span class="sxs-lookup"><span data-stu-id="2ef0d-152">**Read**</span></span>](iscardfileaccess-read.md)
</dt> <dt>

[<span data-ttu-id="2ef0d-153">**Ecrire**</span><span class="sxs-lookup"><span data-stu-id="2ef0d-153">**Write**</span></span>](iscardfileaccess-write.md)
</dt> </dl>

 

 
