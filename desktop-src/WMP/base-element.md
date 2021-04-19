---
title: Élément de BASE
description: L’élément BASE définit une chaîne d’URL ajoutée au début des URL envoyées au lecteur Windows Media.
ms.assetid: 887cf860-d06e-44a1-b729-28a285f6c7d3
keywords:
- Élément de BASE lecteur Windows Media
topic_type:
- apiref
api_name:
- BASE Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44b62a24f73ed6cf78820efe1ca76e0eccd3fb59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529944"
---
# <a name="base-element"></a><span data-ttu-id="d678b-104">Élément de BASE</span><span class="sxs-lookup"><span data-stu-id="d678b-104">BASE Element</span></span>

<span data-ttu-id="d678b-105">L’élément **base** définit une chaîne d’URL ajoutée au début des URL envoyées au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d678b-105">The **BASE** element defines a URL string appended to the front of URLs sent to Windows Media Player.</span></span>

``` syntax
<BASE
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="d678b-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="d678b-106">Attributes</span></span>

<span data-ttu-id="d678b-107">**Href** (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="d678b-107">**HREF** (required)</span></span>

<span data-ttu-id="d678b-108">Chaîne ajoutée au début des URL envoyées au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d678b-108">The string appended to the front to URLs sent to Windows Media Player.</span></span> <span data-ttu-id="d678b-109">La valeur par défaut est la chaîne null ("").</span><span class="sxs-lookup"><span data-stu-id="d678b-109">The default value is the null string ("").</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="d678b-110">Éléments parent/enfant</span><span class="sxs-lookup"><span data-stu-id="d678b-110">Parent/Child Elements</span></span>



| <span data-ttu-id="d678b-111">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="d678b-111">Hierarchy</span></span>       | <span data-ttu-id="d678b-112">Éléments</span><span class="sxs-lookup"><span data-stu-id="d678b-112">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="d678b-113">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d678b-113">Parent elements</span></span> | <span data-ttu-id="d678b-114">**ASX**, **entrée**</span><span class="sxs-lookup"><span data-stu-id="d678b-114">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="d678b-115">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d678b-115">Child elements</span></span>  | <span data-ttu-id="d678b-116">Aucune</span><span class="sxs-lookup"><span data-stu-id="d678b-116">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="d678b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d678b-117">Remarks</span></span>

<span data-ttu-id="d678b-118">Cet élément définit une chaîne d’URL ajoutée au début des URL-Flip URL envoyées au lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d678b-118">This element defines a URL string appended to the front of URL-flip URLs sent to Windows Media Player.</span></span> <span data-ttu-id="d678b-119">Le basculement d’URL est un mécanisme de script qui amène le lecteur Windows Media à ouvrir une nouvelle URL dans un navigateur ou un cadre de navigateur lorsqu’il reçoit une commande de script.</span><span class="sxs-lookup"><span data-stu-id="d678b-119">URL-flipping is a scripting mechanism that causes Windows Media Player to open a new URL in a browser or browser frame when it receives a script command.</span></span>

<span data-ttu-id="d678b-120">L’élément de **base** est similaire à un répertoire de base pour les liens relatifs.</span><span class="sxs-lookup"><span data-stu-id="d678b-120">The **BASE** element is similar to a home directory for relative links.</span></span> <span data-ttu-id="d678b-121">Il affecte uniquement les URL envoyées à l’aide de commandes de script dans le cadre du flux de contenu qui est lu dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d678b-121">It only affects URLs sent using script commands as part of the content stream that is playing in Windows Media Player.</span></span>

<span data-ttu-id="d678b-122">Un élément de **base** défini en tant qu’enfant d’un élément **ASX** devient la valeur par défaut pour l’ensemble du métafichier.</span><span class="sxs-lookup"><span data-stu-id="d678b-122">A **BASE** element defined as the child of an **ASX** element becomes the default for the entire metafile.</span></span> <span data-ttu-id="d678b-123">Un élément de **base** défini dans un élément d' **entrée** remplace tout élément de **base** dans l’élément **ASX** parent (pour cet élément d' **entrée** uniquement).</span><span class="sxs-lookup"><span data-stu-id="d678b-123">A **BASE** element defined in an **ENTRY** element overrides any **BASE** element in the parent **ASX** element (for that **ENTRY** element only).</span></span>

> [!Note]  
> <span data-ttu-id="d678b-124">Si l’attribut **href** ne se termine pas par un caractère/, le lecteur Windows Media ajoute l’un à la fin de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d678b-124">If the **HREF** attribute does not end with a / character, Windows Media Player appends one to the end of the string.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d678b-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="d678b-125">Examples</span></span>


```XML
<BASE HREF="https://msdn.microsoft.com/" />

```



## <a name="requirements"></a><span data-ttu-id="d678b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d678b-126">Requirements</span></span>



| <span data-ttu-id="d678b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d678b-127">Requirement</span></span> | <span data-ttu-id="d678b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="d678b-128">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d678b-129">Version</span><span class="sxs-lookup"><span data-stu-id="d678b-129">Version</span></span><br/> | <span data-ttu-id="d678b-130">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="d678b-130">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d678b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d678b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d678b-132">**Informations de référence sur les éléments de métafichier Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d678b-132">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d678b-133">**Informations de référence sur les métafichiers Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d678b-133">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





