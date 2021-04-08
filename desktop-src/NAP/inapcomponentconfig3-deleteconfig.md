---
title: Méthode INapComponentConfig3 DeleteConfig (NapCommon. h)
description: Est implémenté par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de supprimer des données de configuration pour un ID de configuration spécifique.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- Méthode DeleteConfig NAP
- Méthode DeleteConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, méthode DeleteConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740948"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a><span data-ttu-id="0e62d-106">INapComponentConfig3 ::D méthode eleteConfig</span><span class="sxs-lookup"><span data-stu-id="0e62d-106">INapComponentConfig3::DeleteConfig method</span></span>

> [!Note]  
> <span data-ttu-id="0e62d-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0e62d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0e62d-108">La méthode **DeleteConfig** est implémentée par les programmes de validation d’intégrité système (SHV) pour fournir un moyen de supprimer des données de configuration pour un ID de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="0e62d-108">The **DeleteConfig** method is implemented by system health validators (SHVs) to provide a way to delete configuration data for a specific configuration ID.</span></span> <span data-ttu-id="0e62d-109">L’ID peut être réutilisé une fois que les données de configuration ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="0e62d-109">The ID may be reused after the configuration data has been deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e62d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e62d-110">Syntax</span></span>


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="0e62d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e62d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e62d-112">*configID*</span><span class="sxs-lookup"><span data-stu-id="0e62d-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="0e62d-113">Valeur qui représente les données de configuration à supprimer.</span><span class="sxs-lookup"><span data-stu-id="0e62d-113">A value that represents the configuration data to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e62d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e62d-114">Return value</span></span>

<span data-ttu-id="0e62d-115">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="0e62d-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="0e62d-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0e62d-116">Return code</span></span>                                                                                                    | <span data-ttu-id="0e62d-117">Description</span><span class="sxs-lookup"><span data-stu-id="0e62d-117">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e62d-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e62d-118"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="0e62d-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0e62d-119">The operation is successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0e62d-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0e62d-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="0e62d-121">*ConfigId* est égal à 0 (valeur réservée pour la configuration par défaut).</span><span class="sxs-lookup"><span data-stu-id="0e62d-121">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/> |
| <dl> <span data-ttu-id="0e62d-122"><dt>**configuration de NAP \_ E \_ SHV \_ \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="0e62d-122"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="0e62d-123">*ConfigId* introuvable.</span><span class="sxs-lookup"><span data-stu-id="0e62d-123">*ConfigID* cannot be found.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="0e62d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e62d-124">Requirements</span></span>



| <span data-ttu-id="0e62d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e62d-125">Requirement</span></span> | <span data-ttu-id="0e62d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e62d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e62d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e62d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0e62d-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e62d-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0e62d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e62d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0e62d-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e62d-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e62d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="0e62d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e62d-132"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e62d-132"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e62d-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="0e62d-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0e62d-134"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0e62d-134"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e62d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e62d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e62d-136">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="0e62d-136">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





