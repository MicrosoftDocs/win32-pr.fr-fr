---
description: 'Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un <élément wsdl : import> dans un fichier WSDL.'
ms.assetid: 9a50ee38-fadf-4112-8430-cb5a07ae04ce
title: élément excludeImport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c08d8880029d9e03917e48b61561e3ab3eb2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863998"
---
# <a name="excludeimport-element"></a><span data-ttu-id="e214b-103">élément excludeImport</span><span class="sxs-lookup"><span data-stu-id="e214b-103">excludeImport element</span></span>

<span data-ttu-id="e214b-104">Empêche la génération d’instructions d’importation pour des cibles spécifiées nommées dans un <élément wsdl : import> dans un fichier WSDL.</span><span class="sxs-lookup"><span data-stu-id="e214b-104">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <span data-ttu-id="e214b-105">Cela peut être utilisé pour empêcher WsdCodeGen d’importer des cibles connues, telles que les spécifications WS-Addressing et WS-Eventing, même si ces cibles sont référencées dans le WSDL.</span><span class="sxs-lookup"><span data-stu-id="e214b-105">This can be used to keep WsdCodeGen from importing well-known targets, such as the WS-Addressing and WS-Eventing specifications, even though these targets are referenced in the WSDL.</span></span>

<span data-ttu-id="e214b-106">La valeur de cet élément doit être définie sur l’espace de noms nommé dans l’élément <wsdl : import> à exclure.</span><span class="sxs-lookup"><span data-stu-id="e214b-106">The value of this element must be set to the namespace named in the <wsdl:import> element to exclude.</span></span>

## <a name="usage"></a><span data-ttu-id="e214b-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="e214b-107">Usage</span></span>

``` syntax
<excludeImport/>
```

## <a name="attributes"></a><span data-ttu-id="e214b-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="e214b-108">Attributes</span></span>

<span data-ttu-id="e214b-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="e214b-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e214b-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e214b-110">Child elements</span></span>

<span data-ttu-id="e214b-111">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="e214b-111">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="e214b-112">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e214b-112">Parent elements</span></span>



| <span data-ttu-id="e214b-113">Élément</span><span class="sxs-lookup"><span data-stu-id="e214b-113">Element</span></span>                         | <span data-ttu-id="e214b-114">Description</span><span class="sxs-lookup"><span data-stu-id="e214b-114">Description</span></span>                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="e214b-115">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="e214b-115">**wsdl**</span></span>](wsdl.md)<br/> | <span data-ttu-id="e214b-116">Spécifie un fichier WSDL à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="e214b-116">Specifies a WSDL file to process for contract information.</span></span><br/> <br/> |



## <a name="element-information"></a><span data-ttu-id="e214b-117">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e214b-117">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="e214b-118">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e214b-118">Minimum supported system</span></span><br/> | <span data-ttu-id="e214b-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e214b-119">Windows Vista</span></span> |
| <span data-ttu-id="e214b-120">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="e214b-120">Can be empty</span></span>                        | <span data-ttu-id="e214b-121">Oui</span><span class="sxs-lookup"><span data-stu-id="e214b-121">Yes</span></span>           |



 

 




