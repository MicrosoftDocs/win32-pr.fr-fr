---
description: Construit une unité de données de protocole d’application de commande valide pour la transmission vers une carte à puce.
ms.assetid: d1003cc3-c235-4635-ad5a-8cea7363bf30
title: 'ISCardCmd :: BuildCmd, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.BuildCmd
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f44597ea087f7ccec191abc9dd03787780e88b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204006"
---
# <a name="iscardcmdbuildcmd-method"></a><span data-ttu-id="91086-103">ISCardCmd :: BuildCmd, méthode</span><span class="sxs-lookup"><span data-stu-id="91086-103">ISCardCmd::BuildCmd method</span></span>

<span data-ttu-id="91086-104">\[La méthode **BuildCmd** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="91086-104">\[The **BuildCmd** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="91086-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="91086-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="91086-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="91086-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="91086-107">La méthode **BuildCmd** construit une [*unité de données de protocole d’application*](../secgloss/a-gly.md) de commande valide pour la transmission vers une [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="91086-107">The **BuildCmd** method constructs a valid command [*application protocol data unit*](../secgloss/a-gly.md) (APDU) for transmission to a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="91086-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91086-108">Syntax</span></span>


```C++
HRESULT BuildCmd(
  [in] BYTE         byClassId,
  [in] BYTE         byInsId,
  [in] BYTE         byP1,
  [in] BYTE         byP2,
  [in] LPBYTEBUFFER pbyData,
  [in] LONG         *p1Le
);
```



## <a name="parameters"></a><span data-ttu-id="91086-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91086-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91086-110">*byClassId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91086-110">*byClassId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91086-111">Identificateur de classe de commande.</span><span class="sxs-lookup"><span data-stu-id="91086-111">Command class identifier.</span></span>

</dd> <dt>

<span data-ttu-id="91086-112">*byInsId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91086-112">*byInsId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91086-113">Identificateur d’instruction de commande.</span><span class="sxs-lookup"><span data-stu-id="91086-113">Command instruction identifier.</span></span>

</dd> <dt>

<span data-ttu-id="91086-114">*byP1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91086-114">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91086-115">Premier paramètre de la commande.</span><span class="sxs-lookup"><span data-stu-id="91086-115">Command's first parameter.</span></span>

</dd> <dt>

<span data-ttu-id="91086-116">*byP2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91086-116">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91086-117">Deuxième paramètre de la commande.</span><span class="sxs-lookup"><span data-stu-id="91086-117">Command's second parameter.</span></span>

</dd> <dt>

<span data-ttu-id="91086-118">*pbyData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91086-118">*pbyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91086-119">Pointeur vers la partie données de la commande.</span><span class="sxs-lookup"><span data-stu-id="91086-119">Pointer to the data portion of the command.</span></span>

</dd> <dt>

<span data-ttu-id="91086-120">*p1Le* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91086-120">*p1Le* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91086-121">Pointeur vers un entier LONG contenant la longueur attendue des données retournées.</span><span class="sxs-lookup"><span data-stu-id="91086-121">Pointer to a LONG integer containing the expected length of the returned data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91086-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91086-122">Return value</span></span>

<span data-ttu-id="91086-123">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="91086-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="91086-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="91086-124">Return code</span></span>                                                                                   | <span data-ttu-id="91086-125">Description</span><span class="sxs-lookup"><span data-stu-id="91086-125">Description</span></span>                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="91086-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91086-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="91086-127">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="91086-127">Operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="91086-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="91086-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="91086-129">L’un des paramètres n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="91086-129">One of the parameters is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="91086-130"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="91086-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="91086-131">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="91086-131">A bad pointer was passed in.</span></span><br/>        |
| <dl> <span data-ttu-id="91086-132"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="91086-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="91086-133">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="91086-133">Out of memory.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="91086-134">Notes</span><span class="sxs-lookup"><span data-stu-id="91086-134">Remarks</span></span>

<span data-ttu-id="91086-135">Pour encapsuler la commande dans une autre commande, appelez [**encapsuler**](iscardcmd-encapsulate.md).</span><span class="sxs-lookup"><span data-stu-id="91086-135">To encapsulate the command into another command, call [**Encapsulate**](iscardcmd-encapsulate.md).</span></span>

<span data-ttu-id="91086-136">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="91086-136">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="91086-137">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="91086-137">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="91086-138">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="91086-138">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="91086-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="91086-139">Examples</span></span>

<span data-ttu-id="91086-140">L’exemple suivant montre comment construire une commande APDU.</span><span class="sxs-lookup"><span data-stu-id="91086-140">The following example shows how to construct a command APDU.</span></span> <span data-ttu-id="91086-141">L’exemple suppose que pISCardCmd est un pointeur valide vers une instance de l’interface [**ISCardCmd**](iscardcmd.md) et que pIByteRequest est un pointeur valide vers une instance de l’interface [**IByteBuffer**](ibytebuffer.md) initialisée avec un appel précédent à la méthode [**IByteBuffer :: Initialize**](ibytebuffer-initialize.md) .</span><span class="sxs-lookup"><span data-stu-id="91086-141">The example assumes that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface and that pIByteRequest is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface initialized with a previous call to the [**IByteBuffer::Initialize**](ibytebuffer-initialize.md) method.</span></span>


```C++
LONG       lLe = 0;
HRESULT    hr;

hr = pISCardCmd->BuildCmd(0x00,   // Some cards prefer 0xC0
                          0xa4,   // 'Select File'
                          0x00,
                          0x00,
                          pIByteRequest,
                          &lLe);
if (FAILED(hr))
{
    printf("Failed ISCardCmd::BuildCmd\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="91086-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91086-142">Requirements</span></span>



| <span data-ttu-id="91086-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91086-143">Requirement</span></span> | <span data-ttu-id="91086-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="91086-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91086-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91086-145">Minimum supported client</span></span><br/> | <span data-ttu-id="91086-146">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91086-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="91086-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91086-147">Minimum supported server</span></span><br/> | <span data-ttu-id="91086-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91086-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91086-149">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="91086-149">End of client support</span></span><br/>    | <span data-ttu-id="91086-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="91086-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="91086-151">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="91086-151">End of server support</span></span><br/>    | <span data-ttu-id="91086-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="91086-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="91086-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="91086-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="91086-154"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="91086-154"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="91086-155">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="91086-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="91086-156"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="91086-156"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="91086-157">DLL</span><span class="sxs-lookup"><span data-stu-id="91086-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91086-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91086-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="91086-159">IID</span><span class="sxs-lookup"><span data-stu-id="91086-159">IID</span></span><br/>                      | <span data-ttu-id="91086-160">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="91086-160">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="91086-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91086-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91086-162">**Encapsuler**</span><span class="sxs-lookup"><span data-stu-id="91086-162">**Encapsulate**</span></span>](iscardcmd-encapsulate.md)
</dt> <dt>

[<span data-ttu-id="91086-163">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="91086-163">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
