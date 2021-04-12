---
description: Définit le numéro de la couche de code à générer.
ms.assetid: ad67a6fb-4bb6-4550-a9e9-f5219f3868c6
title: élément layerNumber
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c22a20db7817e449b05c943c9016b6002f35b54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203149"
---
# <a name="layernumber-element"></a><span data-ttu-id="e81f1-103">élément layerNumber</span><span class="sxs-lookup"><span data-stu-id="e81f1-103">layerNumber element</span></span>

<span data-ttu-id="e81f1-104">Définit le numéro de la couche de code à générer.</span><span class="sxs-lookup"><span data-stu-id="e81f1-104">Defines the number of the code layer to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="e81f1-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e81f1-105">Usage</span></span>

``` syntax
<layerNumber/>
```

## <a name="attributes"></a><span data-ttu-id="e81f1-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="e81f1-106">Attributes</span></span>

<span data-ttu-id="e81f1-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="e81f1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e81f1-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e81f1-108">Child elements</span></span>

<span data-ttu-id="e81f1-109">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="e81f1-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e81f1-110">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e81f1-110">Parent elements</span></span>



| <span data-ttu-id="e81f1-111">Élément</span><span class="sxs-lookup"><span data-stu-id="e81f1-111">Element</span></span>                                     | <span data-ttu-id="e81f1-112">Description</span><span class="sxs-lookup"><span data-stu-id="e81f1-112">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="e81f1-113">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="e81f1-113">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="e81f1-114">Élément racine d’un fichier de script XML du générateur de code WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="e81f1-114">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="e81f1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e81f1-115">Remarks</span></span>

<span data-ttu-id="e81f1-116">Les numéros de couche sont utilisés dans les tables du runtime pour distinguer une couche de code d’une autre.</span><span class="sxs-lookup"><span data-stu-id="e81f1-116">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="e81f1-117">WSDAPI utilise le code généré qui a un numéro de couche 0.</span><span class="sxs-lookup"><span data-stu-id="e81f1-117">WSDAPI itself uses generated code that has a layer number of 0.</span></span>

<span data-ttu-id="e81f1-118">En général, cette valeur est 1, ce qui indique que le code généré est superposé au-dessus de WSDAPI et aucune autre couche.</span><span class="sxs-lookup"><span data-stu-id="e81f1-118">Typically, this value will be 1, indicating that the generated code is layered on top of WSDAPI and no other layer.</span></span> <span data-ttu-id="e81f1-119">Dans certains cas, des nombres plus élevés peuvent être utilisés.</span><span class="sxs-lookup"><span data-stu-id="e81f1-119">In some cases, higher numbers may be used.</span></span> <span data-ttu-id="e81f1-120">Par exemple, si une société produit du code pour une classe d’appareil (couche 1 numérotée), un fournisseur de matériel particulier peut souhaiter ajouter une couche 2 supplémentaire numérotée à la couche.</span><span class="sxs-lookup"><span data-stu-id="e81f1-120">For example, if one company produces code for a device class (numbered layer 1), a particular hardware vendor may want to add an additional layer numbered layer 2.</span></span>

<span data-ttu-id="e81f1-121">Les valeurs autorisées, sauf dans le cas de WSDAPI lui-même sont supérieures à 0 et inférieures à 16.</span><span class="sxs-lookup"><span data-stu-id="e81f1-121">Legal values, except in the case of WSDAPI itself are greater than 0 and less than 16.</span></span>

## <a name="element-information"></a><span data-ttu-id="e81f1-122">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e81f1-122">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e81f1-123">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e81f1-123">Minimum supported system</span></span><br/> | <span data-ttu-id="e81f1-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e81f1-124">Windows Vista</span></span> |
| <span data-ttu-id="e81f1-125">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="e81f1-125">Can be empty</span></span>                        | <span data-ttu-id="e81f1-126">Oui</span><span class="sxs-lookup"><span data-stu-id="e81f1-126">Yes</span></span>           |



 

 




