---
title: Méthode INapComponentConfig3 GetConfigFromID (NapCommon. h)
description: Est implémenté par les programmes de validation d’intégrité système (SHV) pour fournir un moyen d’obtenir des données de configuration pour un ID de configuration spécifique.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Méthode GetConfigFromID NAP
- Méthode GetConfigFromID NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, méthode GetConfigFromID
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740940"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a><span data-ttu-id="b27ac-106">INapComponentConfig3 :: GetConfigFromID, méthode</span><span class="sxs-lookup"><span data-stu-id="b27ac-106">INapComponentConfig3::GetConfigFromID method</span></span>

> [!Note]  
> <span data-ttu-id="b27ac-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b27ac-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b27ac-108">La méthode **GetConfigFromID** est implémentée par les programmes de validation d’intégrité système (SHV) pour fournir un moyen d’obtenir des données de configuration pour un ID de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="b27ac-108">The **GetConfigFromID** method is implemented by system health validators (SHVs) to provide a way to obtain configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="b27ac-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b27ac-109">Syntax</span></span>


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a><span data-ttu-id="b27ac-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b27ac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b27ac-111">*configID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b27ac-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b27ac-112">Valeur qui représente la configuration.</span><span class="sxs-lookup"><span data-stu-id="b27ac-112">A value that represents the configuration.</span></span> <span data-ttu-id="b27ac-113">Si *configId* a la **valeur 0**, le validateur doit retourner les données de configuration par défaut dans les *données de données*.</span><span class="sxs-lookup"><span data-stu-id="b27ac-113">If *ConfigID* is **0**, the SHV should return the default configuration data in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="b27ac-114">*nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b27ac-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b27ac-115">Taille, en octets, des données de configuration retournées dans les *données de données*.</span><span class="sxs-lookup"><span data-stu-id="b27ac-115">The size, in bytes, of the configuration data returned in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="b27ac-116">*données* \[ de l' à\]</span><span class="sxs-lookup"><span data-stu-id="b27ac-116">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b27ac-117">Au retour, tableau d’octets qui contient les données de configuration représentées par *configId*.</span><span class="sxs-lookup"><span data-stu-id="b27ac-117">On return, a BYTE array that contains the configuration data represented by *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b27ac-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b27ac-118">Return value</span></span>

<span data-ttu-id="b27ac-119">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="b27ac-119">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="b27ac-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b27ac-120">Return code</span></span>                                                                                                    | <span data-ttu-id="b27ac-121">Description</span><span class="sxs-lookup"><span data-stu-id="b27ac-121">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="b27ac-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b27ac-122"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="b27ac-123">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b27ac-123">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="b27ac-124"><dt>**configuration de NAP \_ E \_ SHV \_ \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="b27ac-124"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="b27ac-125">*ConfigId* introuvable.</span><span class="sxs-lookup"><span data-stu-id="b27ac-125">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="b27ac-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b27ac-126">Remarks</span></span>

<span data-ttu-id="b27ac-127">La méthode [**newconfig**](inapcomponentconfig3-newconfig.md) doit être utilisée pour allouer des données de configuration pour *configId* avant que cette méthode puisse être appelée.</span><span class="sxs-lookup"><span data-stu-id="b27ac-127">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="b27ac-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b27ac-128">Requirements</span></span>



| <span data-ttu-id="b27ac-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b27ac-129">Requirement</span></span> | <span data-ttu-id="b27ac-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b27ac-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b27ac-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b27ac-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b27ac-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b27ac-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b27ac-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b27ac-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b27ac-134">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b27ac-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b27ac-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="b27ac-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b27ac-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b27ac-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="b27ac-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="b27ac-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b27ac-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b27ac-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b27ac-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b27ac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b27ac-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="b27ac-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





