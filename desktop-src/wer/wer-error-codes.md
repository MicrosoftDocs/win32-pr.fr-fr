---
title: Codes d’erreur WER (Werapi. h)
description: Le tableau suivant fournit une liste de codes d’erreur personnalisés utilisés par Rapport d’erreurs Windows.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106538608"
---
# <a name="wer-error-codes"></a><span data-ttu-id="dc4e6-103">Codes d’erreur WER</span><span class="sxs-lookup"><span data-stu-id="dc4e6-103">WER Error Codes</span></span>

<span data-ttu-id="dc4e6-104">Le tableau suivant fournit une liste de codes d’erreur personnalisés utilisés par Rapport d’erreurs Windows.</span><span class="sxs-lookup"><span data-stu-id="dc4e6-104">The following table provides a list of custom error codes used by Windows Error Reporting.</span></span>



| <span data-ttu-id="dc4e6-105">Constante</span><span class="sxs-lookup"><span data-stu-id="dc4e6-105">Constant</span></span>                                                                                                                                                                                            | <span data-ttu-id="dc4e6-106">Description</span><span class="sxs-lookup"><span data-stu-id="dc4e6-106">Description</span></span>                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <span data-ttu-id="dc4e6-107"><dt>**WER \_ E \_ tampon insuffisant \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dc4e6-107"><dt>**WER\_E\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="dc4e6-108">Une mémoire tampon est trop petite pour contenir les données.</span><span class="sxs-lookup"><span data-stu-id="dc4e6-108">A buffer is too small to contain the data.</span></span><br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <span data-ttu-id="dc4e6-109"><dt>**WER \_ E \_ État non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dc4e6-109"><dt>**WER\_E\_INVALID\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="dc4e6-110">Une fonction a été appelée de manière non prise en charge.</span><span class="sxs-lookup"><span data-stu-id="dc4e6-110">A function was called in an unsupported manner.</span></span><br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <span data-ttu-id="dc4e6-111"><dt>**dépassement de la longueur du WER \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dc4e6-111"><dt>**WER\_E\_LENGTH\_EXCEEDED**</dt></span></span> </dl>             | <span data-ttu-id="dc4e6-112">L’une des limites de longueur a été dépassée.</span><span class="sxs-lookup"><span data-stu-id="dc4e6-112">One of the length limits has been exceeded.</span></span><br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <span data-ttu-id="dc4e6-113"><dt>**WER \_ # \_ \_ param manquant**</dt></span><span class="sxs-lookup"><span data-stu-id="dc4e6-113"><dt>**WER\_E\_MISSING\_PARAM**</dt></span></span> </dl>                   | <span data-ttu-id="dc4e6-114">Un ou plusieurs paramètres sont manquants.</span><span class="sxs-lookup"><span data-stu-id="dc4e6-114">One or more parameters are missing.</span></span><br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <span data-ttu-id="dc4e6-115"><dt>**WER \_ E \_ non \_ trouvé**</dt></span><span class="sxs-lookup"><span data-stu-id="dc4e6-115"><dt>**WER\_E\_NOT\_FOUND**</dt></span></span> </dl>                               | <span data-ttu-id="dc4e6-116">Element not found.</span><span class="sxs-lookup"><span data-stu-id="dc4e6-116">Element not found.</span></span><br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <span data-ttu-id="dc4e6-117"><dt>**stock E/d WER \_ \_ \_ désactivé**</dt></span><span class="sxs-lookup"><span data-stu-id="dc4e6-117"><dt>**WER\_E\_STORE\_DISABLED**</dt></span></span> </dl>                | <span data-ttu-id="dc4e6-118">Le magasin a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="dc4e6-118">The store has been disabled.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="dc4e6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc4e6-119">Requirements</span></span>



| <span data-ttu-id="dc4e6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc4e6-120">Requirement</span></span> | <span data-ttu-id="dc4e6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc4e6-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc4e6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc4e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dc4e6-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc4e6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dc4e6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc4e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dc4e6-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc4e6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dc4e6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc4e6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc4e6-127"><dt>Werapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc4e6-127"><dt>Werapi.h</dt></span></span> </dl> |



 

 





