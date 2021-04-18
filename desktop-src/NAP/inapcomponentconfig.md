---
title: Interface INapComponentConfig (NapCommon. h)
description: Fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système (SHV).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- NAP de l’interface INapComponentConfig
- INapComponentConfig interface NAP, Description
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384391"
---
# <a name="inapcomponentconfig-interface"></a><span data-ttu-id="8b10a-105">Interface INapComponentConfig</span><span class="sxs-lookup"><span data-stu-id="8b10a-105">INapComponentConfig interface</span></span>

> [!Note]  
> <span data-ttu-id="8b10a-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="8b10a-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8b10a-107">L’interface **INapComponentConfig** fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système (SHV).</span><span class="sxs-lookup"><span data-stu-id="8b10a-107">The **INapComponentConfig** interface provides NAP system configuration methods for system health validators (SHVs).</span></span>

> [!Note]  
> <span data-ttu-id="8b10a-108">[**INapComponentConfig2**](inapcomponentconfig2.md) et [**INapComponentConfig3**](inapcomponentconfig3.md) héritent de toutes les méthodes de cette interface et doivent être utilisés à la place.</span><span class="sxs-lookup"><span data-stu-id="8b10a-108">[**INapComponentConfig2**](inapcomponentconfig2.md) and [**INapComponentConfig3**](inapcomponentconfig3.md) inherit all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="8b10a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="8b10a-109">Members</span></span>

<span data-ttu-id="8b10a-110">L’interface **INapComponentConfig** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8b10a-110">The **INapComponentConfig** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8b10a-111">**INapComponentConfig** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8b10a-111">**INapComponentConfig** also has these types of members:</span></span>

-   [<span data-ttu-id="8b10a-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8b10a-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8b10a-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8b10a-113">Methods</span></span>

<span data-ttu-id="8b10a-114">L’interface **INapComponentConfig** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8b10a-114">The **INapComponentConfig** interface has these methods.</span></span>



| <span data-ttu-id="8b10a-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="8b10a-115">Method</span></span>                                                                          | <span data-ttu-id="8b10a-116">Description</span><span class="sxs-lookup"><span data-stu-id="8b10a-116">Description</span></span>                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b10a-117">**INapComponentConfig :: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="8b10a-117">**INapComponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)         | <span data-ttu-id="8b10a-118">Récupère la configuration du composant SHV.</span><span class="sxs-lookup"><span data-stu-id="8b10a-118">Retrieves the SHV component configuration.</span></span><br/>                                |
| [<span data-ttu-id="8b10a-119">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="8b10a-119">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)           | <span data-ttu-id="8b10a-120">Lance l’interface utilisateur personnalisée pour un composant SHV.</span><span class="sxs-lookup"><span data-stu-id="8b10a-120">Launches the customized user interface for an SHV component.</span></span><br/>              |
| [<span data-ttu-id="8b10a-121">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="8b10a-121">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md) | <span data-ttu-id="8b10a-122">Spécifie si le composant SHV prend en charge une interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="8b10a-122">Specifies whether the SHV component supports a customized user interface.</span></span><br/> |
| [<span data-ttu-id="8b10a-123">**INapComponentConfig::SetConfig**</span><span class="sxs-lookup"><span data-stu-id="8b10a-123">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)         | <span data-ttu-id="8b10a-124">Définit la configuration du composant SHV.</span><span class="sxs-lookup"><span data-stu-id="8b10a-124">Sets the SHV component configuration.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="8b10a-125">Notes</span><span class="sxs-lookup"><span data-stu-id="8b10a-125">Remarks</span></span>

<span data-ttu-id="8b10a-126">Cette interface ne doit pas être implémentée par les agents d’intégrité système (SHA) ou les clients de contrainte de mise en quarantaine (QEC).</span><span class="sxs-lookup"><span data-stu-id="8b10a-126">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b10a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b10a-127">Requirements</span></span>



| <span data-ttu-id="8b10a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b10a-128">Requirement</span></span> | <span data-ttu-id="8b10a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b10a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b10a-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b10a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8b10a-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b10a-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8b10a-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b10a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8b10a-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b10a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8b10a-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b10a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b10a-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b10a-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b10a-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="8b10a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b10a-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b10a-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b10a-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b10a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b10a-139">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="8b10a-139">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8b10a-140">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="8b10a-140">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

