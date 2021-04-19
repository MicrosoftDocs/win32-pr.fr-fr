---
description: La \_ méthode obtenir ParticipantTypedInfo obtient une représentation BSTR du type d’informations nécessaires, par exemple PTI \_ EMAILADDRESS.
ms.assetid: 8dcc6182-ad3c-47f2-b4a0-e18a3c9f6888
title: 'ITParticipant :: get_ParticipantTypedInfo, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9936f49e6daa05702699487e4313a918c545a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530427"
---
# <a name="itparticipantget_participanttypedinfo-method"></a><span data-ttu-id="6cacc-103">ITParticipant :: \_ ParticipantTypedInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="6cacc-103">ITParticipant::get\_ParticipantTypedInfo method</span></span>

<span data-ttu-id="6cacc-104">\[en **savoir \_ plus ParticipantTypedInfo** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6cacc-104">\[**get\_ParticipantTypedInfo** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6cacc-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="6cacc-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6cacc-106">La méthode **obtenir \_ ParticipantTypedInfo** obtient une représentation **BSTR** du type d’informations nécessaires, par exemple PTI \_ EMAILADDRESS.</span><span class="sxs-lookup"><span data-stu-id="6cacc-106">The **get\_ParticipantTypedInfo** method gets a **BSTR** representation of the type of information needed, such as PTI\_EMAILADDRESS.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cacc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6cacc-107">Syntax</span></span>


```C++
HRESULT get_ParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="6cacc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6cacc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cacc-109">*Infotype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6cacc-109">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cacc-110">[**Participant \_ \_**](participant-typed-info.md) Descripteur d’informations typées du type d’informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="6cacc-110">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) descriptor of the type of information needed.</span></span>

</dd> <dt>

<span data-ttu-id="6cacc-111">*ppInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6cacc-111">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cacc-112">Pointeur vers la représentation **BSTR** des informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="6cacc-112">Pointer to **BSTR** representation of the information needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cacc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6cacc-113">Return value</span></span>

<span data-ttu-id="6cacc-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="6cacc-114">This method can return one of these values.</span></span>



| <span data-ttu-id="6cacc-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6cacc-115">Return code</span></span>                                                                                    | <span data-ttu-id="6cacc-116">Description</span><span class="sxs-lookup"><span data-stu-id="6cacc-116">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6cacc-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6cacc-117"><dt>**S\_OK**</dt></span></span> </dl>           | <span data-ttu-id="6cacc-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="6cacc-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6cacc-119"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="6cacc-119"><dt>**E\_FAIL**</dt></span></span> </dl>         | <span data-ttu-id="6cacc-120">Échec du stockage des informations dans *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="6cacc-120">Storage of information into *ppInfo* failed.</span></span><br/>         |
| <dl> <span data-ttu-id="6cacc-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6cacc-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>   | <span data-ttu-id="6cacc-122">Le paramètre *infotype* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6cacc-122">The *InfoType* parameter is not valid.</span></span><br/>               |
| <dl> <span data-ttu-id="6cacc-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="6cacc-123"><dt>**E\_POINTER**</dt></span></span> </dl>      | <span data-ttu-id="6cacc-124">Le paramètre *ppInfo* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="6cacc-124">The *ppInfo* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="6cacc-125"><dt>**initem de TAPI \_ E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6cacc-125"><dt>**TAPI\_E\_NOITEM**</dt></span></span> </dl> | <span data-ttu-id="6cacc-126">L’interface TAPI n’a pas d’informations sur le type spécifié.</span><span class="sxs-lookup"><span data-stu-id="6cacc-126">TAPI has no information on the specified type.</span></span><br/>       |
| <dl> <span data-ttu-id="6cacc-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="6cacc-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>  | <span data-ttu-id="6cacc-128">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="6cacc-128">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6cacc-129">Notes</span><span class="sxs-lookup"><span data-stu-id="6cacc-129">Remarks</span></span>

<span data-ttu-id="6cacc-130">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="6cacc-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cacc-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6cacc-131">Requirements</span></span>



| <span data-ttu-id="6cacc-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6cacc-132">Requirement</span></span> | <span data-ttu-id="6cacc-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="6cacc-133">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6cacc-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6cacc-134">TAPI version</span></span><br/> | <span data-ttu-id="6cacc-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6cacc-135">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="6cacc-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="6cacc-136">Header</span></span><br/>       | <dl> <span data-ttu-id="6cacc-137"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6cacc-137"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6cacc-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6cacc-138">Library</span></span><br/>      | <dl> <span data-ttu-id="6cacc-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6cacc-139"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="6cacc-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6cacc-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="6cacc-141"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cacc-141"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cacc-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6cacc-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cacc-143">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="6cacc-143">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="6cacc-144">**\_infos de saisie du participant \_**</span><span class="sxs-lookup"><span data-stu-id="6cacc-144">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> <dt>

[<span data-ttu-id="6cacc-145">**types de médias**</span><span class="sxs-lookup"><span data-stu-id="6cacc-145">**media types**</span></span>](tapimediatype--constants.md)
</dt> </dl>

 

