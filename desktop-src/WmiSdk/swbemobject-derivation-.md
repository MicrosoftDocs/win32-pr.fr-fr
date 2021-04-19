---
description: La \_ propriété de dérivation de l’objet SWbemObject contient un tableau de chaînes qui décrivent la hiérarchie de dérivation de classes pour l’instance référencée.
ms.assetid: 8a4daab0-7d10-4a37-aacd-1f3f499b859a
ms.tgt_platform: multiple
title: SWbemObject.Derivation_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Derivation_
- ISWbemObject.Derivation_
- ISWbemObject.get_Derivation_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84e7b4e53a1a5544c92bb5116f3f83189789487f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520608"
---
# <a name="swbemobjectderivation_-property"></a><span data-ttu-id="53479-103">SWbemObject. Derivation, \_ propriété</span><span class="sxs-lookup"><span data-stu-id="53479-103">SWbemObject.Derivation\_ property</span></span>

<span data-ttu-id="53479-104">La propriété de **dérivation \_** de l’objet [**SWbemObject**](swbemobject.md) contient un tableau de chaînes qui décrivent la hiérarchie de dérivation de classes pour l’instance référencée.</span><span class="sxs-lookup"><span data-stu-id="53479-104">The **Derivation\_** property of the [**SWbemObject**](swbemobject.md) object contains an array of strings that describe the class derivation hierarchy for the instance being referenced.</span></span> <span data-ttu-id="53479-105">Le premier élément du tableau définit la classe parente et le dernier élément définit la classe Dynasty.</span><span class="sxs-lookup"><span data-stu-id="53479-105">The first element in the array defines the parent class and the last element defines the dynasty class.</span></span> <span data-ttu-id="53479-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="53479-106">This property is read-only.</span></span>

<span data-ttu-id="53479-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="53479-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="53479-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="53479-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="53479-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53479-109">Syntax</span></span>


```VB
SWbemObject.Derivation_ As String
```



## <a name="property-value"></a><span data-ttu-id="53479-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="53479-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="53479-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="53479-111">Examples</span></span>

<span data-ttu-id="53479-112">L’exemple VBScript suivant décrit comment récupérer la hiérarchie de classes pour le \_ disque logique Win32.</span><span class="sxs-lookup"><span data-stu-id="53479-112">The following VBScript sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```VB
on Error resume next

Set c = GetObject("winmgmts://./root/cimv2:win32_logicaldisk")
d = c.Derivation_

for x = LBound(d) to UBound(d)
 WScript.Echo d(x)
Next

if err <> 0 then
 WScript.Echo Err.Description
end if
```



<span data-ttu-id="53479-113">l’exemple perl suivant décrit comment récupérer la hiérarchie de classes pour le \_ disque logique Win32.</span><span class="sxs-lookup"><span data-stu-id="53479-113">he following Perl sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```
use strict;
use Win32::OLE;

my ($C, $D, @collection);

eval {$C = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("win32_logicaldisk") };
unless ($@) 
{
 @collection = in $C;
 eval {$D = $collection[0]->Derivation_();};
 print "\n";
 unless ($@) 
 {
  print map{"$_\n"} @{$D};
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="53479-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53479-114">Requirements</span></span>



| <span data-ttu-id="53479-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53479-115">Requirement</span></span> | <span data-ttu-id="53479-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="53479-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53479-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53479-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53479-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53479-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53479-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53479-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53479-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53479-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53479-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="53479-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="53479-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="53479-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="53479-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="53479-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="53479-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="53479-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="53479-125">DLL</span><span class="sxs-lookup"><span data-stu-id="53479-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53479-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53479-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="53479-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="53479-127">CLSID</span></span><br/>                    | <span data-ttu-id="53479-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="53479-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="53479-129">IID</span><span class="sxs-lookup"><span data-stu-id="53479-129">IID</span></span><br/>                      | <span data-ttu-id="53479-130">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="53479-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




