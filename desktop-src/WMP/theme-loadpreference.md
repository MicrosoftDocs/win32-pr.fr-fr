---
title: THÈME. loadPreference
description: La méthode loadPreference charge une préférence à partir du Registre.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- THEMe. loadPreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526495"
---
# <a name="themeloadpreference"></a><span data-ttu-id="3375f-104">THÈME. loadPreference</span><span class="sxs-lookup"><span data-stu-id="3375f-104">THEME.loadPreference</span></span>

<span data-ttu-id="3375f-105">La méthode **loadPreference** charge une préférence à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="3375f-105">The **loadPreference** method loads a preference from the registry.</span></span>

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a><span data-ttu-id="3375f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3375f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3375f-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="3375f-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="3375f-108">**Chaîne** spécifiant la clé de la valeur de préférence à charger.</span><span class="sxs-lookup"><span data-stu-id="3375f-108">A **String** specifying the key of the preference value to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3375f-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3375f-109">Return Value</span></span>

<span data-ttu-id="3375f-110">Cette méthode retourne une **chaîne**.</span><span class="sxs-lookup"><span data-stu-id="3375f-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3375f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3375f-111">Remarks</span></span>

<span data-ttu-id="3375f-112">Une préférence est une paire clé/valeur qui peut être stockée dans le registre pour conserver les informations sur l’état du lecteur Windows Media entre les exécutions.</span><span class="sxs-lookup"><span data-stu-id="3375f-112">A preference is a key/value pair that can be stored in the registry to retain information about the state of the Windows Media Player between runs.</span></span> <span data-ttu-id="3375f-113">Cette fonctionnalité peut être utilisée, par exemple, pour enregistrer les paramètres de personnalisation afin qu’ils n’aient pas à entrer à nouveau chaque fois que le lecteur Windows Media est démarré.</span><span class="sxs-lookup"><span data-stu-id="3375f-113">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="3375f-114">Les préférences ne sont pas chiffrées et ne sont donc pas une méthode sécurisée pour la persistance des données.</span><span class="sxs-lookup"><span data-stu-id="3375f-114">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="3375f-115">N’utilisez pas de préférences pour stocker des données privées.</span><span class="sxs-lookup"><span data-stu-id="3375f-115">Do not use preferences to store private data.</span></span>

## <a name="requirements"></a><span data-ttu-id="3375f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3375f-116">Requirements</span></span>



| <span data-ttu-id="3375f-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3375f-117">Requirement</span></span> | <span data-ttu-id="3375f-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3375f-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3375f-119">Version</span><span class="sxs-lookup"><span data-stu-id="3375f-119">Version</span></span><br/> | <span data-ttu-id="3375f-120">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="3375f-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3375f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3375f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3375f-122">**Élément THEMe**</span><span class="sxs-lookup"><span data-stu-id="3375f-122">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="3375f-123">**THÈME. savePreference**</span><span class="sxs-lookup"><span data-stu-id="3375f-123">**THEME.savePreference**</span></span>](theme-savepreference.md)
</dt> </dl>

 

 





