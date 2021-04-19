---
description: L’interface IProvidePropertyBuilder, lorsqu’elle est implémentée, permet aux objets de spécifier des objets de générateur de propriétés pour les propriétés.
ms.assetid: 26557622-4a97-4db0-85ed-3f77fcb769a0
title: Interface IProvidePropertyBuilder
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IProvidePropertyBuilder:IUnknown
api_type:
- COM
api_location:
- Vsp.dll
ms.openlocfilehash: b93d05c3c64686b21f19ffe6262ddfd68812dd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520812"
---
# <a name="iprovidepropertybuilder-interface"></a><span data-ttu-id="1a2fe-103">Interface IProvidePropertyBuilder</span><span class="sxs-lookup"><span data-stu-id="1a2fe-103">IProvidePropertyBuilder interface</span></span>

<span data-ttu-id="1a2fe-104">L’interface **IProvidePropertyBuilder** , lorsqu’elle est implémentée, permet aux objets de spécifier des objets de générateur de propriétés pour les propriétés.</span><span class="sxs-lookup"><span data-stu-id="1a2fe-104">The **IProvidePropertyBuilder** interface, when implemented, allows objects to specify property builder objects for properties.</span></span> <span data-ttu-id="1a2fe-105">Les générateurs sont appelés par un bouton de sélection ( \[ ... \] ) dans l’Explorateur de propriétés Microsoft Visual Studio et sont appelés via [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) quand le bouton est enfoncé.</span><span class="sxs-lookup"><span data-stu-id="1a2fe-105">Builders are invoked by an ellipsis button (\[...\]) on the Microsoft Visual Studio property browser and is invoked through [**ExecuteBuilder**](iprovidepropertybuilder-executebuilder.md) when the button is pressed.</span></span> <span data-ttu-id="1a2fe-106">Pour fournir un générateur pour une propriété donnée, retournez un GUID pour le générateur de propriétés qui doit être appelé pour la propriété actuelle à partir de [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span><span class="sxs-lookup"><span data-stu-id="1a2fe-106">To supply a builder for a given property, return a GUID for the property builder that should be invoked for the current property from [**MapPropertyToBuilder**](iprovidepropertybuilder-mappropertytobuilder.md).</span></span> <span data-ttu-id="1a2fe-107">Les générateurs sont généralement implémentés par le biais de boîtes de dialogue modales.</span><span class="sxs-lookup"><span data-stu-id="1a2fe-107">Builders are generally implemented through modal dialog boxes.</span></span>

<span data-ttu-id="1a2fe-108">La version de cette interface est 1,0.</span><span class="sxs-lookup"><span data-stu-id="1a2fe-108">The version for this interface is 1.0.</span></span> <span data-ttu-id="1a2fe-109">Les appels de méthode sont reçus au niveau d’un point de terminaison attribué dynamiquement (comme décrit dans la documentation binaire MSMQ sur le mappage de point de terminaison) et utilisent l’UUID (identificateur unique universel) « 33C0C1D8-33CF-11d3-BFF2-00C04F990235 ».</span><span class="sxs-lookup"><span data-stu-id="1a2fe-109">Method calls are received at a dynamically assigned endpoint (as described in the MSMQ binary documentation on endpoint mapping) and use the UUID (universally unique identifier) "33C0C1D8-33CF-11d3-BFF2-00C04F990235".</span></span>

## <a name="members"></a><span data-ttu-id="1a2fe-110">Membres</span><span class="sxs-lookup"><span data-stu-id="1a2fe-110">Members</span></span>

<span data-ttu-id="1a2fe-111">L’interface **IProvidePropertyBuilder : IUnknown** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1a2fe-111">The **IProvidePropertyBuilder:IUnknown** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1a2fe-112">**IProvidePropertyBuilder** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1a2fe-112">**IProvidePropertyBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="1a2fe-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1a2fe-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1a2fe-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1a2fe-114">Methods</span></span>

<span data-ttu-id="1a2fe-115">L’interface **IProvidePropertyBuilder : IUnknown** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="1a2fe-115">The **IProvidePropertyBuilder:IUnknown** interface has these methods.</span></span>



| <span data-ttu-id="1a2fe-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="1a2fe-116">Method</span></span>                                                                       | <span data-ttu-id="1a2fe-117">Description</span><span class="sxs-lookup"><span data-stu-id="1a2fe-117">Description</span></span>                                                                                  |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a2fe-118">**ExecuteBuilder**</span><span class="sxs-lookup"><span data-stu-id="1a2fe-118">**ExecuteBuilder**</span></span>](iprovidepropertybuilder-executebuilder.md)             | <span data-ttu-id="1a2fe-119">Avertit un objet qu’il doit afficher son générateur pour la propriété spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1a2fe-119">Notifies an object that it should display its builder for the specified property.</span></span><br/> |
| [<span data-ttu-id="1a2fe-120">**MapPropertyToBuilder**</span><span class="sxs-lookup"><span data-stu-id="1a2fe-120">**MapPropertyToBuilder**</span></span>](iprovidepropertybuilder-mappropertytobuilder.md) | <span data-ttu-id="1a2fe-121">Vérifie si un générateur doit être associé à une propriété particulière.</span><span class="sxs-lookup"><span data-stu-id="1a2fe-121">Checks whether a builder should be associated with a particular property.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="1a2fe-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a2fe-122">Requirements</span></span>



| <span data-ttu-id="1a2fe-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a2fe-123">Requirement</span></span> | <span data-ttu-id="1a2fe-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a2fe-124">Value</span></span> |
|----------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a2fe-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1a2fe-125">DLL</span></span><br/> | <dl> <span data-ttu-id="1a2fe-126"><dt>Vsp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a2fe-126"><dt>Vsp.dll</dt></span></span> </dl> |



 

 
