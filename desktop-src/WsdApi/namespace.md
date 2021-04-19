---
description: Décrit un espace de noms.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2414919f699bb60c2cf1e48bc52030c36cf67a0
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380843"
---
# <a name="namespace-element"></a><span data-ttu-id="4cae4-103">nameSpace, élément</span><span class="sxs-lookup"><span data-stu-id="4cae4-103">nameSpace element</span></span>

<span data-ttu-id="4cae4-104">Décrit un espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4cae4-104">Describes a namespace.</span></span> <span data-ttu-id="4cae4-105">Cet espace de noms peut être utilisé pour la génération de code ou pour la gestion de \<wsdl:import> directives.</span><span class="sxs-lookup"><span data-stu-id="4cae4-105">This namespace may be used for code generation or for handling \<wsdl:import> directives.</span></span>

## <a name="usage"></a><span data-ttu-id="4cae4-106">Usage</span><span class="sxs-lookup"><span data-stu-id="4cae4-106">Usage</span></span>

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a><span data-ttu-id="4cae4-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="4cae4-107">Attributes</span></span>



| <span data-ttu-id="4cae4-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="4cae4-108">Attribute</span></span>          | <span data-ttu-id="4cae4-109">Type</span><span class="sxs-lookup"><span data-stu-id="4cae4-109">Type</span></span>                         | <span data-ttu-id="4cae4-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4cae4-110">Required</span></span>       | <span data-ttu-id="4cae4-111">Description</span><span class="sxs-lookup"><span data-stu-id="4cae4-111">Description</span></span>                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="4cae4-112">**uri**</span><span class="sxs-lookup"><span data-stu-id="4cae4-112">**uri**</span></span><br/> | <span data-ttu-id="4cae4-113">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="4cae4-113">character\_string</span></span><br/> | <span data-ttu-id="4cae4-114">Oui</span><span class="sxs-lookup"><span data-stu-id="4cae4-114">Yes</span></span><br/> | <span data-ttu-id="4cae4-115">URI unique de l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4cae4-115">The unique URI of the namespace.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="4cae4-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4cae4-116">Child elements</span></span>



| <span data-ttu-id="4cae4-117">Élément</span><span class="sxs-lookup"><span data-stu-id="4cae4-117">Element</span></span>                                               | <span data-ttu-id="4cae4-118">Description</span><span class="sxs-lookup"><span data-stu-id="4cae4-118">Description</span></span>                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cae4-119">**Baptisé**</span><span class="sxs-lookup"><span data-stu-id="4cae4-119">**codeName**</span></span>](codename.md)<br/>               | <span data-ttu-id="4cae4-120">Nom à utiliser pour identifier l’espace de noms dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="4cae4-120">The name to be used to identify the namespace in generated code.</span></span><br/> <br/>                  |
| [<span data-ttu-id="4cae4-121">**macroPrefix**</span><span class="sxs-lookup"><span data-stu-id="4cae4-121">**macroPrefix**</span></span>](macroprefix.md)<br/>         | <span data-ttu-id="4cae4-122">Préfixe à utiliser dans le code généré pour les noms de macros dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4cae4-122">The prefix to be used in the generated code for names of macros in the namespace.</span></span><br/> <br/> |
| [<span data-ttu-id="4cae4-123">**nomme**</span><span class="sxs-lookup"><span data-stu-id="4cae4-123">**name**</span></span>](name.md)<br/>                       | <span data-ttu-id="4cae4-124">Nom qualifié dans l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="4cae4-124">A qualified name in the namespace.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="4cae4-125">**preferredPrefix**</span><span class="sxs-lookup"><span data-stu-id="4cae4-125">**preferredPrefix**</span></span>](preferredprefix.md)<br/> | <span data-ttu-id="4cae4-126">Préfixe auquel l’espace de noms doit être mappé pour rendre le XML plus lisible.</span><span class="sxs-lookup"><span data-stu-id="4cae4-126">The prefix to which the namespace should be mapped to make the XML more readable.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="4cae4-127">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4cae4-127">Child element sequence</span></span>

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a><span data-ttu-id="4cae4-128">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4cae4-128">Parent elements</span></span>



| <span data-ttu-id="4cae4-129">Élément</span><span class="sxs-lookup"><span data-stu-id="4cae4-129">Element</span></span>                                     | <span data-ttu-id="4cae4-130">Description</span><span class="sxs-lookup"><span data-stu-id="4cae4-130">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cae4-131">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="4cae4-131">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="4cae4-132">Élément racine d’un fichier de script XML du générateur de code WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="4cae4-132">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="4cae4-133">Notes</span><span class="sxs-lookup"><span data-stu-id="4cae4-133">Remarks</span></span>

<span data-ttu-id="4cae4-134">Cet élément peut être utilisé pour fournir le générateur de code avec des informations supplémentaires sur les espaces de noms qu’il rencontre dans les fichiers WSDL et XSD ou pour introduire de nouveaux espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="4cae4-134">This element may be used to provide the code generator with additional information about namespaces that it encounters in WSDL and XSD files or to introduce new namespaces.</span></span>

<span data-ttu-id="4cae4-135">Les espaces de noms implicites par la réflexion de type ou spécifiés dans les fichiers WSDL et XSD sont analysés automatiquement par le générateur de code et n’ont pas besoin d’être explicitement définis dans le script.</span><span class="sxs-lookup"><span data-stu-id="4cae4-135">Namespaces implied by type reflection or specified in WSDL and XSD files are parsed automatically by the code generator and do not have to be explicitly defined in the script.</span></span> <span data-ttu-id="4cae4-136">Dans certains cas, cet élément peut être utilisé pour ajouter des propriétés ou des noms supplémentaires à un espace de noms référencé par la réflexion de type ou WSDL/XSD.</span><span class="sxs-lookup"><span data-stu-id="4cae4-136">In some cases, this element can be used to add additional properties or names to a namespace that is referenced by type reflection or WSDL/XSD.</span></span> <span data-ttu-id="4cae4-137">Le générateur de code ne considère pas ceci comme un conflit.</span><span class="sxs-lookup"><span data-stu-id="4cae4-137">The code generator does not regard this as a conflict.</span></span>

<span data-ttu-id="4cae4-138">Le code XML suivant montre un élément d’espace de noms (avec des enfants omis par souci de concision).</span><span class="sxs-lookup"><span data-stu-id="4cae4-138">The following XML shows a nameSpace element (with children omitted for brevity).</span></span>

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a><span data-ttu-id="4cae4-139">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4cae4-139">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="4cae4-140">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cae4-140">Minimum supported system</span></span><br/> | <span data-ttu-id="4cae4-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4cae4-141">Windows Vista</span></span> |
| <span data-ttu-id="4cae4-142">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="4cae4-142">Can be empty</span></span>                        | <span data-ttu-id="4cae4-143">Oui</span><span class="sxs-lookup"><span data-stu-id="4cae4-143">Yes</span></span>           |



 

 




