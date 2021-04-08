---
title: Ressource de police
description: Définit un fichier qui contient une police.
ms.assetid: 0e19edd5-6cfc-44e6-add4-7413eb94867a
keywords:
- Menus des ressources de polices et autres ressources
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e205d80779a1a228ee50e062f6904c1ed4a4934
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678693"
---
# <a name="font-resource"></a><span data-ttu-id="56643-104">Ressource de police</span><span class="sxs-lookup"><span data-stu-id="56643-104">FONT resource</span></span>

<span data-ttu-id="56643-105">Définit un fichier qui contient une police.</span><span class="sxs-lookup"><span data-stu-id="56643-105">Defines a file that contains a font.</span></span>

``` syntax
nameID FONT filename
```

## <a name="parameters"></a><span data-ttu-id="56643-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56643-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56643-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="56643-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="56643-108">Valeur d’entier non signé 16 bits unique identifiant la ressource.</span><span class="sxs-lookup"><span data-stu-id="56643-108">Unique 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="56643-109"><span id="filename"></span><span id="FILENAME"></span>*extension*</span><span class="sxs-lookup"><span data-stu-id="56643-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="56643-110">Nom du fichier qui contient la ressource.</span><span class="sxs-lookup"><span data-stu-id="56643-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="56643-111">Le nom doit être un nom de fichier valide ; il doit s’agir d’un chemin d’accès complet si le fichier ne se trouve pas dans le répertoire de travail actuel.</span><span class="sxs-lookup"><span data-stu-id="56643-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="56643-112">Le chemin d’accès doit être une chaîne entre guillemets.</span><span class="sxs-lookup"><span data-stu-id="56643-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="56643-113">Certains attributs sont également pris en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="56643-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="56643-114">Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="56643-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="56643-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="56643-115">Examples</span></span>

<span data-ttu-id="56643-116">L’exemple suivant définit une ressource de police unique :</span><span class="sxs-lookup"><span data-stu-id="56643-116">The following example defines a single font resource:</span></span>

``` syntax
5 FONT  "cmroman.fnt"
```

 

 




