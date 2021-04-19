---
title: VUE. scriptFile
description: L’attribut scriptFile spécifie les noms de fichiers des fichiers JScript associés.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- AFFICHER. scriptFile lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541421"
---
# <a name="viewscriptfile"></a><span data-ttu-id="8cbff-104">VUE. scriptFile</span><span class="sxs-lookup"><span data-stu-id="8cbff-104">VIEW.scriptFile</span></span>

<span data-ttu-id="8cbff-105">L’attribut **scriptFile** spécifie les noms de fichiers des fichiers JScript associés.</span><span class="sxs-lookup"><span data-stu-id="8cbff-105">The **scriptFile** attribute specifies the file names of accompanying JScript files.</span></span>

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a><span data-ttu-id="8cbff-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="8cbff-106">Possible Values</span></span>

<span data-ttu-id="8cbff-107">Cet attribut est une **chaîne** en écriture seule sans valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="8cbff-107">This attribute is a write-only **String** with no default value.</span></span> <span data-ttu-id="8cbff-108">Les noms de fichiers de plusieurs fichiers JScript sont délimités par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="8cbff-108">The file names of multiple JScript files are delimited with semicolons.</span></span> <span data-ttu-id="8cbff-109">Les espaces et les points-virgules de début et suivants ne doivent pas être présents.</span><span class="sxs-lookup"><span data-stu-id="8cbff-109">Leading and following spaces and semicolons should not be present.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cbff-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8cbff-110">Remarks</span></span>

<span data-ttu-id="8cbff-111">Le code dans les fichiers spécifiés peut être utilisé par n’importe quel gestionnaire d’événements dans la vue.</span><span class="sxs-lookup"><span data-stu-id="8cbff-111">The code in the specified files can be used by any event handler in the View.</span></span> <span data-ttu-id="8cbff-112">Le code utilisé par les gestionnaires d’événements dans plusieurs vues peut être placé dans un fichier portant le même nom que le fichier de définition d’apparence, mais avec une extension. js au lieu d’une extension. WMS.</span><span class="sxs-lookup"><span data-stu-id="8cbff-112">Code that is used by event handlers in multiple Views can be placed in a file with the same name as the skin definition file but with a .js extension instead of a .wms extension.</span></span> <span data-ttu-id="8cbff-113">Ce fichier est chargé automatiquement et n’a pas besoin d’être spécifié dans le fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="8cbff-113">This file is loaded automatically and need not be specified in the skin definition file.</span></span>

## <a name="examples"></a><span data-ttu-id="8cbff-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="8cbff-114">Examples</span></span>


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a><span data-ttu-id="8cbff-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cbff-115">Requirements</span></span>



| <span data-ttu-id="8cbff-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cbff-116">Requirement</span></span> | <span data-ttu-id="8cbff-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cbff-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="8cbff-118">Version</span><span class="sxs-lookup"><span data-stu-id="8cbff-118">Version</span></span><br/> | <span data-ttu-id="8cbff-119">Lecteur Windows Media version 7,0 ou ultérieure</span><span class="sxs-lookup"><span data-stu-id="8cbff-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8cbff-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cbff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cbff-121">**Élément VIEW**</span><span class="sxs-lookup"><span data-stu-id="8cbff-121">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





