---
title: Enumerator. AtEndOfStream, propriété (WSManDisp. h)
description: Obtient une valeur booléenne qui indique s’il y a plus d’éléments dans la collection.
ms.assetid: 5e80674a-7889-4753-b0dd-4d7b44eba00a
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété AtEndOfStream
- Propriété AtEndOfStream Windows Remote Management, objet Enumerator
- Objet Enumerator Windows Remote Management, propriété AtEndOfStream
topic_type:
- apiref
api_name:
- Enumerator.AtEndOfStream
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 023798f6c868e434218dd1a4dbdf1928bf4526a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103265"
---
# <a name="enumeratoratendofstream-property"></a><span data-ttu-id="86019-106">Enumerator. AtEndOfStream, propriété</span><span class="sxs-lookup"><span data-stu-id="86019-106">Enumerator.AtEndOfStream property</span></span>

<span data-ttu-id="86019-107">Obtient une valeur booléenne qui indique s’il y a plus d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="86019-107">Gets a Boolean value that indicates whether there are any more items in the collection.</span></span>

<span data-ttu-id="86019-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="86019-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="86019-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86019-109">Syntax</span></span>


```VB
Enumerator.AtEndOfStream As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="86019-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="86019-110">Property value</span></span>

<dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="86019-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**:**</span><span class="sxs-lookup"><span data-stu-id="86019-111"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</span></span>


</dt> <dd>

<span data-ttu-id="86019-112">Il n’y a plus d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="86019-112">No more items are in the collection.</span></span>

</dd> <dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="86019-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Fausses**</span><span class="sxs-lookup"><span data-stu-id="86019-113"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</span></span>


</dt> <dd>

<span data-ttu-id="86019-114">D’autres éléments sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="86019-114">More items are available.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86019-115">Notes</span><span class="sxs-lookup"><span data-stu-id="86019-115">Remarks</span></span>

<span data-ttu-id="86019-116">Si vous libérez l’objet [**énumérateur**](enumerator.md) après avoir obtenu toutes les données requises, toutes les demandes d’énumération en attente sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="86019-116">If you free the [**Enumerator**](enumerator.md) object after you have obtained all the data required, then any pending enumeration requests are removed.</span></span> <span data-ttu-id="86019-117">Pour plus d’informations, consultez [énumération ou liste de toutes les instances d’une ressource](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="86019-117">For more information, see [Enumerating or Listing All of the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span>

## <a name="examples"></a><span data-ttu-id="86019-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="86019-118">Examples</span></span>

<span data-ttu-id="86019-119">L’exemple VBScript suivant énumère les instances du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="86019-119">The following VBScript example enumerates operating system instances.</span></span> <span data-ttu-id="86019-120">Notez que la libération de l’objet d’énumération nettoie toutes les demandes d’énumération en attente.</span><span class="sxs-lookup"><span data-stu-id="86019-120">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span> <span data-ttu-id="86019-121">La sous-routine DisplayOutput met en forme la sortie des données de la même façon que l’outil WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="86019-121">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & _
    RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
    "wmi/root/cimv2/Win32_OperatingSystem"

Set objResultSet = objSession.Enumerate( strResource )

While Not objResultSet.AtEndOfStream
 
 DisplayOutput( objResultSet.ReadItem ) 

Wend

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************
Sub DisplayOutput( strWinRMXml )
 Dim xmlFile, xslFile
 Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" ) 
 Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
 xmlFile.LoadXml( strWinRMXml )
 xslFile.Load( "WsmTxt.xsl" )
 Wscript.Echo xmlFile.TransformNode( xslFile ) 
End Sub
```



## <a name="requirements"></a><span data-ttu-id="86019-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86019-122">Requirements</span></span>



| <span data-ttu-id="86019-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86019-123">Requirement</span></span> | <span data-ttu-id="86019-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="86019-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86019-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86019-125">Minimum supported client</span></span><br/> | <span data-ttu-id="86019-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86019-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="86019-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86019-127">Minimum supported server</span></span><br/> | <span data-ttu-id="86019-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86019-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="86019-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="86019-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="86019-130"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="86019-130"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="86019-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="86019-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86019-132"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="86019-132"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="86019-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86019-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="86019-134"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="86019-134"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="86019-135">DLL</span><span class="sxs-lookup"><span data-stu-id="86019-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86019-136"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86019-136"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="86019-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86019-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86019-138">**Énumérateur**</span><span class="sxs-lookup"><span data-stu-id="86019-138">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="86019-139">Énumération ou liste de toutes les instances d’une ressource</span><span class="sxs-lookup"><span data-stu-id="86019-139">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

 





