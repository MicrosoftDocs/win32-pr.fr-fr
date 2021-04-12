---
title: Enumerator. ReadItem, méthode (WSManDisp. h)
description: Récupère un élément de la ressource et retourne une représentation XML de l’élément.
ms.assetid: 4280ecb8-2449-41bd-868a-785e8ac3b3d5
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode ReadItem
- Méthode ReadItem Windows Remote Management, objet Enumerator
- Objet Enumerator Windows Remote Management, méthode ReadItem
topic_type:
- apiref
api_name:
- Enumerator.ReadItem
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fda1b31cbc14d4a7474d4de55b572df82a8aaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032632"
---
# <a name="enumeratorreaditem-method"></a><span data-ttu-id="af524-106">Enumerator. ReadItem, méthode</span><span class="sxs-lookup"><span data-stu-id="af524-106">Enumerator.ReadItem method</span></span>

<span data-ttu-id="af524-107">Récupère un élément de la ressource et retourne une représentation XML de l’élément.</span><span class="sxs-lookup"><span data-stu-id="af524-107">Retrieves an item from the resource and returns an XML representation of the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="af524-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af524-108">Syntax</span></span>


```VB
Enumerator.ReadItem( _
  ByVal resource _
)
```



## <a name="parameters"></a><span data-ttu-id="af524-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af524-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af524-110">*resource*</span><span class="sxs-lookup"><span data-stu-id="af524-110">*resource*</span></span> 
</dt> <dd>

<span data-ttu-id="af524-111">URI de l’élément.</span><span class="sxs-lookup"><span data-stu-id="af524-111">The URI of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af524-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af524-112">Return value</span></span>

<span data-ttu-id="af524-113">Représentation XML de l’élément.</span><span class="sxs-lookup"><span data-stu-id="af524-113">The XML representation of the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="af524-114">Notes</span><span class="sxs-lookup"><span data-stu-id="af524-114">Remarks</span></span>

<span data-ttu-id="af524-115">Pour limiter le nombre d’éléments lus, définissez la propriété [**Session.BatchItems**](session-batchitems.md) .</span><span class="sxs-lookup"><span data-stu-id="af524-115">To limit the number of items that are read, set the [**Session.BatchItems**](session-batchitems.md) property.</span></span>

<span data-ttu-id="af524-116">Notez que la libération de l’objet d’énumération nettoie toutes les demandes d’énumération en attente.</span><span class="sxs-lookup"><span data-stu-id="af524-116">Note that the freeing of the enumeration object cleans up any pending enumeration requests.</span></span>

<span data-ttu-id="af524-117">La méthode [**session. Enumerate**](session-enumerate.md) n’obtient pas de collection de la même façon qu’une [requête WMI](/windows/desktop/WmiSdk/querying-wmi), telle que `SELECT * from Win32_LogicalDisk` , retourne une collection dans une [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span><span class="sxs-lookup"><span data-stu-id="af524-117">The [**Session.Enumerate**](session-enumerate.md) method does not obtain a collection in the same way that a [WMI query](/windows/desktop/WmiSdk/querying-wmi), such as `SELECT * from Win32_LogicalDisk`, returns a collection in an [**SWbemObjectSet**](/windows/desktop/WmiSdk/swbemobjectset).</span></span> <span data-ttu-id="af524-118">Pour lire un fichier en tant que flux de texte, vous créez l’objet [TextStream](/previous-versions//312a5kbt(v=vs.85)) de script et appelez la méthode [TextStream. ReadLine](/previous-versions//h7se9d4f(v=vs.85)) pour lire chaque ligne du fichier.</span><span class="sxs-lookup"><span data-stu-id="af524-118">To read a file as a text stream, you create the scripting [TextStream](/previous-versions//312a5kbt(v=vs.85)) object and call the [TextStream.Readline](/previous-versions//h7se9d4f(v=vs.85)) method to read each line of the file.</span></span> <span data-ttu-id="af524-119">De la même façon, vous appelez la méthode **session. Enumerate** pour obtenir un objet [**énumérateur**](enumerator.md) , puis vous appelez la méthode **Enumerator. ReadItem** .</span><span class="sxs-lookup"><span data-stu-id="af524-119">In a similar way, you call the **Session.Enumerate** method to obtain an [**Enumerator**](enumerator.md) object and then call the **Enumerator.ReadItem** method.</span></span> <span data-ttu-id="af524-120">Comme pour la lecture à partir du fichier texte, vous pouvez vérifier la propriété [**Enumerator. AtEndOfStream**](enumerator-atendofstream.md) pour vérifier si vous avez atteint la fin des éléments de données.</span><span class="sxs-lookup"><span data-stu-id="af524-120">As in reading from the text file, you can check the [**Enumerator.AtEndOfStream**](enumerator-atendofstream.md) property to check for whether you have reached the end of the data items.</span></span>

## <a name="examples"></a><span data-ttu-id="af524-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="af524-121">Examples</span></span>

<span data-ttu-id="af524-122">L’exemple VBScript suivant appelle la méthode [**session. Enumerate**](session-enumerate.md) pour obtenir une liste de tâches planifiées.</span><span class="sxs-lookup"><span data-stu-id="af524-122">The following VBScript example calls the [**Session.Enumerate**](session-enumerate.md) method to obtain a list of scheduled jobs.</span></span> <span data-ttu-id="af524-123">La sous-routine DisplayOutput utilise le fichier de transformation XML (WsmTxt. Xsl) de l’outil en ligne de commande WinRM pour générer les données sous forme de tableau.</span><span class="sxs-lookup"><span data-stu-id="af524-123">The DisplayOutput subroutine uses the Winrm command line tool XML transform file (WsmTxt.xsl) to output the data in a tabular form.</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
              "wmi/root/cimv2/Win32_ScheduledJob"

Set objResultSet = objSession.Enumerate( strResource )
NumOfJobs = 0

While Not objResultSet.AtEndOfStream
    NumOfJobs = NumOfJobs + 1
    DisplayOutput( objResultSet.ReadItem ) 
Wend

Wscript.Echo "There are " & NumOfJobs & " jobs scheduled."

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



## <a name="requirements"></a><span data-ttu-id="af524-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af524-124">Requirements</span></span>



| <span data-ttu-id="af524-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af524-125">Requirement</span></span> | <span data-ttu-id="af524-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="af524-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="af524-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af524-127">Minimum supported client</span></span><br/> | <span data-ttu-id="af524-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af524-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="af524-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af524-129">Minimum supported server</span></span><br/> | <span data-ttu-id="af524-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af524-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="af524-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="af524-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="af524-132"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af524-132"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="af524-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="af524-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="af524-134"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="af524-134"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="af524-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af524-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="af524-136"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af524-136"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af524-137">DLL</span><span class="sxs-lookup"><span data-stu-id="af524-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af524-138"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af524-138"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af524-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af524-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af524-140">**Énumérateur**</span><span class="sxs-lookup"><span data-stu-id="af524-140">**Enumerator**</span></span>](enumerator.md)
</dt> <dt>

[<span data-ttu-id="af524-141">Énumération ou liste de toutes les instances d’une ressource</span><span class="sxs-lookup"><span data-stu-id="af524-141">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> </dl>

 

