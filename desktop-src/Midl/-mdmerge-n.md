---
title: commutateur/n
description: Le commutateur/n spécifie la profondeur de composition pour la composition des fichiers de métadonnées.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n Switch MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541468"
---
# <a name="n-switch"></a><span data-ttu-id="39ad2-104">commutateur/n</span><span class="sxs-lookup"><span data-stu-id="39ad2-104">/n switch</span></span>

<span data-ttu-id="39ad2-105">Le commutateur **/n** spécifie la profondeur de composition pour la composition des fichiers de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="39ad2-105">The **/n** switch specifies the composition depth for composing metadata files.</span></span>

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a><span data-ttu-id="39ad2-106">Options de commutateur</span><span class="sxs-lookup"><span data-stu-id="39ad2-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="39ad2-107">*profondeur de l’espace de noms \_*</span><span class="sxs-lookup"><span data-stu-id="39ad2-107">*namespace\_depth*</span></span> 
</dt> <dd>

<span data-ttu-id="39ad2-108">Spécifie la profondeur de l’espace de noms à composer en un seul fichier de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="39ad2-108">Specifies the namespace depth to compose into a single metadata file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39ad2-109">Notes</span><span class="sxs-lookup"><span data-stu-id="39ad2-109">Remarks</span></span>

<span data-ttu-id="39ad2-110">Voici les formats de valeurs possibles que vous pouvez spécifier avec le commutateur **/n** .</span><span class="sxs-lookup"><span data-stu-id="39ad2-110">Here are the possible value formats that you can specify with the **/n** switch.</span></span>



| <span data-ttu-id="39ad2-111">Format de valeur</span><span class="sxs-lookup"><span data-stu-id="39ad2-111">Value format</span></span>                   | <span data-ttu-id="39ad2-112">Description</span><span class="sxs-lookup"><span data-stu-id="39ad2-112">Description</span></span>                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="39ad2-113">> Int32 0</span><span class="sxs-lookup"><span data-stu-id="39ad2-113">Int32 > 0</span></span>                   | <span data-ttu-id="39ad2-114">Compose tous les types à la profondeur d’espace de noms spécifiée dans le commutateur.</span><span class="sxs-lookup"><span data-stu-id="39ad2-114">Compose all types at the namespace depth specified in the switch.</span></span>               |
| <span data-ttu-id="39ad2-115">-1</span><span class="sxs-lookup"><span data-stu-id="39ad2-115">-1</span></span>                             | <span data-ttu-id="39ad2-116">Composez tous les types dans un fichier IDL par espace de noms.</span><span class="sxs-lookup"><span data-stu-id="39ad2-116">Compose all types into one IDL file per namespace.</span></span>                              |
| <span data-ttu-id="39ad2-117"><namespace>: Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="39ad2-117"><namespace>:Int32 > 0</span></span> | <span data-ttu-id="39ad2-118">Compose tous les types avec l’espace de noms correspondant à la profondeur spécifiée dans le commutateur.</span><span class="sxs-lookup"><span data-stu-id="39ad2-118">Compose all types with matching namespace at the depth specified in the switch.</span></span> |
| <span data-ttu-id="39ad2-119"><namespace>:-1</span><span class="sxs-lookup"><span data-stu-id="39ad2-119"><namespace>:-1</span></span>           | <span data-ttu-id="39ad2-120">Compose tous les types avec l’espace de noms correspondant dans un fichier par espace de noms.</span><span class="sxs-lookup"><span data-stu-id="39ad2-120">Compose all types with matching namespace into one file per namespace.</span></span>          |



 

<span data-ttu-id="39ad2-121">Le tableau suivant présente les résultats de différentes combinaisons du commutateur **/n** qui fonctionnent sur ces espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="39ad2-121">The following table shows the results from different combinations of the **/n** switch working on these namespaces.</span></span>

