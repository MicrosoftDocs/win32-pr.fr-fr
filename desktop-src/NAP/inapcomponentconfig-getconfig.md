---
title: INapComponentConfig GetConfig, méthode (NapCommon. h)
description: Récupère la configuration du composant du programme de validation d’intégrité système (SHV).
ms.assetid: 57a1d3a7-05c0-4e0f-91b8-b3cf8982d04f
keywords:
- Méthode GetConfig NAP
- GetConfig, méthode NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, méthode GetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.GetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e07465d768c8902166150e53d4200e775e2597
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466459"
---
# <a name="inapcomponentconfiggetconfig-method"></a><span data-ttu-id="8568c-106">INapComponentConfig :: GetConfig, méthode</span><span class="sxs-lookup"><span data-stu-id="8568c-106">INapComponentConfig::GetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="8568c-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="8568c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8568c-108">La méthode **GetConfig** récupère la configuration du composant du programme de validation d’intégrité système (SHV).</span><span class="sxs-lookup"><span data-stu-id="8568c-108">The **GetConfig** method retrieves the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="8568c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8568c-109">Syntax</span></span>


```C++
HRESULT GetConfig(
  [out] UINT16 *bCount,
  [out] BYTE   **data
) const;
```



## <a name="parameters"></a><span data-ttu-id="8568c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8568c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8568c-111">*bCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8568c-111">*bCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8568c-112">Taille, en octets, de l’objet blob de configuration de *données* .</span><span class="sxs-lookup"><span data-stu-id="8568c-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="8568c-113">*données* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8568c-113">*data* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8568c-114">Pointeur vers l’adresse des données de configuration du composant SHV.</span><span class="sxs-lookup"><span data-stu-id="8568c-114">A pointer to the address of the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="8568c-115">Les données de configuration exportées à partir d’un ordinateur x86 à l’aide de la méthode **GetConfig** peuvent être importées sur un ordinateur x64 à l’aide de la méthode [**setconfig**](inapcomponentconfig-setconfig.md) , et vice versa.</span><span class="sxs-lookup"><span data-stu-id="8568c-115">Configuration data exported from an x86 machine using the **GetConfig** method may be imported onto an x64 machine using the [**SetConfig**](inapcomponentconfig-setconfig.md) method, and vice versa.</span></span> <span data-ttu-id="8568c-116">Par conséquent, les données de configuration doivent être dans un format indépendant de l’architecture, tel que XML.</span><span class="sxs-lookup"><span data-stu-id="8568c-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="8568c-117">L’utilisation de XML au lieu d’un flux d’octets permet d’utiliser plus facilement des données de configuration sur différentes architectures.</span><span class="sxs-lookup"><span data-stu-id="8568c-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="8568c-118">Les éléments XML utilisés dans les données de configuration sont déterminés par l’implémenteur.</span><span class="sxs-lookup"><span data-stu-id="8568c-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8568c-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8568c-119">Return value</span></span>

<span data-ttu-id="8568c-120">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="8568c-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="8568c-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8568c-121">Return code</span></span>                                                                                     | <span data-ttu-id="8568c-122">Description</span><span class="sxs-lookup"><span data-stu-id="8568c-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8568c-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8568c-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="8568c-124">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8568c-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="8568c-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8568c-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="8568c-126">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="8568c-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8568c-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8568c-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="8568c-128">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8568c-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8568c-129">Notes</span><span class="sxs-lookup"><span data-stu-id="8568c-129">Remarks</span></span>

<span data-ttu-id="8568c-130">Le paramètre de données doit être alloué par l’appelé (implémenteur de composants) à l’aide de **CoTaskMemAlloc** et libéré par l’appelant à l’aide de **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="8568c-130">The data parameter must be allocated by the callee (component implementor) using **CoTaskMemAlloc** and freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8568c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8568c-131">Requirements</span></span>



| <span data-ttu-id="8568c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8568c-132">Requirement</span></span> | <span data-ttu-id="8568c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8568c-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8568c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8568c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8568c-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8568c-135">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8568c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8568c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8568c-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8568c-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8568c-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="8568c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8568c-139"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8568c-139"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8568c-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="8568c-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8568c-141"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8568c-141"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8568c-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8568c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8568c-143">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="8568c-143">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="8568c-144">**INapComponentConfig::SetConfig**</span><span class="sxs-lookup"><span data-stu-id="8568c-144">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)
</dt> </dl>

 

 





