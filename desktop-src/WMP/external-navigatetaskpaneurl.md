---
title: External. NavigateTaskPaneURL, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. NavigateTaskPaneURL, méthode
ms.assetid: c3a888c0-6589-4d21-9d47-37372d9069f4
keywords:
- Méthode NavigateTaskPaneURL lecteur Windows Media
- Méthode NavigateTaskPaneURL lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode NavigateTaskPaneURL
topic_type:
- apiref
api_name:
- External.NavigateTaskPaneURL
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e70558c7616738f67d9dc1d6d29eca15e5c30d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528381"
---
# <a name="externalnavigatetaskpaneurl-method"></a><span data-ttu-id="f7fdc-107">External. NavigateTaskPaneURL, méthode</span><span class="sxs-lookup"><span data-stu-id="f7fdc-107">External.NavigateTaskPaneURL method</span></span>

> [!Note]  
> <span data-ttu-id="f7fdc-108">Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="f7fdc-109">L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="f7fdc-110">La méthode **NavigateTaskPaneURL** ouvre une page Web dans le volet de tâches spécifié et active le volet spécifié.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-110">The **NavigateTaskPaneURL** method opens a webpage in the specified task pane, and changes focus to the specified pane.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7fdc-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7fdc-111">Syntax</span></span>


```JScript
External.NavigateTaskPaneURL(
  bstrKeyName,
  bstrTaskPane,
  bstrParams
)
```



## <a name="parameters"></a><span data-ttu-id="f7fdc-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7fdc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7fdc-113">*bstrKeyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7fdc-113">*bstrKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7fdc-114">**Chaîne** contenant le nom de clé du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-114">**String** containing the key name for the online store.</span></span> <span data-ttu-id="f7fdc-115">(obligatoire)</span><span class="sxs-lookup"><span data-stu-id="f7fdc-115">(required)</span></span>

</dd> <dt>

<span data-ttu-id="f7fdc-116">*bstrTaskPane* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7fdc-116">*bstrTaskPane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7fdc-117">**Chaîne** contenant le nom du volet de tâches dans lequel la page Web s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-117">**String** containing the name of the task pane in which the webpage opens.</span></span> <span data-ttu-id="f7fdc-118">(obligatoire)</span><span class="sxs-lookup"><span data-stu-id="f7fdc-118">(required)</span></span>

</dd> <dt>

<span data-ttu-id="f7fdc-119">*bstrParams* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7fdc-119">*bstrParams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7fdc-120">**Chaîne** contenant les paramètres de chaîne de requête à ajouter à l’URL spécifiée par l’élément **Navigate** du document serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-120">**String** containing the query string parameters to append to the URL specified by the **Navigate** element of the ServiceInfo document.</span></span> <span data-ttu-id="f7fdc-121">(facultatif)</span><span class="sxs-lookup"><span data-stu-id="f7fdc-121">(optional)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7fdc-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7fdc-122">Return value</span></span>

<span data-ttu-id="f7fdc-123">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7fdc-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f7fdc-124">Remarks</span></span>

<span data-ttu-id="f7fdc-125">La navigation vers un volet que votre magasin en ligne ne prend pas en charge peut entraîner la modification du magasin en ligne actuel.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-125">Navigating to a pane that your online store does not support may cause the current online store to change.</span></span>

<span data-ttu-id="f7fdc-126">La valeur spécifiée pour *bstrParams* est valide uniquement lorsque **NavigateTaskPaneURL** est appelé à partir de pages Web fournies par le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-126">The value specified for *bstrParams* is valid only when **NavigateTaskPaneURL** is called from webpages provided by the online store.</span></span>

<span data-ttu-id="f7fdc-127">Le tableau suivant répertorie les valeurs valides pour *bstrTaskPane* et le volet de tâches associé pour chacun d’entre eux.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-127">The following table lists of valid values for *bstrTaskPane* and the associated task pane for each.</span></span>



