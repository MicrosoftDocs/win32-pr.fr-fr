---
description: La méthode EvaluateCondition de l’objet session évalue une expression logique qui contient des symboles et des valeurs. Cette méthode utilise la fonction MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Session. EvaluateCondition, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520973"
---
# <a name="sessionevaluatecondition-method"></a><span data-ttu-id="1d422-104">Session. EvaluateCondition, méthode</span><span class="sxs-lookup"><span data-stu-id="1d422-104">Session.EvaluateCondition method</span></span>

<span data-ttu-id="1d422-105">La méthode **EvaluateCondition** de l’objet [**session**](session-object.md) évalue une expression logique qui contient des symboles et des valeurs.</span><span class="sxs-lookup"><span data-stu-id="1d422-105">The **EvaluateCondition** method of the [**Session**](session-object.md) object evaluates a logical expression that contains symbols and values.</span></span> <span data-ttu-id="1d422-106">Cette méthode utilise la fonction [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="1d422-106">This method uses the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d422-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d422-107">Syntax</span></span>


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a><span data-ttu-id="1d422-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d422-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d422-109">*condition*</span><span class="sxs-lookup"><span data-stu-id="1d422-109">*condition*</span></span> 
</dt> <dd>

<span data-ttu-id="1d422-110">Chaîne obligatoire qui contient l’expression logique.</span><span class="sxs-lookup"><span data-stu-id="1d422-110">Required string that contains the logical expression.</span></span> <span data-ttu-id="1d422-111">Pour plus d’informations, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="1d422-111">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d422-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d422-112">Return value</span></span>

<span data-ttu-id="1d422-113">Cette méthode retourne un entier qui indique l’évaluation de la condition.</span><span class="sxs-lookup"><span data-stu-id="1d422-113">This method returns an integer that indicates the evaluation of the condition.</span></span>



| <span data-ttu-id="1d422-114">Constante</span><span class="sxs-lookup"><span data-stu-id="1d422-114">Constant</span></span>                  | <span data-ttu-id="1d422-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d422-115">Value</span></span> | <span data-ttu-id="1d422-116">Description</span><span class="sxs-lookup"><span data-stu-id="1d422-116">Description</span></span>                               |
|---------------------------|-------|-------------------------------------------|
| <span data-ttu-id="1d422-117">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="1d422-117">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="1d422-118">0</span><span class="sxs-lookup"><span data-stu-id="1d422-118">0</span></span>     | <span data-ttu-id="1d422-119">La condition prend la valeur false.</span><span class="sxs-lookup"><span data-stu-id="1d422-119">The condition evaluates to false.</span></span>         |
| <span data-ttu-id="1d422-120">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="1d422-120">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="1d422-121">1</span><span class="sxs-lookup"><span data-stu-id="1d422-121">1</span></span>     | <span data-ttu-id="1d422-122">La condition prend la valeur true.</span><span class="sxs-lookup"><span data-stu-id="1d422-122">The condition evaluates to true.</span></span>          |
| <span data-ttu-id="1d422-123">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="1d422-123">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="1d422-124">2</span><span class="sxs-lookup"><span data-stu-id="1d422-124">2</span></span>     | <span data-ttu-id="1d422-125">Une expression conditionnelle n’est pas fournie.</span><span class="sxs-lookup"><span data-stu-id="1d422-125">A conditional expression is not provided.</span></span> |
| <span data-ttu-id="1d422-126">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="1d422-126">msiEvaluateConditionError</span></span> | <span data-ttu-id="1d422-127">3</span><span class="sxs-lookup"><span data-stu-id="1d422-127">3</span></span>     | <span data-ttu-id="1d422-128">La condition contient une erreur de syntaxe.</span><span class="sxs-lookup"><span data-stu-id="1d422-128">The condition contains a syntax error.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="1d422-129">Notes</span><span class="sxs-lookup"><span data-stu-id="1d422-129">Remarks</span></span>

<span data-ttu-id="1d422-130">Les expressions conditionnelles peuvent être utilisées pour comparer les États des fonctionnalités et des composants.</span><span class="sxs-lookup"><span data-stu-id="1d422-130">Conditional expressions can be used to compare feature and component states.</span></span> <span data-ttu-id="1d422-131">Le tableau suivant présente les États des fonctionnalités et des composants utilisés par la méthode EvaluateCondition.</span><span class="sxs-lookup"><span data-stu-id="1d422-131">The following table shows the feature and component states that the EvaluateCondition method uses.</span></span>



| <span data-ttu-id="1d422-132">State</span><span class="sxs-lookup"><span data-stu-id="1d422-132">State</span></span>                 | <span data-ttu-id="1d422-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d422-133">Value</span></span> | <span data-ttu-id="1d422-134">Description</span><span class="sxs-lookup"><span data-stu-id="1d422-134">Description</span></span>                                              |
|-----------------------|-------|----------------------------------------------------------|
| <span data-ttu-id="1d422-135">Null</span><span class="sxs-lookup"><span data-stu-id="1d422-135">Null</span></span>                  | <span data-ttu-id="1d422-136">Null</span><span class="sxs-lookup"><span data-stu-id="1d422-136">Null</span></span>  | <span data-ttu-id="1d422-137">Aucune action effectuée sur la fonctionnalité ou le composant.</span><span class="sxs-lookup"><span data-stu-id="1d422-137">No action taken on feature or component.</span></span>                 |
| <span data-ttu-id="1d422-138">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="1d422-138">msiInstallStateAbsent</span></span> | <span data-ttu-id="1d422-139">2</span><span class="sxs-lookup"><span data-stu-id="1d422-139">2</span></span>     | <span data-ttu-id="1d422-140">La fonctionnalité ou le composant n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="1d422-140">Feature or component is not present.</span></span>                     |
| <span data-ttu-id="1d422-141">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="1d422-141">msiInstallStateLocal</span></span>  | <span data-ttu-id="1d422-142">3</span><span class="sxs-lookup"><span data-stu-id="1d422-142">3</span></span>     | <span data-ttu-id="1d422-143">La fonctionnalité ou le composant est installé sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="1d422-143">Feature or component is installed on the local computer.</span></span> |
| <span data-ttu-id="1d422-144">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="1d422-144">msiInstallStateSource</span></span> | <span data-ttu-id="1d422-145">4</span><span class="sxs-lookup"><span data-stu-id="1d422-145">4</span></span>     | <span data-ttu-id="1d422-146">La fonctionnalité ou le composant est installé pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="1d422-146">Feature or component is installed to run from source.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="1d422-147">Les États ne sont pas définis tant que la méthode [**SetInstallLevel**](session-setinstalllevel.md) n’est pas appelée, soit directement, soit par l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="1d422-147">The states are not set until the [**SetInstallLevel**](session-setinstalllevel.md) method is called, either directly or by the [CostFinalize Action](costfinalize-action.md).</span></span> <span data-ttu-id="1d422-148">Par conséquent, la vérification de l’État n’est utile que dans une expression conditionnelle dans une table de séquences d’actions.</span><span class="sxs-lookup"><span data-stu-id="1d422-148">Therefore, state checking is only useful in conditional expression in an action sequence table.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1d422-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d422-149">Requirements</span></span>



| <span data-ttu-id="1d422-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d422-150">Requirement</span></span> | <span data-ttu-id="1d422-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d422-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d422-152">Version</span><span class="sxs-lookup"><span data-stu-id="1d422-152">Version</span></span><br/> | <span data-ttu-id="1d422-153">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1d422-153">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1d422-154">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1d422-154">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1d422-155">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="1d422-155">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="1d422-156">DLL</span><span class="sxs-lookup"><span data-stu-id="1d422-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="1d422-157"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d422-157"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="1d422-158">IID</span><span class="sxs-lookup"><span data-stu-id="1d422-158">IID</span></span><br/>     | <span data-ttu-id="1d422-159">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1d422-159">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="1d422-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d422-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d422-161">Syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="1d422-161">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 




