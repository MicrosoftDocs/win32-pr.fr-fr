---
description: La méthode AttachByReader ouvre la carte à puce dans le lecteur nommé.
ms.assetid: a92f3281-5018-4e90-bfa0-f03eb9373bb1
title: 'ISCard :: AttachByReader, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByReader
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 2607ea2e13be2dcccc3c1b6beebd40c86822d0a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952788"
---
# <a name="iscardattachbyreader-method"></a><span data-ttu-id="3e17f-103">ISCard :: AttachByReader, méthode</span><span class="sxs-lookup"><span data-stu-id="3e17f-103">ISCard::AttachByReader method</span></span>

<span data-ttu-id="3e17f-104">\[La méthode **AttachByReader** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="3e17f-104">\[The **AttachByReader** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3e17f-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3e17f-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3e17f-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3e17f-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3e17f-107">La méthode **AttachByReader** ouvre la [*carte à puce*](../secgloss/s-gly.md) dans le [*lecteur*](../secgloss/r-gly.md)nommé.</span><span class="sxs-lookup"><span data-stu-id="3e17f-107">The **AttachByReader** method opens the [*smart card*](../secgloss/s-gly.md) in the named [*reader*](../secgloss/r-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e17f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e17f-108">Syntax</span></span>


```C++
HRESULT AttachByReader(
  [in] BSTR              bstrReaderName,
  [in] SCARD_SHARE_MODES ShareMode,
  [in] SCARD_PROTOCOLS   PrefProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="3e17f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e17f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e17f-110">*bstrReaderName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e17f-110">*bstrReaderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e17f-111">**BSTR** qui contient le nom du lecteur de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="3e17f-111">A **BSTR** that contains the name of the smart card reader.</span></span>

</dd> <dt>

<span data-ttu-id="3e17f-112">*ShareMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e17f-112">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e17f-113">Mode dans lequel revendiquer l’accès à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="3e17f-113">Mode in which to claim access to the smart card.</span></span>



| <span data-ttu-id="3e17f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e17f-114">Value</span></span>                                                                                                                                            | <span data-ttu-id="3e17f-115">Signification</span><span class="sxs-lookup"><span data-stu-id="3e17f-115">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="3e17f-116"><dt>**Or**</dt></span><span class="sxs-lookup"><span data-stu-id="3e17f-116"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="3e17f-117">Personne d’autre n’utilise cette connexion à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="3e17f-117">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="3e17f-118"><dt>**PARTAGÉ**</dt></span><span class="sxs-lookup"><span data-stu-id="3e17f-118"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="3e17f-119">D’autres applications peuvent utiliser cette connexion.</span><span class="sxs-lookup"><span data-stu-id="3e17f-119">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="3e17f-120">*PrefProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e17f-120">*PrefProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e17f-121">Valeur de protocole préférée.</span><span class="sxs-lookup"><span data-stu-id="3e17f-121">Preferred protocol value.</span></span>

<dl><span id="T0"></span><span id="t0"></span><dt>

<span data-ttu-id="3e17f-122">**T0**</span><span class="sxs-lookup"><span data-stu-id="3e17f-122">**T0**</span></span>
</dt><span id="T1"></span><span id="t1"></span><dt>

<span data-ttu-id="3e17f-123">**T1**</span><span class="sxs-lookup"><span data-stu-id="3e17f-123">**T1**</span></span>
</dt><span id="RAW"></span><span id="raw"></span><dt>

<span data-ttu-id="3e17f-124">**RAW**</span><span class="sxs-lookup"><span data-stu-id="3e17f-124">**RAW**</span></span>
</dt><span id="T0_T1"></span><span id="t0_t1"></span><dt>

<span data-ttu-id="3e17f-125">**T0 \| T1**</span><span class="sxs-lookup"><span data-stu-id="3e17f-125">**T0\|T1**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e17f-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e17f-126">Return value</span></span>

<span data-ttu-id="3e17f-127">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="3e17f-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3e17f-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3e17f-128">Return code</span></span>                                                                                  | <span data-ttu-id="3e17f-129">Description</span><span class="sxs-lookup"><span data-stu-id="3e17f-129">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e17f-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3e17f-130"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3e17f-131">L’ouverture de la carte à puce dans le lecteur nommé s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="3e17f-131">Open on the smart card in the named reader has been completed successfully.</span></span><br/>           |
| <dl> <span data-ttu-id="3e17f-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e17f-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3e17f-133">Il y a un problème avec un ou plusieurs des paramètres transmis à la fonction.</span><span class="sxs-lookup"><span data-stu-id="3e17f-133">There is something wrong with one or more of the parameters passed into the function.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3e17f-134">Notes</span><span class="sxs-lookup"><span data-stu-id="3e17f-134">Remarks</span></span>

<span data-ttu-id="3e17f-135">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="3e17f-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3e17f-136">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3e17f-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

<span data-ttu-id="3e17f-137">Lorsque vous avez fini d’utiliser le lecteur, libérez la pièce jointe en appelant la méthode [**ISCard ::D Etach**](iscard-detach.md) .</span><span class="sxs-lookup"><span data-stu-id="3e17f-137">When you have finished using the reader, release the attachment by calling the [**ISCard::Detach**](iscard-detach.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="3e17f-138">Exemples</span><span class="sxs-lookup"><span data-stu-id="3e17f-138">Examples</span></span>

<span data-ttu-id="3e17f-139">L’exemple suivant illustre l’attachement à une carte à puce dans un lecteur de carte à puce spécifié.</span><span class="sxs-lookup"><span data-stu-id="3e17f-139">The following example shows attaching to a smart card in a specified smart card reader.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Scardmgr.h>

// The reader name is vendor specific; change as needed.
#define READER_NAME L"Vendor Reader 0"

void main()
{
    BSTR     bstrReader = NULL;
    HRESULT  hr;

    bstrReader = SysAllocString(READER_NAME);
    if (NULL == bstrReader)
    {
        // Error encountered.
        exit(1);
    }

    // Connect to the reader.
    hr = pISCard->AttachByReader(bstrReader, SHARED, T0);
    if (FAILED(hr))
    {
        printf("Failed AttachByReader\n");
        // Take other error handling action.
        // ...
    }

    // Detach reader by calling ISCard::Detach (not shown).
    // ...

    // When done, free BSTR.
    if (NULL != bstrReader)
        SysFreeString(bstrReader);
}
```



## <a name="requirements"></a><span data-ttu-id="3e17f-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e17f-140">Requirements</span></span>



| <span data-ttu-id="3e17f-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e17f-141">Requirement</span></span> | <span data-ttu-id="3e17f-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e17f-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e17f-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e17f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3e17f-144">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e17f-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3e17f-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e17f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3e17f-146">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e17f-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3e17f-147">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3e17f-147">End of client support</span></span><br/>    | <span data-ttu-id="3e17f-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e17f-148">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3e17f-149">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="3e17f-149">End of server support</span></span><br/>    | <span data-ttu-id="3e17f-150">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e17f-150">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3e17f-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e17f-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e17f-152"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e17f-152"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="3e17f-153">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3e17f-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="3e17f-154"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3e17f-154"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3e17f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3e17f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e17f-156"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e17f-156"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3e17f-157">IID</span><span class="sxs-lookup"><span data-stu-id="3e17f-157">IID</span></span><br/>                      | <span data-ttu-id="3e17f-158">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3e17f-158">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3e17f-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e17f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e17f-160">**AttachByHandle**</span><span class="sxs-lookup"><span data-stu-id="3e17f-160">**AttachByHandle**</span></span>](iscard-attachbyhandle.md)
</dt> <dt>

[<span data-ttu-id="3e17f-161">**Dissocié**</span><span class="sxs-lookup"><span data-stu-id="3e17f-161">**Detach**</span></span>](iscard-detach.md)
</dt> <dt>

[<span data-ttu-id="3e17f-162">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="3e17f-162">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="3e17f-163">**Rattacher**</span><span class="sxs-lookup"><span data-stu-id="3e17f-163">**ReAttach**</span></span>](iscard-reattach.md)
</dt> </dl>

 

 
