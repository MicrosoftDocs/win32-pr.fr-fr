---
title: Méthode INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon. h)
description: Est implémenté par les validateurs d’intégrité système (SHV) si nécessaire pour charger la configuration d’un ordinateur distant ou local en mémoire et afficher une interface utilisateur qui autorise la manipulation des données de configuration.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Méthode InvokeUIFromConfigBlob NAP
- Méthode InvokeUIFromConfigBlob NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, méthode InvokeUIFromConfigBlob
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54cc1efaf7da3434e1aff10d57c2e175481a3d2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843338"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a><span data-ttu-id="7365b-106">INapComponentConfig2 :: InvokeUIFromConfigBlob, méthode</span><span class="sxs-lookup"><span data-stu-id="7365b-106">INapComponentConfig2::InvokeUIFromConfigBlob method</span></span>

> [!Note]  
> <span data-ttu-id="7365b-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="7365b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7365b-108">La méthode **InvokeUIFromConfigBlob** est implémentée par les validateurs d’intégrité système (SHV) si nécessaire pour charger la configuration d’un ordinateur distant ou local en mémoire et afficher une interface utilisateur qui permet de manipuler les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="7365b-108">The **InvokeUIFromConfigBlob** method is implemented by system health validators (SHVs) as needed to load the configuration of a remote or local machine in memory and display a UI that allows manipulation of the configuration data.</span></span> <span data-ttu-id="7365b-109">Le composant de configuration doit prendre en charge l’utilisation de [**INapComponentConfig**](inapcomponentconfig.md) via DCOM.</span><span class="sxs-lookup"><span data-stu-id="7365b-109">The configuration component must support the usage of [**INapComponentConfig**](inapcomponentconfig.md) through DCOM.</span></span>

## <a name="syntax"></a><span data-ttu-id="7365b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7365b-110">Syntax</span></span>


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a><span data-ttu-id="7365b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7365b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7365b-112">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7365b-112">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7365b-113">Handle de la fenêtre parente ou propriétaire.</span><span class="sxs-lookup"><span data-stu-id="7365b-113">A handle to the parent or owner window.</span></span> <span data-ttu-id="7365b-114">Un handle de fenêtre valide doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="7365b-114">A valid window handle must be supplied.</span></span>

</dd> <dt>

<span data-ttu-id="7365b-115">*inbCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7365b-115">*inbCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7365b-116">Taille, en octets, des *indonnées*.</span><span class="sxs-lookup"><span data-stu-id="7365b-116">The size, in bytes, of *inData*.</span></span>

</dd> <dt>

<span data-ttu-id="7365b-117">*Indonnées* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7365b-117">*inData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7365b-118">Pointeur vers une mémoire tampon qui stocke les données de configuration initiales.</span><span class="sxs-lookup"><span data-stu-id="7365b-118">A pointer to a buffer that stores the initial configuration data.</span></span> <span data-ttu-id="7365b-119">Ces données sont exportées à partir de l’ordinateur distant ou local.</span><span class="sxs-lookup"><span data-stu-id="7365b-119">This data is exported from the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="7365b-120">*outbCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7365b-120">*outbCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7365b-121">Taille, en octets, des *données* de l’octet.</span><span class="sxs-lookup"><span data-stu-id="7365b-121">The size, in bytes, of *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="7365b-122">*données* \[ de l' à\]</span><span class="sxs-lookup"><span data-stu-id="7365b-122">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7365b-123">Pointeur vers une mémoire tampon qui stocke les données de configuration modifiées par l’interface utilisateur de configuration SHV.</span><span class="sxs-lookup"><span data-stu-id="7365b-123">A pointer to a buffer that stores configuration data changed by the SHV configuration user interface.</span></span> <span data-ttu-id="7365b-124">Ces données sont importées par l’ordinateur distant ou local.</span><span class="sxs-lookup"><span data-stu-id="7365b-124">This data is imported by the remote or local machine.</span></span>

</dd> <dt>

<span data-ttu-id="7365b-125">*fConfigChanged* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7365b-125">*fConfigChanged* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7365b-126">Pointeur vers un **booléen** dont la valeur est **true** si la configuration a été modifiée pendant l’opération d’interface utilisateur et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7365b-126">A pointer to a **BOOL** that is set to **TRUE** if the configuration was changed during the UI operation and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7365b-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7365b-127">Return value</span></span>

<span data-ttu-id="7365b-128">Retourne S \_ OK en cas de réussite, ou l’un des codes d’erreur Windows standard.</span><span class="sxs-lookup"><span data-stu-id="7365b-128">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="7365b-129">Notes</span><span class="sxs-lookup"><span data-stu-id="7365b-129">Remarks</span></span>

<span data-ttu-id="7365b-130">S’il est utilisé pour un ordinateur local, cette fonction peut être utilisée pour la configuration SHV de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="7365b-130">If used for a local machine, this function can be used for per policy SHV configuration.</span></span> <span data-ttu-id="7365b-131">Il offre un moyen d’appeler une interface utilisateur SHV et de modifier une configuration SHV existante.</span><span class="sxs-lookup"><span data-stu-id="7365b-131">It provides a way to invoke an SHV UI and edit an existing SHV configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="7365b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7365b-132">Requirements</span></span>



| <span data-ttu-id="7365b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7365b-133">Requirement</span></span> | <span data-ttu-id="7365b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="7365b-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7365b-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7365b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7365b-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7365b-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7365b-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7365b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7365b-138">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7365b-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7365b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="7365b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7365b-140"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7365b-140"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="7365b-141">MIDL</span><span class="sxs-lookup"><span data-stu-id="7365b-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7365b-142"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7365b-142"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7365b-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7365b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7365b-144">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="7365b-144">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





