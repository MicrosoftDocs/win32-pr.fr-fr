---
description: Récupère une chaîne ATR de la carte à puce.
ms.assetid: 2021bd0c-6ef8-4679-be6c-9a9fd33d9fd6
title: 'ISCard :: get_Atr, méthode (Scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Atr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4f2a5688ee85318003ea366bbce614e8250a131a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523379"
---
# <a name="iscardget_atr-method"></a><span data-ttu-id="7d41a-103">ISCard :: obtient la \_ méthode ATR</span><span class="sxs-lookup"><span data-stu-id="7d41a-103">ISCard::get\_Atr method</span></span>

<span data-ttu-id="7d41a-104">\[La méthode **obtenir \_ ATR** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="7d41a-104">\[The **get\_Atr** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7d41a-105">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="7d41a-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7d41a-106">La méthode **obtenir \_ ATR** récupère une [*chaîne ATR*](../secgloss/a-gly.md) de la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7d41a-106">The **get\_Atr** method retrieves an [*ATR string*](../secgloss/a-gly.md) of the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7d41a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7d41a-107">Syntax</span></span>


```C++
HRESULT get_Atr(
  [out] LPBYTEBUFFER *ppAtr
);
```



## <a name="parameters"></a><span data-ttu-id="7d41a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d41a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d41a-109">*ppAtr* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7d41a-109">*ppAtr* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d41a-110">Pointeur vers une mémoire tampon d’octets sous la forme d’un [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) qui contiendra la chaîne ATR en retour.</span><span class="sxs-lookup"><span data-stu-id="7d41a-110">Pointer to a byte buffer in the form of an [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) that will contain the ATR string on return.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d41a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7d41a-111">Return value</span></span>

<span data-ttu-id="7d41a-112">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="7d41a-112">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7d41a-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7d41a-113">Return code</span></span>                                                                                   | <span data-ttu-id="7d41a-114">Description</span><span class="sxs-lookup"><span data-stu-id="7d41a-114">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="7d41a-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7d41a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7d41a-116">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="7d41a-116">Operation completed successfully.</span></span><br/>             |
| <dl> <span data-ttu-id="7d41a-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7d41a-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7d41a-118">Le paramètre *ppAtr* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7d41a-118">The *ppAtr* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="7d41a-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="7d41a-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7d41a-120">Un pointeur incorrect a été passé dans *ppAtr*.</span><span class="sxs-lookup"><span data-stu-id="7d41a-120">A bad pointer was passed in *ppAtr*.</span></span><br/>          |
| <dl> <span data-ttu-id="7d41a-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="7d41a-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7d41a-122">La mémoire pour satisfaire la demande n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="7d41a-122">Memory to satisfy the request is unavailable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d41a-123">Notes</span><span class="sxs-lookup"><span data-stu-id="7d41a-123">Remarks</span></span>

<span data-ttu-id="7d41a-124">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="7d41a-124">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7d41a-125">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7d41a-125">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7d41a-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="7d41a-126">Examples</span></span>

<span data-ttu-id="7d41a-127">L’exemple suivant montre comment récupérer la chaîne ATR à partir de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="7d41a-127">The following example shows retrieving the ATR string from the smart card.</span></span>


```C++
// Retrieve the ATR.
// pISCard is a pointer to a previously instantiated ISCard.
// pAtr is a pointer to a previously instantiated IByteBuffer.
hr = pISCard->get_Atr(&pAtr);
if (FAILED(hr))
{
    printf("Failed get_Atr\n");
    // Take other error handling action.
}
// Success, you can now use IByteBuffer::Read to access ATR bytes.
BYTE  byAtr[32];
   long  lBytesRead, i;
   // Read the ATR string into a byte array.
   hr = pAtr->Read(byAtr, 32, &lBytesRead);
   // Use the ATR value. (This example merely displays the bytes.)
   for ( i = 0; i < lBytesRead; i++)
       printf("%c", *(byAtr + i));
   printf("\n");
```



## <a name="requirements"></a><span data-ttu-id="7d41a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d41a-128">Requirements</span></span>



| <span data-ttu-id="7d41a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d41a-129">Requirement</span></span> | <span data-ttu-id="7d41a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d41a-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d41a-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d41a-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7d41a-132">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d41a-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7d41a-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d41a-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7d41a-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d41a-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7d41a-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7d41a-135">End of client support</span></span><br/>    | <span data-ttu-id="7d41a-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7d41a-136">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7d41a-137">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7d41a-137">End of server support</span></span><br/>    | <span data-ttu-id="7d41a-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7d41a-138">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7d41a-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d41a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d41a-140"><dt>Scardmgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d41a-140"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="7d41a-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7d41a-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="7d41a-142"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7d41a-142"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7d41a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7d41a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d41a-144"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d41a-144"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7d41a-145">IID</span><span class="sxs-lookup"><span data-stu-id="7d41a-145">IID</span></span><br/>                      | <span data-ttu-id="7d41a-146">IID \_ ISCard est défini en tant que 1461AAC3-6810-11D0-918F-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7d41a-146">IID\_ISCard is defined as 1461AAC3-6810-11D0-918F-00AA00C18068</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7d41a-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d41a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d41a-148">**Obtient \_ CardHandle**</span><span class="sxs-lookup"><span data-stu-id="7d41a-148">**get\_CardHandle**</span></span>](iscard-get-cardhandle.md)
</dt> <dt>

[<span data-ttu-id="7d41a-149">**recevoir le \_ contexte**</span><span class="sxs-lookup"><span data-stu-id="7d41a-149">**get\_Context**</span></span>](iscard-get-context.md)
</dt> <dt>

[<span data-ttu-id="7d41a-150">**Obtient le \_ protocole**</span><span class="sxs-lookup"><span data-stu-id="7d41a-150">**get\_Protocol**</span></span>](iscard-get-protocol.md)
</dt> <dt>

[<span data-ttu-id="7d41a-151">**afficher l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="7d41a-151">**get\_Status**</span></span>](iscard-get-status.md)
</dt> <dt>

[<span data-ttu-id="7d41a-152">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="7d41a-152">**ISCard**</span></span>](iscard.md)
</dt> <dt>

[<span data-ttu-id="7d41a-153">**IByteBuffer :: lecture**</span><span class="sxs-lookup"><span data-stu-id="7d41a-153">**IByteBuffer::Read**</span></span>](ibytebuffer-read.md)
</dt> </dl>

 

 
