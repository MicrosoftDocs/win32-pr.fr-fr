---
description: Indique si WsdCodeGen doit essayer d’indicateur automatique de certains champs générés comme statiques.
ms.assetid: 0c858567-e17a-46a0-b3ff-a0dc8089b0cd
title: autostatic, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32591c43c850af05014ff92fc4023e228b371fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524147"
---
# <a name="autostatic-element"></a><span data-ttu-id="0a79b-103">autostatic, élément</span><span class="sxs-lookup"><span data-stu-id="0a79b-103">autoStatic element</span></span>

<span data-ttu-id="0a79b-104">Indique si WsdCodeGen doit essayer d’indicateur automatique de certains champs générés comme statiques.</span><span class="sxs-lookup"><span data-stu-id="0a79b-104">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="0a79b-105">Ce comportement est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="0a79b-105">This behavior is enabled by default.</span></span>

## <a name="usage"></a><span data-ttu-id="0a79b-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0a79b-106">Usage</span></span>

``` syntax
<autoStatic/>
```

## <a name="attributes"></a><span data-ttu-id="0a79b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="0a79b-107">Attributes</span></span>

<span data-ttu-id="0a79b-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0a79b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0a79b-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0a79b-109">Child elements</span></span>

<span data-ttu-id="0a79b-110">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="0a79b-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="0a79b-111">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0a79b-111">Parent elements</span></span>



| <span data-ttu-id="0a79b-112">Élément</span><span class="sxs-lookup"><span data-stu-id="0a79b-112">Element</span></span>                                     | <span data-ttu-id="0a79b-113">Description</span><span class="sxs-lookup"><span data-stu-id="0a79b-113">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a79b-114">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="0a79b-114">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0a79b-115">Élément racine d’un fichier de script XML du générateur de code WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="0a79b-115">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0a79b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="0a79b-116">Remarks</span></span>

<span data-ttu-id="0a79b-117">L’élément **autostatique** n’est pas obligatoire et peut être omis dans le fichier de configuration XML.</span><span class="sxs-lookup"><span data-stu-id="0a79b-117">The **autoStatic** element is not required and may be omitted from the XML configuration file.</span></span> <span data-ttu-id="0a79b-118">L’élément peut être utilisé pour désactiver le marquage des champs générés comme statiques ou pour forcer explicitement le marquage de certains champs générés comme statiques.</span><span class="sxs-lookup"><span data-stu-id="0a79b-118">The element can be used to disable the flagging of generated fields as static or to explicitly force the flagging of certain generated fields as static.</span></span>

<span data-ttu-id="0a79b-119">Les valeurs possibles sont 1 (activé, valeur par défaut) et 0 (désactivé).</span><span class="sxs-lookup"><span data-stu-id="0a79b-119">Possible values are 1 (enabled, default) and 0 (disabled).</span></span> <span data-ttu-id="0a79b-120">L’activation d' **autostatique** peut entraîner des problèmes de compilation en fonction de la façon dont le générateur de code est dirigé vers les données de sortie.</span><span class="sxs-lookup"><span data-stu-id="0a79b-120">Enabling **autoStatic** may cause compilation issues depending on how the code generator is directed to output data.</span></span>

## <a name="element-information"></a><span data-ttu-id="0a79b-121">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0a79b-121">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0a79b-122">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a79b-122">Minimum supported system</span></span><br/> | <span data-ttu-id="0a79b-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a79b-123">Windows Vista</span></span> |
| <span data-ttu-id="0a79b-124">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="0a79b-124">Can be empty</span></span>                        | <span data-ttu-id="0a79b-125">Oui</span><span class="sxs-lookup"><span data-stu-id="0a79b-125">Yes</span></span>           |



 

 




