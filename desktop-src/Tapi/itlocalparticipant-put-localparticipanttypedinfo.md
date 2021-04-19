---
description: La \_ méthode put LocalParticipantTypedInfo définit les informations sur les participants.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: ITLocalParticipant ::p ut_LocalParticipantTypedInfo, méthode (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537782"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a><span data-ttu-id="67db2-103">ITLocalParticipant ::p ut \_ LocalParticipantTypedInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="67db2-103">ITLocalParticipant::put\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="67db2-104">La méthode **put \_ LocalParticipantTypedInfo** définit les informations sur les participants.</span><span class="sxs-lookup"><span data-stu-id="67db2-104">The **put\_LocalParticipantTypedInfo** method sets participant information.</span></span>

## <a name="syntax"></a><span data-ttu-id="67db2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67db2-105">Syntax</span></span>


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="67db2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67db2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67db2-107">*Infotype* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67db2-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67db2-108">[**Participant \_ Identificateur \_ d’informations typées**](participant-typed-info.md) du type d’information requis.</span><span class="sxs-lookup"><span data-stu-id="67db2-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of the type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="67db2-109">*ppInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67db2-109">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67db2-110">**BSTR** contenant la nouvelle valeur requise pour les informations.</span><span class="sxs-lookup"><span data-stu-id="67db2-110">**BSTR** containing the required new value for the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67db2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67db2-111">Return value</span></span>

<span data-ttu-id="67db2-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="67db2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="67db2-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="67db2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="67db2-114">Notes</span><span class="sxs-lookup"><span data-stu-id="67db2-114">Remarks</span></span>

<span data-ttu-id="67db2-115">L’application doit utiliser [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PpInfo* et utiliser [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="67db2-115">The application must use [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *ppInfo* parameter and use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="67db2-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67db2-116">Requirements</span></span>



| <span data-ttu-id="67db2-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67db2-117">Requirement</span></span> | <span data-ttu-id="67db2-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="67db2-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67db2-119">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="67db2-119">TAPI version</span></span><br/> | <span data-ttu-id="67db2-120">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="67db2-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="67db2-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="67db2-121">Header</span></span><br/>       | <dl> <span data-ttu-id="67db2-122"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="67db2-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="67db2-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="67db2-123">Library</span></span><br/>      | <dl> <span data-ttu-id="67db2-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67db2-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="67db2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="67db2-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="67db2-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67db2-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="67db2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67db2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67db2-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="67db2-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="67db2-129">**\_infos de saisie du participant \_**</span><span class="sxs-lookup"><span data-stu-id="67db2-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

