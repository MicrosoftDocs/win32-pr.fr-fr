---
title: Méthode INapComponentConfig3 SetConfigToID (NapCommon. h)
description: Est implémenté par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de définir les données de configuration pour un ID de configuration spécifique.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Méthode SetConfigToID NAP
- Méthode SetConfigToID NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, méthode SetConfigToID
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513045"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a><span data-ttu-id="dc206-106">INapComponentConfig3 :: SetConfigToID, méthode</span><span class="sxs-lookup"><span data-stu-id="dc206-106">INapComponentConfig3::SetConfigToID method</span></span>

> [!Note]  
> <span data-ttu-id="dc206-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="dc206-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dc206-108">La méthode **SetConfigToID** est implémentée par les validateurs d’intégrité système (SHV) pour fournir un moyen de définir les données de configuration pour un ID de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="dc206-108">The **SetConfigToID** method is implemented by system health validators (SHVs) to provide a way to set the configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc206-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc206-109">Syntax</span></span>


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="dc206-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc206-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc206-111">*configID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc206-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc206-112">Valeur qui représente la configuration.</span><span class="sxs-lookup"><span data-stu-id="dc206-112">A value that represents the configuration.</span></span> <span data-ttu-id="dc206-113">*ConfigId* est attribué par le service NPS (Network Policy Server) et est unique dans la SHV.</span><span class="sxs-lookup"><span data-stu-id="dc206-113">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span> <span data-ttu-id="dc206-114">Si *configId* a la valeur 0, la configuration par défaut de l’SHV est définie.</span><span class="sxs-lookup"><span data-stu-id="dc206-114">If *ConfigID* is 0, the default configuration of the SHV is set.</span></span>

</dd> <dt>

<span data-ttu-id="dc206-115">*nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc206-115">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc206-116">Taille, en octets, des données de configuration dans les *données*.</span><span class="sxs-lookup"><span data-stu-id="dc206-116">The size, in bytes, of the configuration data in *data*.</span></span>

</dd> <dt>

<span data-ttu-id="dc206-117">*données* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc206-117">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc206-118">En entrée, tableau d’octets qui contient les données de configuration définies sur *configId*.</span><span class="sxs-lookup"><span data-stu-id="dc206-118">On input, a BYTE array that contains the configuration data set to *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc206-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc206-119">Return value</span></span>

<span data-ttu-id="dc206-120">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="dc206-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="dc206-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dc206-121">Return code</span></span>                                                                                                    | <span data-ttu-id="dc206-122">Description</span><span class="sxs-lookup"><span data-stu-id="dc206-122">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="dc206-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc206-123"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="dc206-124">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="dc206-124">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="dc206-125"><dt>**configuration de NAP \_ E \_ SHV \_ \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="dc206-125"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="dc206-126">*ConfigId* introuvable.</span><span class="sxs-lookup"><span data-stu-id="dc206-126">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="dc206-127">Notes</span><span class="sxs-lookup"><span data-stu-id="dc206-127">Remarks</span></span>

<span data-ttu-id="dc206-128">La méthode [**newconfig**](inapcomponentconfig3-newconfig.md) doit être utilisée pour allouer des données de configuration pour *configId* avant que cette méthode puisse être appelée.</span><span class="sxs-lookup"><span data-stu-id="dc206-128">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc206-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc206-129">Requirements</span></span>



| <span data-ttu-id="dc206-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc206-130">Requirement</span></span> | <span data-ttu-id="dc206-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc206-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc206-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc206-132">Minimum supported client</span></span><br/> | <span data-ttu-id="dc206-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc206-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="dc206-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc206-134">Minimum supported server</span></span><br/> | <span data-ttu-id="dc206-135">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc206-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc206-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc206-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc206-137"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc206-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc206-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="dc206-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc206-139"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc206-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc206-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc206-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc206-141">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="dc206-141">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





