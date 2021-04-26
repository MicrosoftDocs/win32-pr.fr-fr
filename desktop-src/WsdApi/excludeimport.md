---
description: 'Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un élément wsdl : import dans un fichier WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: élément excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e14d79576151fbb3dc266621c3fa34816cea55e5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995876"
---
# <a name="excludeimport-element"></a><span data-ttu-id="188e7-103">élément excludeImport</span><span class="sxs-lookup"><span data-stu-id="188e7-103">excludeImport element</span></span>

<span data-ttu-id="188e7-104">Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un \<wsdl:import> élément d’un fichier WSDL.</span><span class="sxs-lookup"><span data-stu-id="188e7-104">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="188e7-105">Cela peut être utilisé pour empêcher WsdCodeGen d’importer des cibles connues, telles que les spécifications WS-Addressing et WS-Eventing, même si ces cibles sont référencées dans le WSDL.</span><span class="sxs-lookup"><span data-stu-id="188e7-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="188e7-106">La valeur de cet élément doit être définie sur l’espace de noms nommé dans l' \<wsdl:import> élément à exclure.</span><span class="sxs-lookup"><span data-stu-id="188e7-106">The value of this element must be set to the namespace named in the \<wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="188e7-107">Usage</span><span class="sxs-lookup"><span data-stu-id="188e7-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="188e7-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="188e7-108">Attributes</span></span>

<span data-ttu-id="188e7-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="188e7-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="188e7-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="188e7-110">Child elements</span></span>

<span data-ttu-id="188e7-111">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="188e7-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="188e7-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="188e7-112">Parent elements</span></span>



| <span data-ttu-id="188e7-113">Élément</span><span class="sxs-lookup"><span data-stu-id="188e7-113">Element</span></span>                         | <span data-ttu-id="188e7-114">Description</span><span class="sxs-lookup"><span data-stu-id="188e7-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="188e7-115">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="188e7-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="188e7-116">Spécifie un fichier WSDL à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="188e7-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="188e7-117">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="188e7-117">Element information</span></span>



| <span data-ttu-id="188e7-118">Étiquette</span><span class="sxs-lookup"><span data-stu-id="188e7-118">Label</span></span> | <span data-ttu-id="188e7-119">Value</span><span class="sxs-lookup"><span data-stu-id="188e7-119">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="188e7-120">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="188e7-120">Minimum supported system</span></span><br/> | <span data-ttu-id="188e7-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="188e7-121">Windows Vista</span></span> |
| <span data-ttu-id="188e7-122">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="188e7-122">Can be empty</span></span>                        | <span data-ttu-id="188e7-123">Oui</span><span class="sxs-lookup"><span data-stu-id="188e7-123">Yes</span></span>           |



 

 




