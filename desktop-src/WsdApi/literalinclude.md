---
description: Place une instruction include C ou IDL dans le code généré.
ms.assetid: 7a7ffd54-09e9-412d-a637-5dc27597b46e
title: élément literalInclude
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e1f43f1b8d3d95e2ad8a378dd1c8cbada7758ad
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995126"
---
# <a name="literalinclude-element"></a><span data-ttu-id="9f556-103">élément literalInclude</span><span class="sxs-lookup"><span data-stu-id="9f556-103">literalInclude element</span></span>

<span data-ttu-id="9f556-104">Place une instruction include C ou IDL dans le code généré.</span><span class="sxs-lookup"><span data-stu-id="9f556-104">Places a C or IDL include statement in the generated code.</span></span>

## <a name="usage"></a><span data-ttu-id="9f556-105">Usage</span><span class="sxs-lookup"><span data-stu-id="9f556-105">Usage</span></span>

``` syntax
<literalInclude
  Language = "language string"
  Local = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="9f556-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="9f556-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f556-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="9f556-107">Attribute</span></span></th>
<th><span data-ttu-id="9f556-108">Type</span><span class="sxs-lookup"><span data-stu-id="9f556-108">Type</span></span></th>
<th><span data-ttu-id="9f556-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9f556-109">Required</span></span></th>
<th><span data-ttu-id="9f556-110">Description</span><span class="sxs-lookup"><span data-stu-id="9f556-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f556-111"><strong>Langage</strong></span><span class="sxs-lookup"><span data-stu-id="9f556-111"><strong>Language</strong></span></span><br/></td>
<td><span data-ttu-id="9f556-112">chaîne de langue</span><span class="sxs-lookup"><span data-stu-id="9f556-112">language string</span></span><br/></td>
<td><span data-ttu-id="9f556-113">Non</span><span class="sxs-lookup"><span data-stu-id="9f556-113">No</span></span><br/></td>
<td><span data-ttu-id="9f556-114">Type de fichier d’en-tête à inclure.</span><span class="sxs-lookup"><span data-stu-id="9f556-114">The type of header file to be included.</span></span> <br/> <br/><span data-ttu-id="9f556-115">
<dt><strong>Secteur</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f556-115">
<dt><strong>C</strong></dt> </span></span><dd> <span data-ttu-id="9f556-116">Incluez un fichier d’en-tête C.</span><span class="sxs-lookup"><span data-stu-id="9f556-116">Include a C header file.</span></span><br/> </dd> <span data-ttu-id="9f556-117"><dt><strong>MIDL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f556-117"><dt><strong>IDL</strong></dt> </span></span><dd> <span data-ttu-id="9f556-118">Incluez un fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="9f556-118">Include an IDL file.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f556-119"><strong>Local</strong></span><span class="sxs-lookup"><span data-stu-id="9f556-119"><strong>Local</strong></span></span><br/></td>
<td><span data-ttu-id="9f556-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="9f556-120">Boolean</span></span><br/></td>
<td><span data-ttu-id="9f556-121">Non</span><span class="sxs-lookup"><span data-stu-id="9f556-121">No</span></span><br/></td>
<td><span data-ttu-id="9f556-122">Cet attribut est utilisé uniquement lorsque la <strong>langue</strong> est définie sur &quot; C &quot; .</span><span class="sxs-lookup"><span data-stu-id="9f556-122">This attribute is only used when <strong>Language</strong> is set to &quot;C&quot;.</span></span><br/> <br/><span data-ttu-id="9f556-123">
<dt><strong>:</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f556-123">
<dt><strong>True</strong></dt> </span></span><dd> <span data-ttu-id="9f556-124">Recherche l’en-tête nommé dans le répertoire actif avant de rechercher dans les répertoires système.</span><span class="sxs-lookup"><span data-stu-id="9f556-124">Searches the current directory for the named header before searching the system directories.</span></span><br/> </dd> <span data-ttu-id="9f556-125"><dt><strong>Fausses</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9f556-125"><dt><strong>False</strong></dt> </span></span><dd> <span data-ttu-id="9f556-126">Recherche uniquement les répertoires système pour l’en-tête nommé.</span><span class="sxs-lookup"><span data-stu-id="9f556-126">Only search system directories for the named header.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="9f556-127">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9f556-127">Child elements</span></span>

<span data-ttu-id="9f556-128">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="9f556-128">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="9f556-129">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="9f556-129">Parent elements</span></span>



| <span data-ttu-id="9f556-130">Élément</span><span class="sxs-lookup"><span data-stu-id="9f556-130">Element</span></span>                         | <span data-ttu-id="9f556-131">Description</span><span class="sxs-lookup"><span data-stu-id="9f556-131">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9f556-132">**txt**</span><span class="sxs-lookup"><span data-stu-id="9f556-132">**file**</span></span>](file.md)<br/> | <span data-ttu-id="9f556-133">Génère un fichier à partir du générateur de code.</span><span class="sxs-lookup"><span data-stu-id="9f556-133">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9f556-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="9f556-134">Remarks</span></span>

<span data-ttu-id="9f556-135">Les exemples suivants illustrent le code généré à partir de différents éléments **literalInclude** .</span><span class="sxs-lookup"><span data-stu-id="9f556-135">The following examples show the code generated from different **literalInclude** elements.</span></span>

### <a name="example-1---generating-a-c-include-statement"></a><span data-ttu-id="9f556-136">Exemple 1 : génération d’une instruction include C</span><span class="sxs-lookup"><span data-stu-id="9f556-136">Example 1 - Generating a C include statement</span></span>

<span data-ttu-id="9f556-137">XML d’entrée :</span><span class="sxs-lookup"><span data-stu-id="9f556-137">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="False">wsdapi.h</literalInclude>
```

