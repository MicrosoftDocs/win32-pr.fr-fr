---
title: Interface INapSoHProcessor (NapProtocol. h)
description: Sont utilisés par les Sha pour traiter le contenu de SoHResponses et par les validateurs d’intégrité du système pour traiter le contenu de SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- NAP de l’interface INapSoHProcessor
- INapSoHProcessor interface NAP, Description
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032384"
---
# <a name="inapsohprocessor-interface"></a><span data-ttu-id="cb649-105">Interface INapSoHProcessor</span><span class="sxs-lookup"><span data-stu-id="cb649-105">INapSoHProcessor interface</span></span>

> [!Note]  
> <span data-ttu-id="cb649-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="cb649-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cb649-107">**INapSoHProcessor** fournit des méthodes utilisées par les Sha pour traiter le contenu de [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) et par les validateurs d’intégrité du système pour traiter le contenu de **SoHRequests**.</span><span class="sxs-lookup"><span data-stu-id="cb649-107">The **INapSoHProcessor** provides methods that are used by SHAs to process the contents of [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to process the contents of **SoHRequests**.</span></span>

## <a name="members"></a><span data-ttu-id="cb649-108">Membres</span><span class="sxs-lookup"><span data-stu-id="cb649-108">Members</span></span>

<span data-ttu-id="cb649-109">L’interface **INapSoHProcessor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cb649-109">The **INapSoHProcessor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cb649-110">**INapSoHProcessor** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="cb649-110">**INapSoHProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="cb649-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb649-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cb649-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="cb649-112">Methods</span></span>

<span data-ttu-id="cb649-113">L’interface **INapSoHProcessor** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="cb649-113">The **INapSoHProcessor** interface has these methods.</span></span>



| <span data-ttu-id="cb649-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="cb649-114">Method</span></span>                                                                                           | <span data-ttu-id="cb649-115">Description</span><span class="sxs-lookup"><span data-stu-id="cb649-115">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb649-116">**INapSoHProcessor::FindNextAttribute**</span><span class="sxs-lookup"><span data-stu-id="cb649-116">**INapSoHProcessor::FindNextAttribute**</span></span>](inapsohprocessor-findnextattribute-method.md)         | <span data-ttu-id="cb649-117">Recherche l’index d’emplacement de l’attribut de paquet SoH suivant.</span><span class="sxs-lookup"><span data-stu-id="cb649-117">Finds the location index of the next SoH packet attribute.</span></span><br/>                 |
| [<span data-ttu-id="cb649-118">**INapSoHProcessor :: GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="cb649-118">**INapSoHProcessor::GetAttribute**</span></span>](inapsohprocessor-getattribute-method.md)                   | <span data-ttu-id="cb649-119">Récupère le type et la valeur de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="cb649-119">Retrieves the attribute type and value.</span></span><br/>                                    |
| [<span data-ttu-id="cb649-120">**INapSoHProcessor::GetNumberOfAttributes**</span><span class="sxs-lookup"><span data-stu-id="cb649-120">**INapSoHProcessor::GetNumberOfAttributes**</span></span>](inapsohprocessor-getnumberofattributes-method.md) | <span data-ttu-id="cb649-121">Récupère le nombre d’attributs contenus dans la SoH.</span><span class="sxs-lookup"><span data-stu-id="cb649-121">Retrieves the number of attributes contained in the SoH.</span></span><br/>                   |
| [<span data-ttu-id="cb649-122">**INapSoHProcessor :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="cb649-122">**INapSoHProcessor::Initialize**</span></span>](inapsohprocessor-initialize-method.md)                       | <span data-ttu-id="cb649-123">Initialise le paquet de protocole SoH et le système NAP pour le traitement du contenu.</span><span class="sxs-lookup"><span data-stu-id="cb649-123">Initializes the SoH protocol packet and NAP System for content processing.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cb649-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb649-124">Requirements</span></span>



| <span data-ttu-id="cb649-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb649-125">Requirement</span></span> | <span data-ttu-id="cb649-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb649-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb649-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb649-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cb649-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb649-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cb649-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb649-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cb649-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb649-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="cb649-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="cb649-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb649-132"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb649-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb649-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="cb649-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb649-134"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb649-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="cb649-135">DLL</span><span class="sxs-lookup"><span data-stu-id="cb649-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb649-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb649-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="cb649-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb649-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb649-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="cb649-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cb649-139">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="cb649-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

