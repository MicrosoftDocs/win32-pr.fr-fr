---
description: Comprend le contenu d’une macro ou d’un fichier dans la sortie générée.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034931"
---
# <a name="include-element"></a><span data-ttu-id="5a174-103">include, élément</span><span class="sxs-lookup"><span data-stu-id="5a174-103">include element</span></span>

<span data-ttu-id="5a174-104">Comprend le contenu d’une macro ou d’un fichier dans la sortie générée.</span><span class="sxs-lookup"><span data-stu-id="5a174-104">Includes the contents of a macro or file in the generated output.</span></span>

## <a name="usage"></a><span data-ttu-id="5a174-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="5a174-105">Usage</span></span>

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="5a174-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="5a174-106">Attributes</span></span>



| <span data-ttu-id="5a174-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="5a174-107">Attribute</span></span>            | <span data-ttu-id="5a174-108">Type</span><span class="sxs-lookup"><span data-stu-id="5a174-108">Type</span></span>                         | <span data-ttu-id="5a174-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5a174-109">Required</span></span>      | <span data-ttu-id="5a174-110">Description</span><span class="sxs-lookup"><span data-stu-id="5a174-110">Description</span></span>                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| <span data-ttu-id="5a174-111">**file**</span><span class="sxs-lookup"><span data-stu-id="5a174-111">**file**</span></span><br/>  | <span data-ttu-id="5a174-112">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="5a174-112">character\_string</span></span><br/> | <span data-ttu-id="5a174-113">Non</span><span class="sxs-lookup"><span data-stu-id="5a174-113">No</span></span><br/> | <span data-ttu-id="5a174-114">Chemin d’accès au fichier à inclure.</span><span class="sxs-lookup"><span data-stu-id="5a174-114">The path to the file to include.</span></span><br/> <br/>  |
| <span data-ttu-id="5a174-115">**macrovirus**</span><span class="sxs-lookup"><span data-stu-id="5a174-115">**macro**</span></span><br/> | <span data-ttu-id="5a174-116">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="5a174-116">character\_string</span></span><br/> | <span data-ttu-id="5a174-117">Non</span><span class="sxs-lookup"><span data-stu-id="5a174-117">No</span></span><br/> | <span data-ttu-id="5a174-118">Nom de la macro à inclure.</span><span class="sxs-lookup"><span data-stu-id="5a174-118">The name of the macro to include.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="5a174-119">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5a174-119">Child elements</span></span>

<span data-ttu-id="5a174-120">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="5a174-120">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="5a174-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5a174-121">Parent elements</span></span>



| <span data-ttu-id="5a174-122">Élément</span><span class="sxs-lookup"><span data-stu-id="5a174-122">Element</span></span>                         | <span data-ttu-id="5a174-123">Description</span><span class="sxs-lookup"><span data-stu-id="5a174-123">Description</span></span>                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a174-124">**fichier**</span><span class="sxs-lookup"><span data-stu-id="5a174-124">**file**</span></span>](file.md)<br/> | <span data-ttu-id="5a174-125">Indique au générateur de code de générer un fichier et spécifie le nom du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="5a174-125">Directs the code generator to generate a file and specifies the output file name.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="5a174-126">Notes</span><span class="sxs-lookup"><span data-stu-id="5a174-126">Remarks</span></span>

<span data-ttu-id="5a174-127">L’attribut de **macro** ou l’attribut de **fichier** doit être spécifié.</span><span class="sxs-lookup"><span data-stu-id="5a174-127">Either the **macro** attribute or the **file** attribute must be specified.</span></span> <span data-ttu-id="5a174-128">Ne spécifiez pas les deux attributs.</span><span class="sxs-lookup"><span data-stu-id="5a174-128">Do not specify both attributes.</span></span>

<span data-ttu-id="5a174-129">WsdCodeGen définit une macro nommée **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="5a174-129">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="5a174-130">Lorsque cette macro est incluse, le code généré contient un bloc de commentaires de visibilité élevée qui indique aux développeurs qu’ils ne peuvent pas modifier le code généré.</span><span class="sxs-lookup"><span data-stu-id="5a174-130">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

## <a name="examples"></a><span data-ttu-id="5a174-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="5a174-131">Examples</span></span>

<span data-ttu-id="5a174-132">Le code XML suivant montre comment inclure la macro **DoNotModify** .</span><span class="sxs-lookup"><span data-stu-id="5a174-132">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="5a174-133">Ce code XML peut être ajouté à un fichier de configuration XML pour WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="5a174-133">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="5a174-134">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5a174-134">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="5a174-135">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a174-135">Minimum supported system</span></span><br/> | <span data-ttu-id="5a174-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a174-136">Windows Vista</span></span> |
| <span data-ttu-id="5a174-137">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="5a174-137">Can be empty</span></span>                        | <span data-ttu-id="5a174-138">Oui</span><span class="sxs-lookup"><span data-stu-id="5a174-138">Yes</span></span>           |



 

 