-   <span data-ttu-id="39ad2-122">Windows. Foundation. Collections. interface iiterable</span><span class="sxs-lookup"><span data-stu-id="39ad2-122">Windows.Foundation.Collections.IIterable</span></span>
-   <span data-ttu-id="39ad2-123">Windows. UI. DirectUI. Controls. Button</span><span class="sxs-lookup"><span data-stu-id="39ad2-123">Windows.UI.DirectUI.Controls.Button</span></span>
-   <span data-ttu-id="39ad2-124">Windows. UI. DirectUI. Controls. ListView</span><span class="sxs-lookup"><span data-stu-id="39ad2-124">Windows.UI.DirectUI.Controls.ListView</span></span>
-   <span data-ttu-id="39ad2-125">Windows. UI. immersif. application. point. Target</span><span class="sxs-lookup"><span data-stu-id="39ad2-125">Windows.UI.Immersive.Application.PlayTo.Target</span></span>
-   <span data-ttu-id="39ad2-126">Windows. Web. Syndication. RSS</span><span class="sxs-lookup"><span data-stu-id="39ad2-126">Windows.Web.Syndication.RSS</span></span>



| <span data-ttu-id="39ad2-127">Commutateurs</span><span class="sxs-lookup"><span data-stu-id="39ad2-127">Switches</span></span>                         | <span data-ttu-id="39ad2-128">Résultats</span><span class="sxs-lookup"><span data-stu-id="39ad2-128">Result</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="39ad2-129">Explication</span><span class="sxs-lookup"><span data-stu-id="39ad2-129">Explanation</span></span>                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39ad2-130">**/n :-1**  / **n :1**</span><span class="sxs-lookup"><span data-stu-id="39ad2-130">**/n:-1** /**n:1**</span></span>               | <span data-ttu-id="39ad2-131">Windows.winmd</span><span class="sxs-lookup"><span data-stu-id="39ad2-131">Windows.winmd</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="39ad2-132">Le dernier commutateur/n remplace tous les commutateurs-n précédents.</span><span class="sxs-lookup"><span data-stu-id="39ad2-132">The last /n switch overrides all previous –n switches.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="39ad2-133">**/n :-1/n : Windows. UI : 2**</span><span class="sxs-lookup"><span data-stu-id="39ad2-133">**/n:-1/n:Windows.UI:2**</span></span>         | <dl> <span data-ttu-id="39ad2-134">Windows. <dt>Foundation. winmd</dt> <dt>Windows. UI. Winmd</dt> <dt>Windows. Web. Syndication. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="39ad2-134"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.winmd</dt> <dt>Windows.Web.Syndication.winmd</dt></span></span> </dl> | <dl> <span data-ttu-id="39ad2-135"><dt>**Windows. Foundation** est toujours composé à – n :2.</dt></span><span class="sxs-lookup"><span data-stu-id="39ad2-135"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="39ad2-136"><dt>Les types **Windows. UI** sont regroupés.</dt></span><span class="sxs-lookup"><span data-stu-id="39ad2-136"><dt>**Windows.UI** types are grouped.</dt></span></span> <span data-ttu-id="39ad2-137"><dt>**Windows. Web. Syndication** est composé dans n :-1.</dt></span><span class="sxs-lookup"><span data-stu-id="39ad2-137"><dt>**Windows.Web.Syndication** is composed at n:-1.</dt></span></span> </dl>       |
| <span data-ttu-id="39ad2-138">**/n : 1/n : Windows. UI. DirectUI : 3**</span><span class="sxs-lookup"><span data-stu-id="39ad2-138">**/n:1/n:Windows.UI.DirectUI:3**</span></span> | <dl> <span data-ttu-id="39ad2-139">Windows. <dt>Foundation. winmd</dt> <dt>Windows. UI. directui. winmd</dt> <dt>Windows. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="39ad2-139"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.DirectUI.winmd </dt> <dt>Windows.winmd</dt></span></span> </dl>       | <dl> <span data-ttu-id="39ad2-140"><dt>**Windows. Foundation** est toujours composé à – n :2.</dt></span><span class="sxs-lookup"><span data-stu-id="39ad2-140"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="39ad2-141"><dt>**Windows. UI. directui** est composé au niveau 3.</dt></span><span class="sxs-lookup"><span data-stu-id="39ad2-141"><dt>**Windows.UI.DirectUI** is composed at level 3.</dt></span></span> <span data-ttu-id="39ad2-142"><dt>Tous les autres types sont composés au niveau 1.</dt></span><span class="sxs-lookup"><span data-stu-id="39ad2-142"><dt>All other types are composed at level 1.</dt></span></span> </dl> |



 

