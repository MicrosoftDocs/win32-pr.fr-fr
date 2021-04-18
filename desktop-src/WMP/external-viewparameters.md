---
title: External. viewParameters
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. viewParameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- External. viewParameters Windows Media Player
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533080"
---
# <a name="externalviewparameters"></a><span data-ttu-id="828d8-105">External. viewParameters</span><span class="sxs-lookup"><span data-stu-id="828d8-105">External.viewParameters</span></span>

> [!Note]  
> <span data-ttu-id="828d8-106">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="828d8-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="828d8-107">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="828d8-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="828d8-108">La propriété **viewParameters** récupère les paramètres associés à la vue actuelle dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="828d8-108">The **viewParameters** property retrieves parameters associated with the current view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="828d8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="828d8-109">Syntax</span></span>

<span data-ttu-id="828d8-110">**Window. external. viewParameters**</span><span class="sxs-lookup"><span data-stu-id="828d8-110">**window.external.viewParameters**</span></span>

## <a name="possible-values"></a><span data-ttu-id="828d8-111">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="828d8-111">Possible Values</span></span>

<span data-ttu-id="828d8-112">Cette propriété retourne une **chaîne** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="828d8-112">This property returns a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="828d8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="828d8-113">Remarks</span></span>

<span data-ttu-id="828d8-114">Cette propriété récupère les paramètres qui ont été définis précédemment par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="828d8-114">This property retrieves parameters that were previously set by the online store.</span></span> <span data-ttu-id="828d8-115">Par exemple, le magasin en ligne peut spécifier des paramètres d’affichage dans le paramètre *ViewParams* de la méthode [changeView](external-changeview.md) ou le paramètre *params* de la méthode [changeViewOnlineList](external-changeviewonlinelist.md) .</span><span class="sxs-lookup"><span data-stu-id="828d8-115">For example, the online store can specify view parameters in the *ViewParams* parameter of the [changeView](external-changeview.md) method or the *Params* parameter of the [changeViewOnlineList](external-changeviewonlinelist.md) method.</span></span>

<span data-ttu-id="828d8-116">Les paramètres d’affichage ne sont pas interprétés par le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="828d8-116">View parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="828d8-117">Ils sont créés par le magasin en ligne et ont une signification uniquement pour le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="828d8-117">They are created by the online store and have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="828d8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="828d8-118">Requirements</span></span>



| <span data-ttu-id="828d8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="828d8-119">Requirement</span></span> | <span data-ttu-id="828d8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="828d8-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="828d8-121">Version</span><span class="sxs-lookup"><span data-stu-id="828d8-121">Version</span></span><br/> | <span data-ttu-id="828d8-122">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="828d8-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="828d8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="828d8-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="828d8-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="828d8-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="828d8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="828d8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="828d8-126">**Objet externe pour les magasins de type 1 en ligne**</span><span class="sxs-lookup"><span data-stu-id="828d8-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