| <span data-ttu-id="f7fdc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7fdc-128">Value</span></span>            | <span data-ttu-id="f7fdc-129">Volet des tâches</span><span class="sxs-lookup"><span data-stu-id="f7fdc-129">Task Pane</span></span>                      |
|------------------|--------------------------------|
| <span data-ttu-id="f7fdc-130">**ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-130">**ServiceTask1**</span></span> | <span data-ttu-id="f7fdc-131">Premier volet de tâches du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-131">First online store task pane.</span></span>  |
| <span data-ttu-id="f7fdc-132">**ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-132">**ServiceTask2**</span></span> | <span data-ttu-id="f7fdc-133">Deuxième volet des tâches du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-133">Second online store task pane.</span></span> |
| <span data-ttu-id="f7fdc-134">**ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-134">**ServiceTask3**</span></span> | <span data-ttu-id="f7fdc-135">Troisième volet des tâches de la boutique en ligne.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-135">Third online store task pane.</span></span>  |



 

<span data-ttu-id="f7fdc-136">Votre code de page Web doit spécifier une valeur pour [External. SelectedTaskPane](external-selectedtaskpane.md) lors du chargement pour garantir que le bouton de volet de tâches correct est mis en surbrillance une fois la navigation terminée.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-136">Your webpage code should specify a value for [External.SelectedTaskPane](external-selectedtaskpane.md) when loading to ensure that the correct task pane button is highlighted after navigation is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="f7fdc-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="f7fdc-137">Examples</span></span>

<span data-ttu-id="f7fdc-138">L’exemple de code suivant montre comment **NavigateTaskPaneURL** crée l’URL de la page Web à afficher pour **ServiceTask1**.</span><span class="sxs-lookup"><span data-stu-id="f7fdc-138">The following example code shows how **NavigateTaskPaneURL** creates the URL of the webpage to display for **ServiceTask1**.</span></span>

<span data-ttu-id="f7fdc-139">Exemple de l’élément **Navigate** :</span><span class="sxs-lookup"><span data-stu-id="f7fdc-139">Example of the **Navigate** element:</span></span>


```XML
<Navigate
    BaseURL = "https://www.proseware.com/online store/html/navigate.asp">
</Navigate>
```



<span data-ttu-id="f7fdc-140">Exemple d’appel à la méthode **NavigateTaskPaneURL** :</span><span class="sxs-lookup"><span data-stu-id="f7fdc-140">Example call to the **NavigateTaskPaneURL** method:</span></span>


```XML
external.NavigateTaskPaneURL("Proseware", "ServiceTask1", "Pane=Store");
```



<span data-ttu-id="f7fdc-141">Exemple d’URL résultante utilisée pour la page Web affichée dans **ServiceTask1**:</span><span class="sxs-lookup"><span data-stu-id="f7fdc-141">Example of resulting URL used for the webpage displayed in **ServiceTask1**:</span></span>


```XML
https://www.proseware.com/online store/html/navigate.asp?Pane=Store
```



## <a name="requirements"></a><span data-ttu-id="f7fdc-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7fdc-142">Requirements</span></span>



| <span data-ttu-id="f7fdc-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7fdc-143">Requirement</span></span> | <span data-ttu-id="f7fdc-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7fdc-144">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f7fdc-145">Version</span><span class="sxs-lookup"><span data-stu-id="f7fdc-145">Version</span></span><br/> | <span data-ttu-id="f7fdc-146">Lecteur Windows Media 10 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f7fdc-146">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="f7fdc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="f7fdc-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="f7fdc-148"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7fdc-148"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7fdc-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7fdc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7fdc-150">**Objet externe pour les magasins de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-150">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f7fdc-151">**External. SelectedTaskPane**</span><span class="sxs-lookup"><span data-stu-id="f7fdc-151">**External.SelectedTaskPane**</span></span>](external-selectedtaskpane.md)
</dt> </dl>

 

 





