---
description: La méthode GetChallenge renvoie un challenge à partir de la carte à puce.
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: 'ISCardAuth :: GetChallenge, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9282c0a922a1f8c8daff07c31dcafa7e47e923a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201947"
---
# <a name="iscardauthgetchallenge-method"></a><span data-ttu-id="8a149-103">ISCardAuth :: GetChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="8a149-103">ISCardAuth::GetChallenge method</span></span>

<span data-ttu-id="8a149-104">\[La méthode **GetChallenge** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="8a149-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8a149-105">Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8a149-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a149-106">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8a149-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8a149-107">La méthode **GetChallenge** renvoie un challenge à partir de la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8a149-107">The **GetChallenge** method returns a challenge from the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a149-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a149-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="8a149-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a149-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a149-110">*lAlgoID* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="8a149-110">*lAlgoID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a149-111">Algorithme à utiliser dans le processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8a149-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="8a149-112">*lLengthOfChallenge* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a149-112">*lLengthOfChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a149-113">Longueur maximale de la réponse attendue.</span><span class="sxs-lookup"><span data-stu-id="8a149-113">Maximum length of expected response.</span></span>

</dd> <dt>

<span data-ttu-id="8a149-114">*pParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a149-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a149-115">Objet [**IByteBuffer**](ibytebuffer.md) contenant les paramètres spécifiques au fournisseur du processus d’authentification.</span><span class="sxs-lookup"><span data-stu-id="8a149-115">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="8a149-116">*pbuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8a149-116">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a149-117">En entrée, pointe vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="8a149-117">On input, points to the buffer.</span></span>

<span data-ttu-id="8a149-118">Lors de la sortie, contient les données de vérification de la carte.</span><span class="sxs-lookup"><span data-stu-id="8a149-118">On output, contains the challenge data from the card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a149-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a149-119">Return value</span></span>

<span data-ttu-id="8a149-120">La méthode retourne l’une des valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="8a149-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8a149-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8a149-121">Return code</span></span>                                                                                   | <span data-ttu-id="8a149-122">Description</span><span class="sxs-lookup"><span data-stu-id="8a149-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8a149-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a149-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8a149-124">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="8a149-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8a149-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8a149-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8a149-126">Paramètre non valide.</span><span class="sxs-lookup"><span data-stu-id="8a149-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8a149-127"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="8a149-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8a149-128">Un pointeur incorrect a été passé.</span><span class="sxs-lookup"><span data-stu-id="8a149-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="8a149-129"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8a149-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8a149-130">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="8a149-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8a149-131">Notes</span><span class="sxs-lookup"><span data-stu-id="8a149-131">Remarks</span></span>

<span data-ttu-id="8a149-132">Pour obtenir la liste de toutes les méthodes fournies par cette interface, consultez [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="8a149-132">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="8a149-133">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="8a149-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8a149-134">Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8a149-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a149-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a149-135">Requirements</span></span>



| <span data-ttu-id="8a149-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a149-136">Requirement</span></span> | <span data-ttu-id="8a149-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a149-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a149-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a149-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8a149-139">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a149-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8a149-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a149-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8a149-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a149-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8a149-142">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8a149-142">End of client support</span></span><br/>    | <span data-ttu-id="8a149-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8a149-143">Windows XP</span></span><br/>                                |
| <span data-ttu-id="8a149-144">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8a149-144">End of server support</span></span><br/>    | <span data-ttu-id="8a149-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a149-145">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8a149-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a149-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a149-147">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="8a149-147">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
