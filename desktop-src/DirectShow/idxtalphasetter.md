---
description: L’interface IDxtAlphaSetter définit les propriétés sur l’effet d’accesseur Set alpha. Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de l’effet d’accesseur Set alpha.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interface IDxtAlphaSetter (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530999"
---
# <a name="idxtalphasetter-interface"></a><span data-ttu-id="eb1da-103">Interface IDxtAlphaSetter</span><span class="sxs-lookup"><span data-stu-id="eb1da-103">IDxtAlphaSetter interface</span></span>

> [!Note]  
> <span data-ttu-id="eb1da-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="eb1da-104">\[Deprecated.</span></span> <span data-ttu-id="eb1da-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb1da-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="eb1da-106">L' `IDxtAlphaSetter` interface définit les propriétés sur l’effet d' [accesseur Set alpha](alpha-setter-effect.md) .</span><span class="sxs-lookup"><span data-stu-id="eb1da-106">The `IDxtAlphaSetter` interface sets properties on the [Alpha Setter](alpha-setter-effect.md) effect.</span></span>

<span data-ttu-id="eb1da-107">Cette interface est utilisée en interne par les services de modification DirectShow (DES) lors du rendu de l’effet d’accesseur Set alpha.</span><span class="sxs-lookup"><span data-stu-id="eb1da-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Alpha Setter effect.</span></span> <span data-ttu-id="eb1da-108">Les applications DES n’ont pas besoin d’utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="eb1da-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="eb1da-109">Pour définir les propriétés d’une transition dans DES, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="eb1da-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="eb1da-110">Membres</span><span class="sxs-lookup"><span data-stu-id="eb1da-110">Members</span></span>

<span data-ttu-id="eb1da-111">L’interface **IDxtAlphaSetter** hérite de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="eb1da-111">The **IDxtAlphaSetter** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="eb1da-112">**IDxtAlphaSetter** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eb1da-112">**IDxtAlphaSetter** also has these types of members:</span></span>

-   [<span data-ttu-id="eb1da-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eb1da-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eb1da-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eb1da-114">Methods</span></span>

<span data-ttu-id="eb1da-115">L’interface **IDxtAlphaSetter** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="eb1da-115">The **IDxtAlphaSetter** interface has these methods.</span></span>



| <span data-ttu-id="eb1da-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="eb1da-116">Method</span></span>                                                  | <span data-ttu-id="eb1da-117">Description</span><span class="sxs-lookup"><span data-stu-id="eb1da-117">Description</span></span>                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="eb1da-118">**récupération \_ alpha**</span><span class="sxs-lookup"><span data-stu-id="eb1da-118">**get\_Alpha**</span></span>](idxtalphasetter-get-alpha.md)         | <span data-ttu-id="eb1da-119">Récupère la valeur alpha de la totalité de l’image.</span><span class="sxs-lookup"><span data-stu-id="eb1da-119">Retrieves the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="eb1da-120">**Obtient \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="eb1da-120">**get\_AlphaRamp**</span></span>](idxtalphasetter-get-alpharamp.md) | <span data-ttu-id="eb1da-121">Récupère la propriété de rampe alpha.</span><span class="sxs-lookup"><span data-stu-id="eb1da-121">Retrieves the alpha ramp property.</span></span><br/>              |
| [<span data-ttu-id="eb1da-122">**put \_ alpha**</span><span class="sxs-lookup"><span data-stu-id="eb1da-122">**put\_Alpha**</span></span>](idxtalphasetter-put-alpha.md)         | <span data-ttu-id="eb1da-123">Spécifie la valeur alpha de la totalité de l’image.</span><span class="sxs-lookup"><span data-stu-id="eb1da-123">Specifies the alpha value for the entire image.</span></span><br/> |
| [<span data-ttu-id="eb1da-124">**put \_ AlphaRamp**</span><span class="sxs-lookup"><span data-stu-id="eb1da-124">**put\_AlphaRamp**</span></span>](idxtalphasetter-put-alpharamp.md) | <span data-ttu-id="eb1da-125">Spécifie la propriété de rampe alpha.</span><span class="sxs-lookup"><span data-stu-id="eb1da-125">Specifies the alpha ramp property.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="eb1da-126">Notes</span><span class="sxs-lookup"><span data-stu-id="eb1da-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="eb1da-127">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="eb1da-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="eb1da-128">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="eb1da-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="eb1da-129">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="eb1da-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eb1da-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb1da-130">Requirements</span></span>



| <span data-ttu-id="eb1da-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb1da-131">Requirement</span></span> | <span data-ttu-id="eb1da-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb1da-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb1da-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb1da-133">Header</span></span><br/>  | <dl> <span data-ttu-id="eb1da-134"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb1da-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="eb1da-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eb1da-135">Library</span></span><br/> | <dl> <span data-ttu-id="eb1da-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb1da-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




