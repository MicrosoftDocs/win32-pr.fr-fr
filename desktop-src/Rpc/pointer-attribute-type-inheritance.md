---
title: Héritage de type de Pointer-Attribute
description: Selon la spécification DCE, chaque fichier IDL doit définir des attributs pour ses pointeurs.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382496"
---
# <a name="pointer-attribute-type-inheritance"></a><span data-ttu-id="dc7ad-103">Héritage de type de Pointer-Attribute</span><span class="sxs-lookup"><span data-stu-id="dc7ad-103">Pointer-Attribute Type Inheritance</span></span>

<span data-ttu-id="dc7ad-104">Selon la spécification DCE, chaque fichier IDL doit définir des attributs pour ses pointeurs.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-104">According to the DCE specification, each IDL file must define attributes for its pointers.</span></span> <span data-ttu-id="dc7ad-105">Si un attribut explicite n’est pas assigné à un pointeur, le pointeur utilise la valeur spécifiée par le \[ mot clé [ \_ par défaut du pointeur](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="dc7ad-105">If an explicit attribute is not assigned to a pointer, the pointer uses the value specified by the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] keyword.</span></span> <span data-ttu-id="dc7ad-106">Certaines implémentations de DCE n’autorisent pas les pointeurs non attributs.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-106">Some DCE implementations do not allow unattributed pointers.</span></span> <span data-ttu-id="dc7ad-107">Si un pointeur n’a pas d’attribut explicite, le fichier IDL doit avoir une spécification de **\[ pointeur \_ par défaut \]** afin que l’attribut de pointeur puisse être défini.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-107">If a pointer does not have an explicit attribute, the IDL file must have a **\[pointer\_default\]** specification so that the pointer attribute can be set.</span></span>

<span data-ttu-id="dc7ad-108">En mode par défaut (extensions Microsoft), vous pouvez spécifier l’attribut d’un pointeur dans le fichier IDL qui importe le fichier IDL de définition.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-108">In default (Microsoft-extensions) mode, you can specify a pointer's attribute in the IDL file that imports the defining IDL file.</span></span> <span data-ttu-id="dc7ad-109">Les pointeurs définis dans un fichier IDL peuvent hériter des attributs spécifiés dans d’autres fichiers IDL.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-109">Pointers defined in one IDL file can inherit attributes that are specified in other IDL files.</span></span> <span data-ttu-id="dc7ad-110">En outre, dans le mode par défaut, les fichiers IDL peuvent inclure des pointeurs non attributs.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-110">Also, in default mode, IDL files can include unattributed pointers.</span></span> <span data-ttu-id="dc7ad-111">Si ni la base ni les fichiers IDL importés ne spécifient un attribut de pointeur ou un **\[ pointeur \_ par défaut \]**, les pointeurs non attributs sont interprétés comme des pointeurs uniques.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-111">If neither the base nor the imported IDL files specify a pointer attribute or **\[pointer\_default\]**, unattributed pointers are interpreted as unique pointers.</span></span>

<span data-ttu-id="dc7ad-112">Le compilateur MIDL assigne des attributs de pointeur aux pointeurs à l’aide des règles de priorité suivantes (1 est le plus élevé).</span><span class="sxs-lookup"><span data-stu-id="dc7ad-112">The MIDL compiler assigns pointer attributes to pointers using the following priority rules (1 is highest).</span></span>



| <span data-ttu-id="dc7ad-113">Priority</span><span class="sxs-lookup"><span data-stu-id="dc7ad-113">Priority</span></span> | <span data-ttu-id="dc7ad-114">Description</span><span class="sxs-lookup"><span data-stu-id="dc7ad-114">Description</span></span>                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc7ad-115">1</span><span class="sxs-lookup"><span data-stu-id="dc7ad-115">1</span></span>        | <span data-ttu-id="dc7ad-116">Les attributs de pointeur explicites sont appliqués au pointeur au niveau de la définition ou de l’utilisation du site.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-116">Explicit pointer attributes are applied to the pointer at the definition or use site.</span></span>                                      |
| <span data-ttu-id="dc7ad-117">2</span><span class="sxs-lookup"><span data-stu-id="dc7ad-117">2</span></span>        | <span data-ttu-id="dc7ad-118">La valeur par défaut est l’attribut **\[ \_ par défaut \] du pointeur** dans le fichier IDL qui définit le type.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-118">The default is the **\[pointer\_default\]** attribute in the IDL file that defines the type.</span></span>                               |
| <span data-ttu-id="dc7ad-119">3</span><span class="sxs-lookup"><span data-stu-id="dc7ad-119">3</span></span>        | <span data-ttu-id="dc7ad-120">La valeur par défaut est l’attribut **\[ \_ par défaut \] du pointeur** dans le fichier IDL qui importe le type.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-120">The default is the **\[pointer\_default\]** attribute in the IDL file that imports the type.</span></span>                               |
| <span data-ttu-id="dc7ad-121">4</span><span class="sxs-lookup"><span data-stu-id="dc7ad-121">4</span></span>        | <span data-ttu-id="dc7ad-122">La valeur par défaut est \[ [ptr](/windows/desktop/Midl/ptr) \] dans le mode de compatibilité DCE, ou \[ [unique](/windows/desktop/Midl/unique) \] en mode extensions Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc7ad-122">The default is \[ [ptr](/windows/desktop/Midl/ptr)\] in DCE-compatibility mode, or \[ [unique](/windows/desktop/Midl/unique)\] in Microsoft-extensions mode.</span></span> |



 

 

 