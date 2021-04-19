---
description: La propriété locale de l’objet SWbemObjectPath contient les paramètres régionaux du chemin d’accès à l’objet.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Propriété SWbemObjectPath. locale (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a046d3dabd21b9fc46f63764f9a5c7f3e8701d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530088"
---
# <a name="swbemobjectpathlocale-property"></a><span data-ttu-id="47f55-103">Propriété SWbemObjectPath. locale</span><span class="sxs-lookup"><span data-stu-id="47f55-103">SWbemObjectPath.Locale property</span></span>

<span data-ttu-id="47f55-104">La propriété **locale** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) contient les paramètres régionaux du chemin d’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="47f55-104">The **Locale** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the locale of object path.</span></span>

<span data-ttu-id="47f55-105">Lorsque la propriété **SWbemObjectPath. locale** fait partie d’un objet [**SWbemObjectPath**](swbemobjectpath.md) autonome, elle est en lecture/écriture et peut être utilisée pour définir le composant de paramètres régionaux du moniker.</span><span class="sxs-lookup"><span data-stu-id="47f55-105">When the **SWbemObjectPath.Locale** property is part of a standalone [**SWbemObjectPath**](swbemobjectpath.md) object, it is read/write and can be used to set the locale component of the moniker.</span></span>

<span data-ttu-id="47f55-106">Lorsque la propriété **SWbemObjectPath. locale** est accessible dans le cadre d’une propriété [**SWbemObject. \_ path**](swbemobject-path-.md) , elle est en lecture seule et signale la valeur des paramètres régionaux utilisés dans la liaison à l’espace de noms à partir duquel l’objet a été obtenu.</span><span class="sxs-lookup"><span data-stu-id="47f55-106">When the **SWbemObjectPath.Locale** property is accessed as part of a [**SWbemObject.Path\_**](swbemobject-path-.md) property, it is read-only and reports the value of the locale used in binding to the namespace from which the object was obtained.</span></span>

<span data-ttu-id="47f55-107">Pour les identificateurs de paramètres régionaux Microsoft, le format de la chaîne est « MS \_ xxxx », où xxxx est une chaîne au format hexadécimal qui indique le LCID.</span><span class="sxs-lookup"><span data-stu-id="47f55-107">For Microsoft locale identifiers, the format of the string is "MS\_xxxx", where xxxx is a string in hexadecimal form that indicates the LCID.</span></span> <span data-ttu-id="47f55-108">Par exemple, l’identificateur de paramètres régionaux anglais américain est « MS \_ 409 ».</span><span class="sxs-lookup"><span data-stu-id="47f55-108">For example, the American English locale identifier is "MS\_409".</span></span>

<span data-ttu-id="47f55-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="47f55-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="47f55-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="47f55-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f55-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47f55-111">Syntax</span></span>


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a><span data-ttu-id="47f55-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="47f55-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="47f55-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47f55-113">Requirements</span></span>



| <span data-ttu-id="47f55-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47f55-114">Requirement</span></span> | <span data-ttu-id="47f55-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="47f55-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47f55-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47f55-116">Minimum supported client</span></span><br/> | <span data-ttu-id="47f55-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47f55-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="47f55-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47f55-118">Minimum supported server</span></span><br/> | <span data-ttu-id="47f55-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="47f55-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="47f55-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="47f55-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="47f55-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47f55-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="47f55-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="47f55-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="47f55-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="47f55-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="47f55-124">DLL</span><span class="sxs-lookup"><span data-stu-id="47f55-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47f55-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47f55-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="47f55-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="47f55-126">CLSID</span></span><br/>                    | <span data-ttu-id="47f55-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="47f55-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="47f55-128">IID</span><span class="sxs-lookup"><span data-stu-id="47f55-128">IID</span></span><br/>                      | <span data-ttu-id="47f55-129">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="47f55-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




