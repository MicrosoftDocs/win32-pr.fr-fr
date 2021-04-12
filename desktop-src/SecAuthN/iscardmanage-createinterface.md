---
description: Crée l’interface spécifiée.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'ISCardManage :: CreateInterface, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204168"
---
# <a name="iscardmanagecreateinterface-method"></a><span data-ttu-id="00901-103">ISCardManage :: CreateInterface, méthode</span><span class="sxs-lookup"><span data-stu-id="00901-103">ISCardManage::CreateInterface method</span></span>

<span data-ttu-id="00901-104">\[La méthode **CreateInterface** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise.</span><span class="sxs-lookup"><span data-stu-id="00901-104">\[The **CreateInterface** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="00901-105">Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="00901-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="00901-106">La méthode **CreateInterface** crée l’interface spécifiée.</span><span class="sxs-lookup"><span data-stu-id="00901-106">The **CreateInterface** method creates the specified interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="00901-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00901-107">Syntax</span></span>


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a><span data-ttu-id="00901-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00901-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00901-109">*pguidInterface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00901-109">*pguidInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00901-110">Valeur GUID de l’interface à créer.</span><span class="sxs-lookup"><span data-stu-id="00901-110">The GUID value of the interface to create.</span></span>

</dd> <dt>

<span data-ttu-id="00901-111">*bstrName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00901-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00901-112">Nom de l’interface à créer si le GUID n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="00901-112">The name of the interface to create if the GUID is unavailable.</span></span> <span data-ttu-id="00901-113">Les valeurs standard sont « CryptoProvider ».</span><span class="sxs-lookup"><span data-stu-id="00901-113">Standard values are "CryptoProvider".</span></span>

</dd> <dt>

<span data-ttu-id="00901-114">*pUserData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="00901-114">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00901-115">Pointeur vers des données spécifiques à l’utilisateur à utiliser dans la création d’une interface.</span><span class="sxs-lookup"><span data-stu-id="00901-115">Pointer to user-specific data to use in the creation of an interface.</span></span>

</dd> <dt>

<span data-ttu-id="00901-116">*ppInterface* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="00901-116">*ppInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00901-117">Pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="00901-117">Pointer to the returned interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00901-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00901-118">Return value</span></span>

<span data-ttu-id="00901-119">Les valeurs de retour possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="00901-119">The possible return values are the following:</span></span>



| <span data-ttu-id="00901-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="00901-120">Return code</span></span>                                                                                   | <span data-ttu-id="00901-121">Description</span><span class="sxs-lookup"><span data-stu-id="00901-121">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00901-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="00901-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="00901-123">Opération exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="00901-123">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="00901-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="00901-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="00901-125">L’un des paramètres fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="00901-125">One of the supplied parameters are not valid.</span></span><br/>                                         |
| <dl> <span data-ttu-id="00901-126"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="00901-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="00901-127">Un pointeur incorrect a été passé dans le paramètre *pguidInterface* ou *pUserData* .</span><span class="sxs-lookup"><span data-stu-id="00901-127">A bad pointer was passed in either the *pguidInterface* or the *pUserData* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="00901-128"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="00901-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="00901-129">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="00901-129">Out of memory.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="00901-130">Notes</span><span class="sxs-lookup"><span data-stu-id="00901-130">Remarks</span></span>

<span data-ttu-id="00901-131">Pour obtenir la liste de toutes les méthodes définies par l’interface [**ISCardManage**](iscardmanage.md) , consultez **ISCardManage**.</span><span class="sxs-lookup"><span data-stu-id="00901-131">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see **ISCardManage**.</span></span>

<span data-ttu-id="00901-132">Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de [*carte*](../secgloss/s-gly.md) à puce si une fonction de carte à puce a été appelée pour terminer la demande.</span><span class="sxs-lookup"><span data-stu-id="00901-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="00901-133">Pour plus d’informations sur les codes d’erreur de carte à puce, consultez [valeurs de retour de carte à puce](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="00901-133">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00901-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00901-134">Requirements</span></span>



| <span data-ttu-id="00901-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00901-135">Requirement</span></span> | <span data-ttu-id="00901-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="00901-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="00901-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00901-137">Minimum supported client</span></span><br/> | <span data-ttu-id="00901-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00901-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="00901-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00901-139">Minimum supported server</span></span><br/> | <span data-ttu-id="00901-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="00901-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="00901-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="00901-141">End of client support</span></span><br/>    | <span data-ttu-id="00901-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="00901-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="00901-143">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="00901-143">End of server support</span></span><br/>    | <span data-ttu-id="00901-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00901-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="00901-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00901-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00901-146">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="00901-146">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
