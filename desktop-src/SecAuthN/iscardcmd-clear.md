---
description: La méthode Clear efface les tampons de messages APDU (Application Protocol Data Unit) et de réponse APDU.
ms.assetid: 5fd3ebb9-b492-4668-9dd8-3ffbcfceb12c
title: 'ISCardCmd :: Clear, méthode (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.Clear
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0701906c38764ed1b4817f40430dde9b48bfb12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113238"
---
# <a name="iscardcmdclear-method"></a><span data-ttu-id="99c04-103">ISCardCmd :: Clear, méthode</span><span class="sxs-lookup"><span data-stu-id="99c04-103">ISCardCmd::Clear method</span></span>

<span data-ttu-id="99c04-104">\[La méthode **Clear** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="99c04-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="99c04-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="99c04-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="99c04-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="99c04-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="99c04-107">La méthode **Clear** efface les tampons de messages APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) et de [*réponse APDU*](../secgloss/r-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="99c04-107">The **Clear** method clears the [*application protocol data unit*](../secgloss/a-gly.md) (APDU) and [*reply APDU*](../secgloss/r-gly.md) message buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c04-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99c04-108">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="99c04-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99c04-109">Parameters</span></span>

<span data-ttu-id="99c04-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="99c04-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="99c04-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99c04-111">Return value</span></span>

<span data-ttu-id="99c04-112">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="99c04-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="99c04-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="99c04-113">Return code</span></span>                                                                             | <span data-ttu-id="99c04-114">Description</span><span class="sxs-lookup"><span data-stu-id="99c04-114">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="99c04-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="99c04-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="99c04-116">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="99c04-116">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="99c04-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="99c04-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="99c04-118">Erreur inconnue.</span><span class="sxs-lookup"><span data-stu-id="99c04-118">Unknown error.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="99c04-119">Notes</span><span class="sxs-lookup"><span data-stu-id="99c04-119">Remarks</span></span>

<span data-ttu-id="99c04-120">Pour générer une commande APDU, appelez [**BuildCmd**](iscardcmd-buildcmd.md).</span><span class="sxs-lookup"><span data-stu-id="99c04-120">To build a command APDU, call [**BuildCmd**](iscardcmd-buildcmd.md).</span></span>

<span data-ttu-id="99c04-121">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardCmd**](iscardcmd.md).</span><span class="sxs-lookup"><span data-stu-id="99c04-121">For a list of all the methods provided by this interface, see [**ISCardCmd**](iscardcmd.md).</span></span>

<span data-ttu-id="99c04-122">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="99c04-122">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="99c04-123">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="99c04-123">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="99c04-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="99c04-124">Examples</span></span>

<span data-ttu-id="99c04-125">L’exemple suivant montre comment effacer les tampons de messages APDU et reply.</span><span class="sxs-lookup"><span data-stu-id="99c04-125">The following example shows how to clear the APDU and reply APDU message buffers.</span></span>


```C++
HRESULT  hr;

hr = pISCardCmd->Clear();
if (FAILED(hr))
{
    printf("Failed ISCardCmd::Clear\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="99c04-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99c04-126">Requirements</span></span>



| <span data-ttu-id="99c04-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99c04-127">Requirement</span></span> | <span data-ttu-id="99c04-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="99c04-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99c04-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99c04-129">Minimum supported client</span></span><br/> | <span data-ttu-id="99c04-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99c04-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="99c04-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99c04-131">Minimum supported server</span></span><br/> | <span data-ttu-id="99c04-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99c04-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="99c04-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="99c04-133">End of client support</span></span><br/>    | <span data-ttu-id="99c04-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="99c04-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="99c04-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="99c04-135">End of server support</span></span><br/>    | <span data-ttu-id="99c04-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99c04-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="99c04-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="99c04-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="99c04-138"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="99c04-138"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="99c04-139">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="99c04-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="99c04-140"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99c04-140"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99c04-141">DLL</span><span class="sxs-lookup"><span data-stu-id="99c04-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99c04-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99c04-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="99c04-143">IID</span><span class="sxs-lookup"><span data-stu-id="99c04-143">IID</span></span><br/>                      | <span data-ttu-id="99c04-144">IID \_ ISCardCmd est défini en tant que D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="99c04-144">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="99c04-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99c04-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99c04-146">**ISCardCmd::BuildCmd**</span><span class="sxs-lookup"><span data-stu-id="99c04-146">**ISCardCmd::BuildCmd**</span></span>](iscardcmd-buildcmd.md)
</dt> <dt>

[<span data-ttu-id="99c04-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="99c04-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
