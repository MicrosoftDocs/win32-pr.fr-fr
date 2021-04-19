---
description: La \_ méthode obtenir LocalParticipantTypedInfo obtient les informations sur les participants, telles que le nom du courrier électronique ou l’emplacement géographique.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'ITLocalParticipant :: get_LocalParticipantTypedInfo, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541639"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a><span data-ttu-id="25972-103">ITLocalParticipant :: \_ LocalParticipantTypedInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="25972-103">ITLocalParticipant::get\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="25972-104">La méthode **obtenir \_ LocalParticipantTypedInfo** obtient les informations sur les participants, telles que le nom du courrier électronique ou l’emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="25972-104">The **get\_LocalParticipantTypedInfo** method gets participant information, such as e-mail name or geographical location.</span></span>

## <a name="syntax"></a><span data-ttu-id="25972-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25972-105">Syntax</span></span>


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="25972-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25972-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25972-107">*Infotype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25972-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25972-108">[**Participant \_ Identificateur \_ d’informations typées**](participant-typed-info.md) du type d’information requis.</span><span class="sxs-lookup"><span data-stu-id="25972-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="25972-109">*ppInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="25972-109">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25972-110">Pointeur vers un **BSTR** qui contient les informations requises à la suite d’un retour réussi de la méthode.</span><span class="sxs-lookup"><span data-stu-id="25972-110">Pointer to a **BSTR** that will contain the required information following a successful return of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25972-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25972-111">Return value</span></span>

<span data-ttu-id="25972-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="25972-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="25972-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25972-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="25972-114">Notes</span><span class="sxs-lookup"><span data-stu-id="25972-114">Remarks</span></span>

<span data-ttu-id="25972-115">L’application doit utiliser [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="25972-115">The application must use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="25972-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25972-116">Requirements</span></span>



| <span data-ttu-id="25972-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25972-117">Requirement</span></span> | <span data-ttu-id="25972-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="25972-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25972-119">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="25972-119">TAPI version</span></span><br/> | <span data-ttu-id="25972-120">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="25972-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="25972-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="25972-121">Header</span></span><br/>       | <dl> <span data-ttu-id="25972-122"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="25972-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="25972-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="25972-123">Library</span></span><br/>      | <dl> <span data-ttu-id="25972-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25972-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="25972-125">DLL</span><span class="sxs-lookup"><span data-stu-id="25972-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="25972-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25972-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="25972-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25972-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25972-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="25972-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="25972-129">**\_infos de saisie du participant \_**</span><span class="sxs-lookup"><span data-stu-id="25972-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

