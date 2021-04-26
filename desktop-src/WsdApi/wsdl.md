---
description: Spécifie un fichier WSDL à traiter pour les informations de contrat.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: élément wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef4bc7b76ce22184e4c2f1ceaa2131ef163a26d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994706"
---
# <a name="wsdl-element"></a><span data-ttu-id="33757-103">élément wsdl</span><span class="sxs-lookup"><span data-stu-id="33757-103">wsdl element</span></span>

<span data-ttu-id="33757-104">Spécifie un fichier WSDL à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="33757-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="33757-105">Usage</span><span class="sxs-lookup"><span data-stu-id="33757-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="33757-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="33757-106">Attributes</span></span>

<span data-ttu-id="33757-107">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="33757-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="33757-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="33757-108">Child elements</span></span>



| <span data-ttu-id="33757-109">Élément</span><span class="sxs-lookup"><span data-stu-id="33757-109">Element</span></span>                                           | <span data-ttu-id="33757-110">Description</span><span class="sxs-lookup"><span data-stu-id="33757-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33757-111">**excludeImport**</span><span class="sxs-lookup"><span data-stu-id="33757-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="33757-112">Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un \<wsdl:import> élément d’un fichier WSDL.</span><span class="sxs-lookup"><span data-stu-id="33757-112">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="33757-113">**importHint**</span><span class="sxs-lookup"><span data-stu-id="33757-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="33757-114">Spécifie l’emplacement de téléchargement pour une \<wsdl:import> directive qui ne spécifie pas explicitement d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="33757-114">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="33757-115">**d**</span><span class="sxs-lookup"><span data-stu-id="33757-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="33757-116">Fichier et chemin d’accès du fichier d’entrée WSDL.</span><span class="sxs-lookup"><span data-stu-id="33757-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="33757-117">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="33757-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="33757-118">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="33757-118">Parent elements</span></span>



| <span data-ttu-id="33757-119">Élément</span><span class="sxs-lookup"><span data-stu-id="33757-119">Element</span></span>                                     | <span data-ttu-id="33757-120">Description</span><span class="sxs-lookup"><span data-stu-id="33757-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="33757-121">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="33757-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="33757-122">Élément racine d’un fichier de script XML du générateur de code WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="33757-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="33757-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="33757-123">Remarks</span></span>

<span data-ttu-id="33757-124">Tout élément [**importHint**](importhint.md) ou [**excludeImport**](excludeimport.md) apparaissant après l’élément [**path**](path.md) dans un fichier de configuration XML sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="33757-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="33757-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="33757-125">Element information</span></span>



| <span data-ttu-id="33757-126">Étiquette</span><span class="sxs-lookup"><span data-stu-id="33757-126">Label</span></span> | <span data-ttu-id="33757-127">Value</span><span class="sxs-lookup"><span data-stu-id="33757-127">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="33757-128">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33757-128">Minimum supported system</span></span><br/> | <span data-ttu-id="33757-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33757-129">Windows Vista</span></span> |
| <span data-ttu-id="33757-130">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="33757-130">Can be empty</span></span>                        | <span data-ttu-id="33757-131">Non</span><span class="sxs-lookup"><span data-stu-id="33757-131">No</span></span>            |



 

 




