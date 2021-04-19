---
title: THÈME. savePreference
description: La méthode savePreference enregistre une préférence dans le registre.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- THEMe. savePreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529958"
---
# <a name="themesavepreference"></a><span data-ttu-id="ca089-104">THÈME. savePreference</span><span class="sxs-lookup"><span data-stu-id="ca089-104">THEME.savePreference</span></span>

<span data-ttu-id="ca089-105">La méthode **savePreference** enregistre une préférence dans le registre.</span><span class="sxs-lookup"><span data-stu-id="ca089-105">The **savePreference** method saves a preference in the registry.</span></span>

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a><span data-ttu-id="ca089-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca089-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="ca089-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="ca089-108">**Chaîne** spécifiant la clé de la valeur de préférence à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="ca089-108">A **String** specifying the key of the preference value to save.</span></span>

</dd> <dt>

<span data-ttu-id="ca089-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*Valeurreprésentant*</span><span class="sxs-lookup"><span data-stu-id="ca089-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*</span></span>
</dt> <dd>

<span data-ttu-id="ca089-110">**Chaîne** spécifiant la valeur à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="ca089-110">A **String** specifying the value to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca089-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ca089-111">Return Value</span></span>

<span data-ttu-id="ca089-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ca089-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca089-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ca089-113">Remarks</span></span>

<span data-ttu-id="ca089-114">Une préférence est une paire clé/valeur qui peut être stockée dans le registre pour conserver les informations sur l’état du lecteur Windows Media entre les exécutions.</span><span class="sxs-lookup"><span data-stu-id="ca089-114">A preference is a key/value pair that can be stored in the registry to retain information about the state of Windows Media Player between runs.</span></span> <span data-ttu-id="ca089-115">Cette fonctionnalité peut être utilisée, par exemple, pour enregistrer les paramètres de personnalisation afin qu’ils n’aient pas à entrer à nouveau chaque fois que le lecteur Windows Media est démarré.</span><span class="sxs-lookup"><span data-stu-id="ca089-115">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="ca089-116">Les préférences ne sont pas chiffrées et ne sont donc pas une méthode sécurisée pour la persistance des données.</span><span class="sxs-lookup"><span data-stu-id="ca089-116">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="ca089-117">N’utilisez pas de préférences pour stocker des données privées.</span><span class="sxs-lookup"><span data-stu-id="ca089-117">Do not use preferences to store private data.</span></span>

## <a name="examples"></a><span data-ttu-id="ca089-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="ca089-118">Examples</span></span>


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="ca089-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca089-119">Requirements</span></span>



| <span data-ttu-id="ca089-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca089-120">Requirement</span></span> | <span data-ttu-id="ca089-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca089-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ca089-122">Version</span><span class="sxs-lookup"><span data-stu-id="ca089-122">Version</span></span><br/> | <span data-ttu-id="ca089-123">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="ca089-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca089-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca089-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca089-125">**Élément THEMe**</span><span class="sxs-lookup"><span data-stu-id="ca089-125">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="ca089-126">**THÈME. loadPreference**</span><span class="sxs-lookup"><span data-stu-id="ca089-126">**THEME.loadPreference**</span></span>](theme-loadpreference.md)
</dt> </dl>

 

 





