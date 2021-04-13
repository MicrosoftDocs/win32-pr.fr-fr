---
title: Méthode INapComponentConfig SetConfig (NapCommon. h)
description: Définit la configuration du composant du programme de validation d’intégrité système (SHV).
ms.assetid: ec27e30b-4205-40bc-a24b-61072a746e53
keywords:
- Méthode SetConfig NAP
- Méthode SetConfig NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, méthode SetConfig
topic_type:
- apiref
api_name:
- INapComponentConfig.SetConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f3d557517ec27f9537a7cbcd46be9e2cd107e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519282"
---
# <a name="inapcomponentconfigsetconfig-method"></a><span data-ttu-id="b7923-106">INapComponentConfig :: SetConfig, méthode</span><span class="sxs-lookup"><span data-stu-id="b7923-106">INapComponentConfig::SetConfig method</span></span>

> [!Note]  
> <span data-ttu-id="b7923-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b7923-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b7923-108">La méthode **setconfig** définit la configuration du composant du programme de validation d’intégrité système (SHV).</span><span class="sxs-lookup"><span data-stu-id="b7923-108">The **SetConfig** method sets the system health validator (SHV) component configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7923-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7923-109">Syntax</span></span>


```C++
HRESULT SetConfig(
  [in] UINT16 bCount,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="b7923-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7923-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7923-111">*bCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7923-111">*bCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7923-112">Taille, en octets, de l’objet blob de configuration de *données* .</span><span class="sxs-lookup"><span data-stu-id="b7923-112">The size, in bytes, of the *data* configuration blob.</span></span>

</dd> <dt>

<span data-ttu-id="b7923-113">*données* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7923-113">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7923-114">Pointeur vers les données de configuration du composant SHV.</span><span class="sxs-lookup"><span data-stu-id="b7923-114">A pointer to the SHV component configuration data.</span></span>

> [!Note]  
> <span data-ttu-id="b7923-115">Les données de configuration exportées à partir d’un ordinateur x86 à l’aide de la méthode [**GetConfig**](inapcomponentconfig-getconfig.md) peuvent être importées sur un ordinateur x64 à l’aide de la méthode **setconfig** , et vice versa.</span><span class="sxs-lookup"><span data-stu-id="b7923-115">Configuration data exported from an x86 machine using the [**GetConfig**](inapcomponentconfig-getconfig.md) method may be imported onto an x64 machine using the **SetConfig** method, and vice versa.</span></span> <span data-ttu-id="b7923-116">Par conséquent, les données de configuration doivent être dans un format indépendant de l’architecture, tel que XML.</span><span class="sxs-lookup"><span data-stu-id="b7923-116">Therefore, configuration data must be in an architecture-agnostic format such as XML.</span></span> <span data-ttu-id="b7923-117">L’utilisation de XML au lieu d’un flux d’octets permet d’utiliser plus facilement des données de configuration sur différentes architectures.</span><span class="sxs-lookup"><span data-stu-id="b7923-117">Using XML instead of a byte stream makes it easier to use configuration data on different architectures.</span></span> <span data-ttu-id="b7923-118">Les éléments XML utilisés dans les données de configuration sont déterminés par l’implémenteur.</span><span class="sxs-lookup"><span data-stu-id="b7923-118">The XML elements used in the configuration data are determined by the implementer.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7923-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7923-119">Return value</span></span>

<span data-ttu-id="b7923-120">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="b7923-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="b7923-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b7923-121">Return code</span></span>                                                                                     | <span data-ttu-id="b7923-122">Description</span><span class="sxs-lookup"><span data-stu-id="b7923-122">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7923-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b7923-123"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b7923-124">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b7923-124">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="b7923-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b7923-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b7923-126">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="b7923-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b7923-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b7923-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b7923-128">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="b7923-128">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b7923-129">Notes</span><span class="sxs-lookup"><span data-stu-id="b7923-129">Remarks</span></span>

<span data-ttu-id="b7923-130">Les informations de contrôle de version des composants doivent être incluses dans l’objet blob de configuration de *données* .</span><span class="sxs-lookup"><span data-stu-id="b7923-130">Component versioning information should be included in the *data* configuration blob.</span></span> <span data-ttu-id="b7923-131">Les informations de contrôle de version peuvent être utilisées lors de la migration d’une version de SHV vers une autre.</span><span class="sxs-lookup"><span data-stu-id="b7923-131">The versioning information may be used when migrating from one SHV version to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7923-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7923-132">Requirements</span></span>



| <span data-ttu-id="b7923-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7923-133">Requirement</span></span> | <span data-ttu-id="b7923-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7923-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7923-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7923-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b7923-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7923-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b7923-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7923-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b7923-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7923-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b7923-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7923-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7923-140"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7923-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7923-141">MIDL</span><span class="sxs-lookup"><span data-stu-id="b7923-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b7923-142"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7923-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7923-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7923-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7923-144">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="b7923-144">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="b7923-145">**INapConponentConfig :: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="b7923-145">**INapConponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)
</dt> </dl>

 

 





