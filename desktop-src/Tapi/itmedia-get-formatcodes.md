---
description: La \_ méthode obtenir FormatCodes obtient la liste des codes de format de charge utile du média. La variante retourne un SAFEARRAY de BSTR. Chaque BSTR au sein de ce tableau est une chaîne de code de format.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'ITMedia :: get_FormatCodes, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526780"
---
# <a name="itmediaget_formatcodes-method"></a><span data-ttu-id="71b63-105">ITMedia :: \_ FormatCodes, méthode</span><span class="sxs-lookup"><span data-stu-id="71b63-105">ITMedia::get\_FormatCodes method</span></span>

<span data-ttu-id="71b63-106">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="71b63-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="71b63-107">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="71b63-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="71b63-108">La méthode **obtenir \_ FormatCodes** obtient la liste des codes de format de charge utile du média.</span><span class="sxs-lookup"><span data-stu-id="71b63-108">The **get\_FormatCodes** method gets the list of media payload format codes.</span></span> <span data-ttu-id="71b63-109">La variante retourne un SAFEARRAY de **BSTR** s.</span><span class="sxs-lookup"><span data-stu-id="71b63-109">The variant returns a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="71b63-110">Chaque **BSTR** au sein de ce tableau est une chaîne de code de format.</span><span class="sxs-lookup"><span data-stu-id="71b63-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b63-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71b63-111">Syntax</span></span>


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="71b63-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71b63-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71b63-113">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="71b63-113">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71b63-114">Tableau de codes de format de charge utile de média.</span><span class="sxs-lookup"><span data-stu-id="71b63-114">Array of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71b63-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71b63-115">Return value</span></span>

<span data-ttu-id="71b63-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="71b63-116">This method can return one of these values.</span></span>



| <span data-ttu-id="71b63-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="71b63-117">Return code</span></span>                                                                                   | <span data-ttu-id="71b63-118">Description</span><span class="sxs-lookup"><span data-stu-id="71b63-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="71b63-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71b63-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="71b63-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="71b63-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="71b63-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="71b63-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="71b63-122">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="71b63-122">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="71b63-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="71b63-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="71b63-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="71b63-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="71b63-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="71b63-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="71b63-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="71b63-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="71b63-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="71b63-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="71b63-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="71b63-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="71b63-129">Notes</span><span class="sxs-lookup"><span data-stu-id="71b63-129">Remarks</span></span>

<span data-ttu-id="71b63-130">Quand une liste de formats de charge utile est donnée, cela implique que tous ces formats peuvent être utilisés dans la session, mais que le premier de ces formats soit le format par défaut de la session.</span><span class="sxs-lookup"><span data-stu-id="71b63-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="71b63-131">Lorsque le protocole de transport est RTP, les codes de format sont des types de charge utile RTP.</span><span class="sxs-lookup"><span data-stu-id="71b63-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b63-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71b63-132">Requirements</span></span>



| <span data-ttu-id="71b63-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71b63-133">Requirement</span></span> | <span data-ttu-id="71b63-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="71b63-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71b63-135">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="71b63-135">TAPI version</span></span><br/> | <span data-ttu-id="71b63-136">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="71b63-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="71b63-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="71b63-137">Header</span></span><br/>       | <dl> <span data-ttu-id="71b63-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b63-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="71b63-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71b63-139">Library</span></span><br/>      | <dl> <span data-ttu-id="71b63-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71b63-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="71b63-141">DLL</span><span class="sxs-lookup"><span data-stu-id="71b63-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="71b63-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71b63-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b63-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71b63-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b63-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="71b63-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="71b63-145">**ITMedia ::p ut \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="71b63-145">**ITMedia::put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




