---
description: Définit le texte ou CDATA à réutiliser par l’élément Include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: macro, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f794566b0fd789c463d404289644976c8301a2e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994326"
---
# <a name="macro-element"></a><span data-ttu-id="44086-103">macro, élément</span><span class="sxs-lookup"><span data-stu-id="44086-103">macro element</span></span>

<span data-ttu-id="44086-104">Définit le texte ou CDATA à réutiliser par l’élément [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="44086-104">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span>

## <a name="usage"></a><span data-ttu-id="44086-105">Usage</span><span class="sxs-lookup"><span data-stu-id="44086-105">Usage</span></span>

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a><span data-ttu-id="44086-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="44086-106">Attributes</span></span>



| <span data-ttu-id="44086-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="44086-107">Attribute</span></span>           | <span data-ttu-id="44086-108">Type</span><span class="sxs-lookup"><span data-stu-id="44086-108">Type</span></span>                         | <span data-ttu-id="44086-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="44086-109">Required</span></span>       | <span data-ttu-id="44086-110">Description</span><span class="sxs-lookup"><span data-stu-id="44086-110">Description</span></span>                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| <span data-ttu-id="44086-111">**name**</span><span class="sxs-lookup"><span data-stu-id="44086-111">**name**</span></span><br/> | <span data-ttu-id="44086-112">chaîne de caractères \_</span><span class="sxs-lookup"><span data-stu-id="44086-112">character\_string</span></span><br/> | <span data-ttu-id="44086-113">Oui</span><span class="sxs-lookup"><span data-stu-id="44086-113">Yes</span></span><br/> | <span data-ttu-id="44086-114">Nom de la macro.</span><span class="sxs-lookup"><span data-stu-id="44086-114">The name of the macro.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="44086-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="44086-115">Child elements</span></span>

<span data-ttu-id="44086-116">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="44086-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="44086-117">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="44086-117">Parent elements</span></span>



| <span data-ttu-id="44086-118">Élément</span><span class="sxs-lookup"><span data-stu-id="44086-118">Element</span></span>                                     | <span data-ttu-id="44086-119">Description</span><span class="sxs-lookup"><span data-stu-id="44086-119">Description</span></span>                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="44086-120">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="44086-120">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="44086-121">Élément racine d’un fichier de script XML du générateur de code WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="44086-121">The root element of a WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="44086-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="44086-122">Remarks</span></span>

<span data-ttu-id="44086-123">WsdCodeGen définit une macro nommée **DoNotModify**.</span><span class="sxs-lookup"><span data-stu-id="44086-123">WsdCodeGen defines a macro named **DoNotModify**.</span></span> <span data-ttu-id="44086-124">Lorsque cette macro est incluse, le code généré contient un bloc de commentaires de visibilité élevée qui indique aux développeurs qu’ils ne peuvent pas modifier le code généré.</span><span class="sxs-lookup"><span data-stu-id="44086-124">When this macro is included, the generated code contains a high-visibility comment block that instructs developers not to modify the generated code.</span></span>

<span data-ttu-id="44086-125">Le code XML suivant montre comment inclure la macro **DoNotModify** .</span><span class="sxs-lookup"><span data-stu-id="44086-125">The following XML shows how to include the **DoNotModify** macro.</span></span> <span data-ttu-id="44086-126">Ce code XML peut être ajouté à un fichier de configuration XML pour WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="44086-126">This XML can be added to an XML configuration file for WsdCodeGen.</span></span>

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a><span data-ttu-id="44086-127">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="44086-127">Element information</span></span>



| <span data-ttu-id="44086-128">Étiquette</span><span class="sxs-lookup"><span data-stu-id="44086-128">Label</span></span> | <span data-ttu-id="44086-129">Value</span><span class="sxs-lookup"><span data-stu-id="44086-129">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="44086-130">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44086-130">Minimum supported system</span></span><br/> | <span data-ttu-id="44086-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44086-131">Windows Vista</span></span> |
| <span data-ttu-id="44086-132">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="44086-132">Can be empty</span></span>                        | <span data-ttu-id="44086-133">Oui</span><span class="sxs-lookup"><span data-stu-id="44086-133">Yes</span></span>           |



 

 




