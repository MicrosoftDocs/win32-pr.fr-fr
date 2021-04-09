---
title: Méthode INapComponentConfig3 NewConfig (NapCommon. h)
description: Est implémenté par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de créer des données de configuration pour un ID de configuration spécifique.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Méthode NewConfig NAP
- Méthode NewConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, méthode NewConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103297"
---
# <a name="inapcomponentconfig3newconfig-method"></a><span data-ttu-id="ffad8-106">INapComponentConfig3 :: NewConfig, méthode</span><span class="sxs-lookup"><span data-stu-id="ffad8-106">INapComponentConfig3::NewConfig method</span></span>

> [!Note]  
> <span data-ttu-id="ffad8-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="ffad8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ffad8-108">La méthode **newconfig** est implémentée par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de créer des données de configuration pour un ID de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="ffad8-108">The **NewConfig** method is implemented by system health validators (SHVs) to provide a way to create configuration data for a specific configuration ID.</span></span> <span data-ttu-id="ffad8-109">Lorsque cette fonction est appelée, un SHV doit allouer de nouvelles données de configuration et les remplir avec une copie des données de configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="ffad8-109">When this function is called, an SHV must allocate new configuration data and populate it with a copy of the default configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffad8-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffad8-110">Syntax</span></span>


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="ffad8-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ffad8-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffad8-112">*configID*</span><span class="sxs-lookup"><span data-stu-id="ffad8-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="ffad8-113">Valeur qui représente la configuration.</span><span class="sxs-lookup"><span data-stu-id="ffad8-113">A value that represents the configuration.</span></span> <span data-ttu-id="ffad8-114">*ConfigId* est attribué par le service NPS (Network Policy Server) et est unique dans la SHV.</span><span class="sxs-lookup"><span data-stu-id="ffad8-114">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffad8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ffad8-115">Return value</span></span>

<span data-ttu-id="ffad8-116">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="ffad8-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="ffad8-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ffad8-117">Return code</span></span>                                                                                                 | <span data-ttu-id="ffad8-118">Description</span><span class="sxs-lookup"><span data-stu-id="ffad8-118">Description</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ffad8-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-119"><dt>**S\_OK** </dt></span></span> </dl>                       | <span data-ttu-id="ffad8-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ffad8-120">The operation is successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="ffad8-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="ffad8-122">*ConfigId* est égal à 0 (valeur réservée pour la configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="ffad8-122">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/>                  |
| <dl> <span data-ttu-id="ffad8-123"><dt>**la \_ configuration NAP E \_ SHV \_ \_ existait**</dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-123"><dt>**NAP\_E\_SHV\_CONFIG\_EXISTED**</dt></span></span> </dl> | <span data-ttu-id="ffad8-124">*ConfigId* existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ffad8-124">*ConfigID* already exists.</span></span> <span data-ttu-id="ffad8-125">La liste des ID connus du serveur NPS est différente de la SHV.</span><span class="sxs-lookup"><span data-stu-id="ffad8-125">The list of IDs known to NPS is different from the SHV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ffad8-126">Notes</span><span class="sxs-lookup"><span data-stu-id="ffad8-126">Remarks</span></span>

<span data-ttu-id="ffad8-127">Une fois la nouvelle configuration créée par **newconfig**, les méthodes [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)et [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) doivent être utilisées pour modifier la configuration en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="ffad8-127">After the new configuration is created by **NewConfig**, the [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md), and [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) methods should be used to alter the configuration as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffad8-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffad8-128">Requirements</span></span>



| <span data-ttu-id="ffad8-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffad8-129">Requirement</span></span> | <span data-ttu-id="ffad8-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffad8-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffad8-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffad8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ffad8-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffad8-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ffad8-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffad8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ffad8-134">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffad8-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ffad8-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffad8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffad8-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="ffad8-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="ffad8-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ffad8-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ffad8-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffad8-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffad8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffad8-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="ffad8-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





