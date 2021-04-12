---
description: La propriété d’espace de noms de l’objet SWbemObjectPath contient le nom de l’espace de noms qui fait partie du chemin d’accès de l’objet.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Propriété SWbemObjectPath. Namespace (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 885f7069e901d1d4a490ad7539077463f6c1838c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203355"
---
# <a name="swbemobjectpathnamespace-property"></a><span data-ttu-id="9b940-103">Propriété SWbemObjectPath. Namespace</span><span class="sxs-lookup"><span data-stu-id="9b940-103">SWbemObjectPath.Namespace property</span></span>

<span data-ttu-id="9b940-104">La propriété d' **espace de noms** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) contient le nom de l’espace de noms qui fait partie du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="9b940-104">The **Namespace** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the name of the namespace that is part of the object path.</span></span> <span data-ttu-id="9b940-105">Par exemple, le chemin d’accès suivant montre la propriété d’espace de noms qui retourne \\ cimv2 racine :</span><span class="sxs-lookup"><span data-stu-id="9b940-105">For example, the following path shows the namespace property that returns root\\cimv2:</span></span>

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

<span data-ttu-id="9b940-106">Pour plus d’explications sur la syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9b940-106">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="9b940-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9b940-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b940-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b940-108">Syntax</span></span>


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a><span data-ttu-id="9b940-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9b940-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="9b940-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="9b940-110">Examples</span></span>

<span data-ttu-id="9b940-111">L’exemple suivant montre comment obtenir le nom de l’espace de noms à partir d’instances de disques [**\_ logiques Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) qui sont des disques durs.</span><span class="sxs-lookup"><span data-stu-id="9b940-111">The following example shows you how to obtain the namespace name from instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) that are hard disks.</span></span> <span data-ttu-id="9b940-112">Le script se connecte à l’espace de noms par défaut.</span><span class="sxs-lookup"><span data-stu-id="9b940-112">The script connects to the default namespace.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a><span data-ttu-id="9b940-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b940-113">Requirements</span></span>



| <span data-ttu-id="9b940-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b940-114">Requirement</span></span> | <span data-ttu-id="9b940-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b940-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b940-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b940-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9b940-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b940-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b940-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b940-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9b940-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b940-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b940-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="9b940-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b940-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b940-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b940-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9b940-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="9b940-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9b940-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9b940-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9b940-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b940-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b940-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9b940-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="9b940-126">CLSID</span></span><br/>                    | <span data-ttu-id="9b940-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="9b940-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="9b940-128">IID</span><span class="sxs-lookup"><span data-stu-id="9b940-128">IID</span></span><br/>                      | <span data-ttu-id="9b940-129">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="9b940-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

