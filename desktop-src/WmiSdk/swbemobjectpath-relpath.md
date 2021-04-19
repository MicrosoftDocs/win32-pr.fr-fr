---
description: La propriété RelPath de l’objet SWbemObjectPath contient le chemin d’accès relatif à partir du chemin d’accès complet.
ms.assetid: 9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b
ms.tgt_platform: multiple
title: SWbemObjectPath. RelPath, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Relpath
- ISWbemObjectPath.Relpath
- ISWbemObjectPath.get_Relpath
- ISWbemObjectPath.put_Relpath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8330d1cdc65e818acd4fda63b223303b779b5472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521138"
---
# <a name="swbemobjectpathrelpath-property"></a><span data-ttu-id="50d68-103">SWbemObjectPath. RelPath, propriété</span><span class="sxs-lookup"><span data-stu-id="50d68-103">SWbemObjectPath.Relpath property</span></span>

<span data-ttu-id="50d68-104">La propriété **RelPath** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) contient le chemin d’accès relatif à partir du chemin d’accès complet.</span><span class="sxs-lookup"><span data-stu-id="50d68-104">The **Relpath** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the relative path from the complete path.</span></span>

<span data-ttu-id="50d68-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="50d68-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="50d68-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="50d68-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d68-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50d68-107">Syntax</span></span>


```VB
SWbemObjectPath.Relpath As String
```



## <a name="property-value"></a><span data-ttu-id="50d68-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="50d68-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="50d68-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="50d68-109">Examples</span></span>

<span data-ttu-id="50d68-110">L’exemple de code VBScript suivant illustre la différence entre les données obtenues à partir de [**SWbemObject. Path \_**](swbemobject-path-.md) et **SWbemObjectPath. RelPath**.</span><span class="sxs-lookup"><span data-stu-id="50d68-110">The following VBScript code example shows the difference between the data obtained from [**SWbemObject.Path\_**](swbemobject-path-.md) and **SWbemObjectPath.Relpath**.</span></span>


```VB
set objWMIService = GetObject ("winmgmts:root/cimv2")

set Processes = objWMIService.ExecQuery( _
    "Select * from win32_process")

For Each Process in Processes
 WScript.Echo Process.Path_ 
 WScript.Echo Process.Path_.Relpath
Next
```



## <a name="requirements"></a><span data-ttu-id="50d68-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50d68-111">Requirements</span></span>



| <span data-ttu-id="50d68-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50d68-112">Requirement</span></span> | <span data-ttu-id="50d68-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="50d68-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50d68-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d68-114">Minimum supported client</span></span><br/> | <span data-ttu-id="50d68-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50d68-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50d68-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d68-116">Minimum supported server</span></span><br/> | <span data-ttu-id="50d68-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50d68-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50d68-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="50d68-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d68-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="50d68-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50d68-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="50d68-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="50d68-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50d68-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50d68-122">DLL</span><span class="sxs-lookup"><span data-stu-id="50d68-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50d68-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50d68-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="50d68-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="50d68-124">CLSID</span></span><br/>                    | <span data-ttu-id="50d68-125">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="50d68-125">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="50d68-126">IID</span><span class="sxs-lookup"><span data-stu-id="50d68-126">IID</span></span><br/>                      | <span data-ttu-id="50d68-127">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="50d68-127">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




