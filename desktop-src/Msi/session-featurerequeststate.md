---
description: La propriété FeatureRequestState est une propriété en lecture-écriture de l’objet session.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Session. FeatureRequestState, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542350"
---
# <a name="sessionfeaturerequeststate-property"></a><span data-ttu-id="8391b-103">Session. FeatureRequestState, propriété</span><span class="sxs-lookup"><span data-stu-id="8391b-103">Session.FeatureRequestState property</span></span>

<span data-ttu-id="8391b-104">La propriété **FeatureRequestState** est une propriété en lecture-écriture de l’objet [**session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="8391b-104">The **FeatureRequestState** property is a read-write property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="8391b-105">Il peut être utilisé pour obtenir l’état d’action actuel d’une fonctionnalité ou pour demander une modification de l’action d’une fonctionnalité et de ses sous-composants.</span><span class="sxs-lookup"><span data-stu-id="8391b-105">It can be used to obtain the current action state of a feature or to request a change in the action of a feature and its subfeatures.</span></span> <span data-ttu-id="8391b-106">La fonctionnalité doit être nommée dans le tableau des [fonctionnalités](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="8391b-106">The feature must be named in the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="8391b-107">Si une modification de l’état d’action d’une fonctionnalité est demandée, l’état d’action de tous les composants de la fonctionnalité modifiée peut également être modifié.</span><span class="sxs-lookup"><span data-stu-id="8391b-107">If a change to the action state of a feature is requested, the action state of all components of the changed feature may be changed as well.</span></span> <span data-ttu-id="8391b-108">L’état d’action des composants partagés par plusieurs fonctionnalités sera modifié en fonction du nouvel état de l’action de fonctionnalité (consultez la section Notes).</span><span class="sxs-lookup"><span data-stu-id="8391b-108">The action state of components shared by more than one feature will be changed as appropriate based on the new feature action state (see Remarks).</span></span> <span data-ttu-id="8391b-109">La propriété **FeatureRequestState** peut également être utilisée pour configurer toutes les fonctionnalités à la fois en spécifiant le mot clé All à la place d’un nom de fonctionnalité spécifique.</span><span class="sxs-lookup"><span data-stu-id="8391b-109">The **FeatureRequestState** property can also be used to configure all features at once by specifying the keyword ALL instead of a specific feature name.</span></span>

<span data-ttu-id="8391b-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8391b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8391b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8391b-111">Syntax</span></span>


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a><span data-ttu-id="8391b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8391b-112">Property value</span></span>

<span data-ttu-id="8391b-113">Chaîne obligatoire qui spécifie le nom de la fonctionnalité à configurer.</span><span class="sxs-lookup"><span data-stu-id="8391b-113">Required string that specifies the name of the feature to be configured.</span></span> <span data-ttu-id="8391b-114">Pour définir l’état de la demande de toutes les fonctionnalités, utilisez le mot réservé ne respectant pas la casse : ALL.</span><span class="sxs-lookup"><span data-stu-id="8391b-114">To set all features to a desired request state, use the reserved case-insensitive word: ALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8391b-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8391b-115">Remarks</span></span>

<span data-ttu-id="8391b-116">La méthode [**SetInstallLevel**](session-setinstalllevel.md) doit être appelée avant d’appeler **FeatureRequestState**.</span><span class="sxs-lookup"><span data-stu-id="8391b-116">The [**SetInstallLevel**](session-setinstalllevel.md) method must be called before calling **FeatureRequestState**.</span></span>

<span data-ttu-id="8391b-117">Si l’état actuel de la fonctionnalité est demandé, la propriété **FeatureRequestState** retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8391b-117">If the current state of the feature is being requested, the **FeatureRequestState** property returns one of the following values.</span></span>



| <span data-ttu-id="8391b-118">Nom de l’état de sélection</span><span class="sxs-lookup"><span data-stu-id="8391b-118">Selection state name</span></span>         | <span data-ttu-id="8391b-119">Signification</span><span class="sxs-lookup"><span data-stu-id="8391b-119">Meaning</span></span>                                                               |
|------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8391b-120">msiInstallStateUnknown =-1</span><span class="sxs-lookup"><span data-stu-id="8391b-120">msiInstallStateUnknown = -1</span></span>  | <span data-ttu-id="8391b-121">Aucune action n’est effectuée pour la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8391b-121">No action is taken for the feature.</span></span> <span data-ttu-id="8391b-122">Cela équivaut à la valeur null.</span><span class="sxs-lookup"><span data-stu-id="8391b-122">This is equivalent to null.</span></span>       |
| <span data-ttu-id="8391b-123">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="8391b-123">msiInstallStateAdvertised =1</span></span> | <span data-ttu-id="8391b-124">La fonctionnalité doit être publiée.</span><span class="sxs-lookup"><span data-stu-id="8391b-124">Feature is to be advertised.</span></span>                                          |
| <span data-ttu-id="8391b-125">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="8391b-125">msiInstallStateAbsent = 2</span></span>    | <span data-ttu-id="8391b-126">La fonctionnalité doit être supprimée.</span><span class="sxs-lookup"><span data-stu-id="8391b-126">Feature is to be removed.</span></span>                                             |
| <span data-ttu-id="8391b-127">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="8391b-127">msiInstallStateLocal = 3</span></span>     | <span data-ttu-id="8391b-128">La fonctionnalité doit être installée en tant qu’exécution locale.</span><span class="sxs-lookup"><span data-stu-id="8391b-128">Feature is to be installed as run-local.</span></span>                              |
| <span data-ttu-id="8391b-129">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="8391b-129">msiInstallStateSource = 4</span></span>    | <span data-ttu-id="8391b-130">La fonctionnalité doit être installée en tant qu’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="8391b-130">Feature is to be installed as run-from-source.</span></span>                        |
| <span data-ttu-id="8391b-131">msiInstallStateDefault = 5</span><span class="sxs-lookup"><span data-stu-id="8391b-131">msiInstallStateDefault = 5</span></span>   | <span data-ttu-id="8391b-132">La fonctionnalité doit être réinstallée avec l’état d’action actuel de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8391b-132">Feature is to be reinstalled with the feature's current action state.</span></span> |



 

<span data-ttu-id="8391b-133">Par exemple, le code suivant obtient l’état actuel de « MyFeature » à partir d’une action personnalisée VBScript.</span><span class="sxs-lookup"><span data-stu-id="8391b-133">For example, the following obtains the current state of "MyFeature" from a VBScript custom action.</span></span>


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



<span data-ttu-id="8391b-134">Si l’état de la fonctionnalité est configuré, la propriété **FeatureRequestState** doit être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8391b-134">If the state of the feature is being configured, the **FeatureRequestState** property should be set to one of the following values.</span></span>



| <span data-ttu-id="8391b-135">Nom de l’état de sélection</span><span class="sxs-lookup"><span data-stu-id="8391b-135">Selection state name</span></span>          | <span data-ttu-id="8391b-136">Signification</span><span class="sxs-lookup"><span data-stu-id="8391b-136">Meaning</span></span>                                 |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="8391b-137">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="8391b-137">msiInstallStateAdvertised = 1</span></span> | <span data-ttu-id="8391b-138">Publiez la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8391b-138">Advertise the feature.</span></span>                  |
| <span data-ttu-id="8391b-139">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="8391b-139">msiInstallStateAbsent = 2</span></span>     | <span data-ttu-id="8391b-140">Supprimez la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8391b-140">Remove the feature.</span></span>                     |
| <span data-ttu-id="8391b-141">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="8391b-141">msiInstallStateLocal = 3</span></span>      | <span data-ttu-id="8391b-142">Installez la fonctionnalité en tant qu’exécution locale.</span><span class="sxs-lookup"><span data-stu-id="8391b-142">Install the feature as run-local.</span></span>       |
| <span data-ttu-id="8391b-143">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="8391b-143">msiInstallStateSource = 4</span></span>     | <span data-ttu-id="8391b-144">Installez la fonctionnalité en tant qu’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="8391b-144">Install the feature as run-from-source.</span></span> |



 

<span data-ttu-id="8391b-145">Par exemple, les requêtes suivantes d’une action personnalisée VBScript que « MyFeature » sont installées pour s’exécuter localement sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8391b-145">For example, the following requests from a VBScript custom action that "MyFeature" be installed to run locally on the computer.</span></span>


```VB
Session.FeatureRequestState("MyFeature")=3
```



<span data-ttu-id="8391b-146">Quand **FeatureRequestState** est appelé, le programme d’installation tente de définir l’état d’action de chaque composant lié à la fonctionnalité spécifiée à l’état spécifié, le plus possible.</span><span class="sxs-lookup"><span data-stu-id="8391b-146">When **FeatureRequestState** is called, the installer attempts to set the action state of each component tied to the specified feature to the specified state, as best as possible.</span></span> <span data-ttu-id="8391b-147">Toutefois, il existe des situations courantes dans lesquelles la demande ne peut pas être entièrement honorée.</span><span class="sxs-lookup"><span data-stu-id="8391b-147">However, there are common situations when the request cannot be fully honored.</span></span> <span data-ttu-id="8391b-148">Par exemple, si une fonctionnalité est liée à deux composants, le composant A et le composant B, via la table [FeatureComponents](featurecomponents-table.md) et le composant a, l’attribut **msidbComponentAttributesLocalOnly** et le composant b ont l’attribut **msidbComponentAttributesSourceOnly** .</span><span class="sxs-lookup"><span data-stu-id="8391b-148">For example, if a feature is tied to two components, Component A and Component B, through the [FeatureComponents](featurecomponents-table.md) table and Component A has the **msidbComponentAttributesLocalOnly** attribute and component B has the **msidbComponentAttributesSourceOnly** attribute.</span></span> <span data-ttu-id="8391b-149">Dans ce cas, si **FeatureRequestState** est appelé avec l’État demandé MsiInstallStateLocal ou msiInstallStateSource, la requête ne peut pas être honorée pour les deux composants.</span><span class="sxs-lookup"><span data-stu-id="8391b-149">In this case, if **FeatureRequestState** is called with a requested state of either msiInstallStateLocal or msiInstallStateSource, the request cannot be honored for both components.</span></span> <span data-ttu-id="8391b-150">Dans ce cas, les deux composants peuvent être activés avec le composant A défini sur msiInstallStateLocal et le composant B défini sur msiInstallStateSource.</span><span class="sxs-lookup"><span data-stu-id="8391b-150">In this case, both components can be turned on with Component A set to msiInstallStateLocal and Component B set to msiInstallStateSource.</span></span>

<span data-ttu-id="8391b-151">Si plusieurs fonctionnalités sont liées à un seul composant, l’état d’action final de ce composant est déterminé comme suit : si au moins une fonctionnalité exige que le composant soit installé localement, il est installé msiInstallStateLocal.</span><span class="sxs-lookup"><span data-stu-id="8391b-151">If more than one feature is linked to a single component, the final action state of that component is determined as follows: If at least one feature calls for the component to be installed locally, it is installed msiInstallStateLocal.</span></span> <span data-ttu-id="8391b-152">Si au moins une fonctionnalité exige que le composant soit exécuté à partir du média source, il est installé msiInstallStateSource.</span><span class="sxs-lookup"><span data-stu-id="8391b-152">If at least one feature calls for the component to be run from the source media, it is installed msiInstallStateSource.</span></span> <span data-ttu-id="8391b-153">Si au moins une fonctionnalité appelle pour la suppression du composant, l’état d’action est msiInstallStateAbsent.</span><span class="sxs-lookup"><span data-stu-id="8391b-153">If at least one feature calls for the removal of the component, the action state is msiInstallStateAbsent.</span></span> <span data-ttu-id="8391b-154">Pour plus d’informations sur la sélection des fonctionnalités pour l’installation, [consultez le tableau des fonctionnalités.](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="8391b-154">For more information on how features are selected for installation, see the [Feature](feature-table.md) table.</span></span>

<span data-ttu-id="8391b-155">Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="8391b-155">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8391b-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8391b-156">Requirements</span></span>



| <span data-ttu-id="8391b-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8391b-157">Requirement</span></span> | <span data-ttu-id="8391b-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="8391b-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8391b-159">Version</span><span class="sxs-lookup"><span data-stu-id="8391b-159">Version</span></span><br/> | <span data-ttu-id="8391b-160">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8391b-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8391b-161">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8391b-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8391b-162">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="8391b-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8391b-163">DLL</span><span class="sxs-lookup"><span data-stu-id="8391b-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="8391b-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8391b-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8391b-165">IID</span><span class="sxs-lookup"><span data-stu-id="8391b-165">IID</span></span><br/>     | <span data-ttu-id="8391b-166">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8391b-166">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="8391b-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8391b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8391b-168">**session**</span><span class="sxs-lookup"><span data-stu-id="8391b-168">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="8391b-169">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="8391b-169">Feature</span></span>](feature-table.md)
</dt> </dl>

 

 