<span data-ttu-id="9f556-138">Code de sortie :</span><span class="sxs-lookup"><span data-stu-id="9f556-138">Output code:</span></span>

``` syntax
#include <wsdapi.h>
```

### <a name="example-2---generating-a-c-include-statement"></a><span data-ttu-id="9f556-139">Exemple 2 : génération d’une instruction include C</span><span class="sxs-lookup"><span data-stu-id="9f556-139">Example 2 - Generating a C include statement</span></span>

<span data-ttu-id="9f556-140">XML d’entrée :</span><span class="sxs-lookup"><span data-stu-id="9f556-140">Input XML:</span></span>

``` syntax
<literalInclude Language="C" Local="True">wsdapi.h</literalInclude>
```

<span data-ttu-id="9f556-141">Code de sortie :</span><span class="sxs-lookup"><span data-stu-id="9f556-141">Output code:</span></span>

``` syntax
#include "wsdapi.h"
```

### <a name="example-3---generating-an-idl-import-statement"></a><span data-ttu-id="9f556-142">Exemple 3 : génération d’une instruction d’importation IDL</span><span class="sxs-lookup"><span data-stu-id="9f556-142">Example 3 - Generating an IDL import statement</span></span>

<span data-ttu-id="9f556-143">XML d’entrée :</span><span class="sxs-lookup"><span data-stu-id="9f556-143">Input XML:</span></span>

``` syntax
<literalInclude Language="IDL">wsdclient.idl</literalInclude>
```

<span data-ttu-id="9f556-144">Code de sortie :</span><span class="sxs-lookup"><span data-stu-id="9f556-144">Output code:</span></span>

``` syntax
import wsdclient.idl;
```

## <a name="element-information"></a><span data-ttu-id="9f556-145">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="9f556-145">Element information</span></span>



| <span data-ttu-id="9f556-146">Étiquette</span><span class="sxs-lookup"><span data-stu-id="9f556-146">Label</span></span> | <span data-ttu-id="9f556-147">Value</span><span class="sxs-lookup"><span data-stu-id="9f556-147">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="9f556-148">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9f556-148">Minimum supported system</span></span><br/> | <span data-ttu-id="9f556-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9f556-149">Windows Vista</span></span> |
| <span data-ttu-id="9f556-150">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="9f556-150">Can be empty</span></span>                        | <span data-ttu-id="9f556-151">Oui</span><span class="sxs-lookup"><span data-stu-id="9f556-151">Yes</span></span>           |



 

 




