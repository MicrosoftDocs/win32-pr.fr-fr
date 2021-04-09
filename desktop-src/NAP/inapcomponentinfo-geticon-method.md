---
title: Méthode INapComponentInfo GetIcon (NapCommon. h)
description: Est utilisé par le système NAP pour obtenir l’icône d’un client d’intégrité.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Méthode GetIcon NAP
- Méthode GetIcon NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, méthode GetIcon
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942743"
---
# <a name="inapcomponentinfogeticon-method"></a><span data-ttu-id="69090-106">INapComponentInfo :: GetIcon, méthode</span><span class="sxs-lookup"><span data-stu-id="69090-106">INapComponentInfo::GetIcon method</span></span>

> [!Note]  
> <span data-ttu-id="69090-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="69090-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="69090-108">La méthode de rappel **INapComponentInfo :: GetIcon** est utilisée par le système NAP pour obtenir l’icône d’un client de contrôle d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="69090-108">The **INapComponentInfo::GetIcon** callback method is used by the NAP System to get the icon of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="69090-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69090-109">Syntax</span></span>


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a><span data-ttu-id="69090-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69090-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69090-111">*dllFilePath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="69090-111">*dllFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69090-112">Pointeur vers un pointeur vers un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) utilisé pour retourner le chemin d’accès de fichier de la dll qui contient l’icône.</span><span class="sxs-lookup"><span data-stu-id="69090-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) used to return the file path of the DLL that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="69090-113">*iconResourceId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="69090-113">*iconResourceId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69090-114">Pointeur vers la valeur utilisée pour retourner l’ID de ressource de l’icône à utiliser.</span><span class="sxs-lookup"><span data-stu-id="69090-114">A pointer to value used to return the resource ID of the icon to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69090-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69090-115">Return value</span></span>

<span data-ttu-id="69090-116">Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="69090-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="69090-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="69090-117">Return code</span></span>                                                                                     | <span data-ttu-id="69090-118">Description</span><span class="sxs-lookup"><span data-stu-id="69090-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="69090-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69090-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="69090-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="69090-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="69090-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="69090-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="69090-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="69090-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="69090-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="69090-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="69090-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="69090-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69090-125">Notes</span><span class="sxs-lookup"><span data-stu-id="69090-125">Remarks</span></span>

<span data-ttu-id="69090-126">Les icônes doivent être localisées en fonction de l’ID de langue du thread appelant.</span><span class="sxs-lookup"><span data-stu-id="69090-126">Icons should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="69090-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69090-127">Requirements</span></span>



| <span data-ttu-id="69090-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69090-128">Requirement</span></span> | <span data-ttu-id="69090-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="69090-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="69090-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69090-130">Minimum supported client</span></span><br/> | <span data-ttu-id="69090-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69090-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="69090-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69090-132">Minimum supported server</span></span><br/> | <span data-ttu-id="69090-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69090-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="69090-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="69090-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="69090-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="69090-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="69090-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="69090-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="69090-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="69090-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69090-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69090-138">See also</span></span>

<dl> <span data-ttu-id="69090-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="69090-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="69090-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="69090-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





