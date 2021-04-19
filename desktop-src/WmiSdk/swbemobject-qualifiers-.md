---
description: La propriété Qualifiers \_ de l’objet SWbemObject retourne un objet SWbemQualifierSet qui est une collection des qualificateurs de l’instance ou de la classe actuelle. Cette propriété est en lecture seule.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: SWbemObject.Qualifiers_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521489"
---
# <a name="swbemobjectqualifiers_-property"></a><span data-ttu-id="bb586-104">SWbemObject. Qualifiers, \_ propriété</span><span class="sxs-lookup"><span data-stu-id="bb586-104">SWbemObject.Qualifiers\_ property</span></span>

<span data-ttu-id="bb586-105">La propriété **Qualifiers \_** de l’objet [**SWbemObject**](swbemobject.md) retourne un objet [**SWbemQualifierSet**](swbemqualifierset.md) qui est une collection des qualificateurs de l’instance ou de la classe actuelle.</span><span class="sxs-lookup"><span data-stu-id="bb586-105">The **Qualifiers\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemQualifierSet**](swbemqualifierset.md) object that is a collection of the qualifiers for the current class or instance.</span></span> <span data-ttu-id="bb586-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bb586-106">This property is read-only.</span></span>

<span data-ttu-id="bb586-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bb586-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bb586-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bb586-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb586-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb586-109">Syntax</span></span>


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a><span data-ttu-id="bb586-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bb586-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="bb586-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="bb586-111">Examples</span></span>

<span data-ttu-id="bb586-112">La [liste de tous les qualificateurs d’un exemple de](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) code VBScript de classe WMI dans la Galerie TechNet utilise la \_ propriété qualifier pour répertorier les qualificateurs de classe pour une classe WMI spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bb586-112">The [List All the Qualifiers for a WMI Class](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) VBScript code sample on TechNet Gallery uses the Qualifier\_ property to list the class qualifiers for a specified WMI class.</span></span>

<span data-ttu-id="bb586-113">La [liste de toutes les classes abstraites dans](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) l’exemple de code WMI VBScript sur la Galerie TechNet répertorie toutes les classes WMI abstraites définies dans l' \\ espace de noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="bb586-113">The [List All Abstract Classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript code sample on TechNet Gallery lists all WMI abstract classes defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="bb586-114">L’exemple de code [List All Dynamic classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript utilise la \_ propriété qualifier pour répertorier toutes les classes dynamiques WMI (y compris les classes d’association) définies dans l' \\ espace de noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="bb586-114">The [List All Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript code sample uses the Qualifier\_ property to list all WMI Dynamic classes (including Association classes) defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="bb586-115">L’exemple de code [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell sur la Galerie TechNet répertorie toutes les propriétés accessibles en écriture dans l’espace de noms spécifié.</span><span class="sxs-lookup"><span data-stu-id="bb586-115">The [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell code sample on TechNet Gallery lists all writeable properties in the specified namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb586-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb586-116">Requirements</span></span>



| <span data-ttu-id="bb586-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb586-117">Requirement</span></span> | <span data-ttu-id="bb586-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb586-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb586-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb586-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb586-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bb586-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bb586-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bb586-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb586-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bb586-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bb586-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb586-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb586-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb586-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb586-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bb586-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb586-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bb586-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bb586-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bb586-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb586-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb586-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bb586-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="bb586-129">CLSID</span></span><br/>                    | <span data-ttu-id="bb586-130">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="bb586-130">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="bb586-131">IID</span><span class="sxs-lookup"><span data-stu-id="bb586-131">IID</span></span><br/>                      | <span data-ttu-id="bb586-132">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="bb586-132">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




