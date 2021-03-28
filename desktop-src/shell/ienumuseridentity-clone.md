---
description: 'IEnumUserIdentity :: clone n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: dde9afca-db8d-41ba-afa0-94eadecb695b
title: 'IEnumUserIdentity :: Clone, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Clone
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: ebdec426fe7ab591c801c00b637211e903cf5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991529"
---
# <a name="ienumuseridentityclone-method"></a><span data-ttu-id="cfed5-104">IEnumUserIdentity :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="cfed5-104">IEnumUserIdentity::Clone method</span></span>

<span data-ttu-id="cfed5-105">\[**IEnumUserIdentity :: Clone** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="cfed5-105">\[**IEnumUserIdentity::Clone** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="cfed5-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="cfed5-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="cfed5-107">Obtient une copie de l’énumération actuelle.</span><span class="sxs-lookup"><span data-stu-id="cfed5-107">Gets a copy of the current enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfed5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfed5-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumUserIdentity **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="cfed5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cfed5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfed5-110">*ppEnum* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cfed5-110">*ppenum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfed5-111">Type : **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="cfed5-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="cfed5-112">Adresse d’un pointeur qui reçoit une copie de cette énumération.</span><span class="sxs-lookup"><span data-stu-id="cfed5-112">The address of a pointer that receives a copy of this enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfed5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cfed5-113">Return value</span></span>

<span data-ttu-id="cfed5-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cfed5-114">Type: **HRESULT**</span></span>

<span data-ttu-id="cfed5-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cfed5-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cfed5-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cfed5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfed5-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cfed5-117">Remarks</span></span>

<span data-ttu-id="cfed5-118">[**IEnumUserIdentity**](ienumuseridentity.md) conserve un nombre interne qui spécifie l’interface qui sera ensuite récupérée.</span><span class="sxs-lookup"><span data-stu-id="cfed5-118">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="cfed5-119">La valeur de ce nombre sera appliquée à l’interface reçue par *ppEnum*.</span><span class="sxs-lookup"><span data-stu-id="cfed5-119">The value of this count will be applied to the interface received by *ppenum*.</span></span> <span data-ttu-id="cfed5-120">Pour réinitialiser le compte, appelez [**IEnumUserIdentity :: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="cfed5-120">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfed5-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cfed5-121">Requirements</span></span>



| <span data-ttu-id="cfed5-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cfed5-122">Requirement</span></span> | <span data-ttu-id="cfed5-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cfed5-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfed5-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfed5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cfed5-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfed5-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cfed5-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cfed5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cfed5-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cfed5-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cfed5-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="cfed5-128">End of client support</span></span><br/>    | <span data-ttu-id="cfed5-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cfed5-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="cfed5-130">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="cfed5-130">End of server support</span></span><br/>    | <span data-ttu-id="cfed5-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cfed5-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="cfed5-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="cfed5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfed5-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfed5-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfed5-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="cfed5-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cfed5-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cfed5-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="cfed5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cfed5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfed5-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfed5-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfed5-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfed5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfed5-139">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="cfed5-139">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="cfed5-140">**IEnumUserIdentity :: Reset**</span><span class="sxs-lookup"><span data-stu-id="cfed5-140">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> </dl>

 

 