<span data-ttu-id="39ad2-143">Voici les règles de gestion de plusieurs instances du commutateur **/n** .</span><span class="sxs-lookup"><span data-stu-id="39ad2-143">Here are the rules for handling multiple instances of the **/n** switch.</span></span>

-   <span data-ttu-id="39ad2-144">L’instance la plus spécifique est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="39ad2-144">The most specific instance prevails.</span></span> <span data-ttu-id="39ad2-145">Par exemple, si vous spécifiez **– n :A.B.C : 4 – n :A.B : 5**, MDMERGE résout un. b. c. D au niveau 4, car a. b. c est plus spécifique que A.B.</span><span class="sxs-lookup"><span data-stu-id="39ad2-145">For example, if you specify **–n:A.B.C:4–n:A.B:5**, MDMERGE resolves A.B.C.D at level 4, because A.B.C is more specific than A.B.</span></span> <span data-ttu-id="39ad2-146">A. B. E. F se résout à Depth 5, car il correspond à A. B mais pas à A.B.C.</span><span class="sxs-lookup"><span data-stu-id="39ad2-146">A.B.E.F resolves at depth 5, because it matches A.B but not A.B.C.</span></span>
-   <span data-ttu-id="39ad2-147">La dernière instance est en vigueur.</span><span class="sxs-lookup"><span data-stu-id="39ad2-147">The last instance prevails.</span></span> <span data-ttu-id="39ad2-148">Par exemple, si vous spécifiez **– n :5 – n :2**, les types sont composés au niveau 2.</span><span class="sxs-lookup"><span data-stu-id="39ad2-148">For example, if you specify **–n:5–n:2**, the types are composed at level 2.</span></span>
-   <span data-ttu-id="39ad2-149">Ces deux règles s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="39ad2-149">Both of these rules apply.</span></span> <span data-ttu-id="39ad2-150">Si vous spécifiez – n :A.B.C : 4 – n :A.B.C : 1, l’espace de noms A. B. C est composé au niveau 1.</span><span class="sxs-lookup"><span data-stu-id="39ad2-150">If you specify –n:A.B.C:4 –n:A.B.C:1, namespace A.B.C is composed at level 1.</span></span>

## <a name="examples"></a><span data-ttu-id="39ad2-151">Exemples</span><span class="sxs-lookup"><span data-stu-id="39ad2-151">Examples</span></span>

<span data-ttu-id="39ad2-152">**mdmerge.exe-Metadata \_ dir $ ( \_ chemin des métadonnées du SDK \_ )-i $ ( \_ chemin des métadonnées du kit de développement logiciel (SDK \_ ) interne \_ )-o $ (obj \_ Path) \\ $O \\ SystemMetadata-v-n :-1-n :Windows.Foundation : 2**</span><span class="sxs-lookup"><span data-stu-id="39ad2-152">**mdmerge.exe -metadata\_dir $(SDK\_METADATA\_PATH) -i $(INTERNAL\_SDK\_METADATA\_PATH) -o $(OBJ\_PATH)\\$O\\SystemMetadata -v -n:-1 -n:Windows.Foundation:2**</span></span>

## <a name="requirements"></a><span data-ttu-id="39ad2-153">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39ad2-153">Requirements</span></span>



| <span data-ttu-id="39ad2-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39ad2-154">Requirement</span></span> | <span data-ttu-id="39ad2-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="39ad2-155">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="39ad2-156">Client</span><span class="sxs-lookup"><span data-stu-id="39ad2-156">Client</span></span><br/> | <span data-ttu-id="39ad2-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="39ad2-157">Windows 8</span></span><br/>           |
| <span data-ttu-id="39ad2-158">Serveur</span><span class="sxs-lookup"><span data-stu-id="39ad2-158">Server</span></span><br/> | <span data-ttu-id="39ad2-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="39ad2-159">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39ad2-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39ad2-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ad2-161">Syntaxe générale de la ligne de commande MIDL</span><span class="sxs-lookup"><span data-stu-id="39ad2-161">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





