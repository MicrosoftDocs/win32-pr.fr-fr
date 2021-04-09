---
title: Interface INapSoHConstructor (NapProtocol. h)
description: Sont utilisés par l’SHA pour construire SoHRequests et par les programmes de validation d’intégrité système pour construire SoHResponses.
ms.assetid: ad79c80a-3003-4465-b350-77890c217d63
keywords:
- NAP de l’interface INapSoHConstructor
- INapSoHConstructor interface NAP, Description
topic_type:
- apiref
api_name:
- INapSoHConstructor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 546a6d3b4ec262fdd725af24211338e848b2b848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941729"
---
# <a name="inapsohconstructor-interface"></a><span data-ttu-id="a6ae7-105">Interface INapSoHConstructor</span><span class="sxs-lookup"><span data-stu-id="a6ae7-105">INapSoHConstructor interface</span></span>

> [!Note]  
> <span data-ttu-id="a6ae7-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a6ae7-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a6ae7-107">**INapSoHConstructor** fournit des méthodes qui sont utilisées par l’SHA pour construire des [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) et par les validateurs d’intégrité du système pour construire **SoHResponses**.</span><span class="sxs-lookup"><span data-stu-id="a6ae7-107">The **INapSoHConstructor** provides methods that are used by SHAs to construct [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to construct **SoHResponses**.</span></span>

## <a name="members"></a><span data-ttu-id="a6ae7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="a6ae7-108">Members</span></span>

<span data-ttu-id="a6ae7-109">L’interface **INapSoHConstructor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a6ae7-109">The **INapSoHConstructor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a6ae7-110">**INapSoHConstructor** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a6ae7-110">**INapSoHConstructor** also has these types of members:</span></span>

-   [<span data-ttu-id="a6ae7-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a6ae7-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a6ae7-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a6ae7-112">Methods</span></span>

<span data-ttu-id="a6ae7-113">L’interface **INapSoHConstructor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a6ae7-113">The **INapSoHConstructor** interface has these methods.</span></span>



| <span data-ttu-id="a6ae7-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="a6ae7-114">Method</span></span>                                                                                   | <span data-ttu-id="a6ae7-115">Description</span><span class="sxs-lookup"><span data-stu-id="a6ae7-115">Description</span></span>                                         |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------|
| [<span data-ttu-id="a6ae7-116">**INapSoHConstructor::AppendAttribute**</span><span class="sxs-lookup"><span data-stu-id="a6ae7-116">**INapSoHConstructor::AppendAttribute**</span></span>](inapsohconstructor-appendattribute-method.md) | <span data-ttu-id="a6ae7-117">Ajoute un TLV à la fin de la mémoire tampon SoH.</span><span class="sxs-lookup"><span data-stu-id="a6ae7-117">Adds a TLV to the end of the SoH buffer.</span></span><br/> |
| [<span data-ttu-id="a6ae7-118">**INapSoHConstructor::GetSoH**</span><span class="sxs-lookup"><span data-stu-id="a6ae7-118">**INapSoHConstructor::GetSoH**</span></span>](inapsohconstructor-getsoh-method.md)                   | <span data-ttu-id="a6ae7-119">Récupère le paquet SoH construit.</span><span class="sxs-lookup"><span data-stu-id="a6ae7-119">Retrieves the constructed SoH packet.</span></span><br/>    |
| [<span data-ttu-id="a6ae7-120">**INapSoHConstructor :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="a6ae7-120">**INapSoHConstructor::Initialize**</span></span>](inapsohconstructor-initialize-method.md)           | <span data-ttu-id="a6ae7-121">Initialise le paquet SoH.</span><span class="sxs-lookup"><span data-stu-id="a6ae7-121">Initializes the SoH packet.</span></span><br/>              |
| [<span data-ttu-id="a6ae7-122">**INapSoHConstructor :: Validate**</span><span class="sxs-lookup"><span data-stu-id="a6ae7-122">**INapSoHConstructor::Validate**</span></span>](inapsohconstructor-validate-method.md)               | <span data-ttu-id="a6ae7-123">Vérifie la validité du paquet SoH.</span><span class="sxs-lookup"><span data-stu-id="a6ae7-123">Checks the validity of the SoH packet.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="a6ae7-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6ae7-124">Requirements</span></span>



| <span data-ttu-id="a6ae7-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6ae7-125">Requirement</span></span> | <span data-ttu-id="a6ae7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6ae7-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ae7-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ae7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ae7-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ae7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a6ae7-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ae7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ae7-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ae7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a6ae7-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6ae7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ae7-132"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6ae7-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6ae7-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="a6ae7-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6ae7-134"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6ae7-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="a6ae7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a6ae7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ae7-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6ae7-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="a6ae7-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6ae7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ae7-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="a6ae7-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a6ae7-139">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="a6ae7-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

