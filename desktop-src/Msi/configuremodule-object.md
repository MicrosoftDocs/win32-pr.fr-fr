---
description: L’objet ConfigureModule est une interface implémentée par le client.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Objet ConfigureModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531104"
---
# <a name="configuremodule-object"></a><span data-ttu-id="74cce-103">Objet ConfigureModule</span><span class="sxs-lookup"><span data-stu-id="74cce-103">ConfigureModule object</span></span>

<span data-ttu-id="74cce-104">L' **objet ConfigureModule** est une interface implémentée par le client.</span><span class="sxs-lookup"><span data-stu-id="74cce-104">The **ConfigureModule object** is an interface implemented by the client.</span></span> <span data-ttu-id="74cce-105">Mergemod.dllappelle des méthodes sur l’interface **IMsmConfigureModule** pour demander que l’outil client fournisse des informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="74cce-105">Mergemod.dllcalls methods on the **IMsmConfigureModule** interface to request that the client tool provide configuration information.</span></span> <span data-ttu-id="74cce-106">Le module est configuré en fonction des réponses du client aux appels sur cette interface.</span><span class="sxs-lookup"><span data-stu-id="74cce-106">The module is configured based on the client's responses to calls on this interface.</span></span>

## <a name="members"></a><span data-ttu-id="74cce-107">Membres</span><span class="sxs-lookup"><span data-stu-id="74cce-107">Members</span></span>

<span data-ttu-id="74cce-108">L’objet **ConfigureModule** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="74cce-108">The **ConfigureModule** object has these types of members:</span></span>

-   [<span data-ttu-id="74cce-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="74cce-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="74cce-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="74cce-110">Methods</span></span>

<span data-ttu-id="74cce-111">L’objet **ConfigureModule** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="74cce-111">The **ConfigureModule** object has these methods.</span></span>



| <span data-ttu-id="74cce-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="74cce-112">Method</span></span>                                                           | <span data-ttu-id="74cce-113">Description</span><span class="sxs-lookup"><span data-stu-id="74cce-113">Description</span></span>                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="74cce-114">**ProvideIntegerData**</span><span class="sxs-lookup"><span data-stu-id="74cce-114">**ProvideIntegerData**</span></span>](configuremodule-provideintegerdata.md) | <span data-ttu-id="74cce-115">Appelée par Mergemod.dll pour obtenir des entiers utilisés pour configurer le module.</span><span class="sxs-lookup"><span data-stu-id="74cce-115">Called by Mergemod.dll to obtain integers used to configure the module.</span></span><br/> |
| [<span data-ttu-id="74cce-116">**ProvideTextData**</span><span class="sxs-lookup"><span data-stu-id="74cce-116">**ProvideTextData**</span></span>](configuremodule-providetextdata.md)       | <span data-ttu-id="74cce-117">Appelée par Mergemod.dll pour obtenir le texte utilisé pour configurer le module.</span><span class="sxs-lookup"><span data-stu-id="74cce-117">Called by Mergemod.dll to obtain text used to configure the module.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="74cce-118">Notes</span><span class="sxs-lookup"><span data-stu-id="74cce-118">Remarks</span></span>

### <a name="c"></a><span data-ttu-id="74cce-119">C++</span><span class="sxs-lookup"><span data-stu-id="74cce-119">C++</span></span>

<span data-ttu-id="74cce-120">interface **IMsmConfigureModule : IDispatch**</span><span class="sxs-lookup"><span data-stu-id="74cce-120">interface **IMsmConfigureModule : IDispatch**</span></span>

### <a name="interface-id"></a><span data-ttu-id="74cce-121">ID d’interface</span><span class="sxs-lookup"><span data-stu-id="74cce-121">Interface ID</span></span>



| <span data-ttu-id="74cce-122">Constante</span><span class="sxs-lookup"><span data-stu-id="74cce-122">Constant</span></span>                     | <span data-ttu-id="74cce-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="74cce-123">Value</span></span>                                  |
|------------------------------|----------------------------------------|
| <span data-ttu-id="74cce-124">**IID \_ IMsmConfigureModule**</span><span class="sxs-lookup"><span data-stu-id="74cce-124">**IID\_IMsmConfigureModule**</span></span> | <span data-ttu-id="74cce-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span><span class="sxs-lookup"><span data-stu-id="74cce-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="74cce-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74cce-126">Requirements</span></span>



| <span data-ttu-id="74cce-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74cce-127">Requirement</span></span> | <span data-ttu-id="74cce-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="74cce-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74cce-129">Version</span><span class="sxs-lookup"><span data-stu-id="74cce-129">Version</span></span><br/> | <span data-ttu-id="74cce-130">Mergemod.dll 2,0 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="74cce-130">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="74cce-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="74cce-131">Header</span></span><br/>  | <dl> <span data-ttu-id="74cce-132"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="74cce-132"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="74cce-133">DLL</span><span class="sxs-lookup"><span data-stu-id="74cce-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="74cce-134"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74cce-134"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




