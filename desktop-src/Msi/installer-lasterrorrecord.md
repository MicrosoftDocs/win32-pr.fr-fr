---
description: La méthode LastErrorRecord de l’objet installer retourne un objet record qui contient des paramètres d’erreur pour l’erreur la plus récente de la fonction qui a produit l’enregistrement d’erreur.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Installer. LastErrorRecord, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b368f30b04734b2d253a7d5f2aa64f0d61c930e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530381"
---
# <a name="installerlasterrorrecord-method"></a><span data-ttu-id="b4708-103">Installer. LastErrorRecord, méthode</span><span class="sxs-lookup"><span data-stu-id="b4708-103">Installer.LastErrorRecord method</span></span>

<span data-ttu-id="b4708-104">La méthode **LastErrorRecord** de l’objet [**installer**](installer-object.md) retourne un objet [**Record**](record-object.md) qui contient des paramètres d’erreur pour l’erreur la plus récente de la fonction qui a produit l’enregistrement d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b4708-104">The **LastErrorRecord** method of the [**Installer**](installer-object.md) object returns a [**Record**](record-object.md) object that contains error parameters for the most recent error from the function that produced the error record.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4708-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4708-105">Syntax</span></span>


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a><span data-ttu-id="b4708-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4708-106">Parameters</span></span>

<span data-ttu-id="b4708-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b4708-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4708-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4708-108">Return value</span></span>

<span data-ttu-id="b4708-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b4708-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4708-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b4708-110">Remarks</span></span>

<span data-ttu-id="b4708-111">L’objet [**enregistrement**](record-object.md) est réinitialisé après l’exécution de cette fonction de toute fonction qui génère un enregistrement d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b4708-111">The [**Record**](record-object.md) object is reset after the execution of this function of any function that generates an error record.</span></span>

<span data-ttu-id="b4708-112">Seules les fonctions désignées suivantes génèrent un enregistrement d’erreur :</span><span class="sxs-lookup"><span data-stu-id="b4708-112">Only the following designated functions generate an error record:</span></span>

-   [<span data-ttu-id="b4708-113">**OpenDatabase, méthode (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="b4708-113">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="b4708-114">**Commit**</span><span class="sxs-lookup"><span data-stu-id="b4708-114">**Commit**</span></span>](database-commit.md)
-   [<span data-ttu-id="b4708-115">**OpenView**</span><span class="sxs-lookup"><span data-stu-id="b4708-115">**OpenView**</span></span>](database-openview.md)
-   [<span data-ttu-id="b4708-116">**Importer**</span><span class="sxs-lookup"><span data-stu-id="b4708-116">**Import**</span></span>](database-import.md)
-   [<span data-ttu-id="b4708-117">**Exporter**</span><span class="sxs-lookup"><span data-stu-id="b4708-117">**Export**</span></span>](database-export.md)
-   [<span data-ttu-id="b4708-118">**Fusion**</span><span class="sxs-lookup"><span data-stu-id="b4708-118">**Merge**</span></span>](database-merge.md)
-   [<span data-ttu-id="b4708-119">**GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="b4708-119">**GenerateTransform**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="b4708-120">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="b4708-120">**ApplyTransform**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="b4708-121">**Execute**</span><span class="sxs-lookup"><span data-stu-id="b4708-121">**Execute**</span></span>](view-execute.md)
-   [<span data-ttu-id="b4708-122">**Modifier**</span><span class="sxs-lookup"><span data-stu-id="b4708-122">**Modify**</span></span>](view-modify.md)
-   [<span data-ttu-id="b4708-123">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="b4708-123">**SetStream**</span></span>](record-setstream.md)
-   [<span data-ttu-id="b4708-124">**SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="b4708-124">**SummaryInformation**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="b4708-125">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="b4708-125">**SourcePath**</span></span>](session-sourcepath.md)
-   [<span data-ttu-id="b4708-126">**TargetPath**</span><span class="sxs-lookup"><span data-stu-id="b4708-126">**TargetPath**</span></span>](session-targetpath.md)
-   [<span data-ttu-id="b4708-127">**ComponentCurrentState**</span><span class="sxs-lookup"><span data-stu-id="b4708-127">**ComponentCurrentState**</span></span>](session-componentcurrentstate.md)
-   [<span data-ttu-id="b4708-128">**ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="b4708-128">**ComponentRequestState**</span></span>](session-componentrequeststate.md)
-   [<span data-ttu-id="b4708-129">**FeatureCurrentState**</span><span class="sxs-lookup"><span data-stu-id="b4708-129">**FeatureCurrentState**</span></span>](session-featurecurrentstate.md)
-   [<span data-ttu-id="b4708-130">**FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="b4708-130">**FeatureRequestState**</span></span>](session-featurerequeststate.md)
-   [<span data-ttu-id="b4708-131">**FeatureCost**</span><span class="sxs-lookup"><span data-stu-id="b4708-131">**FeatureCost**</span></span>](session-featurecost.md)
-   [<span data-ttu-id="b4708-132">**FeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="b4708-132">**FeatureValidStates**</span></span>](session-featurevalidstates.md)
-   [<span data-ttu-id="b4708-133">**SetInstallLevel**</span><span class="sxs-lookup"><span data-stu-id="b4708-133">**SetInstallLevel**</span></span>](session-setinstalllevel.md)

<span data-ttu-id="b4708-134">L’exemple suivant dans VBScript utilise un appel à [**OpenDatabase**](installer-opendatabase.md) pour montrer comment obtenir des informations d’erreur étendues à partir de l’une des méthodes ou propriétés qui prennent en charge la méthode **LastErrorRecord** .</span><span class="sxs-lookup"><span data-stu-id="b4708-134">The following sample in VBScript uses a call to [**OpenDatabase**](installer-opendatabase.md) to show how to obtain extended error information from one of the methods or properties that support the **LastErrorRecord** method.</span></span> <span data-ttu-id="b4708-135">L’exemple construit un message d’erreur lorsque la méthode **OpenDatabase** échoue.</span><span class="sxs-lookup"><span data-stu-id="b4708-135">The sample constructs an error message when the **OpenDatabase** method fails.</span></span> <span data-ttu-id="b4708-136">L’objet **Err** est utilisé pour déterminer si une erreur a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="b4708-136">The **Err** object is used to determine whether an error was encountered.</span></span>


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a><span data-ttu-id="b4708-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4708-137">Requirements</span></span>



| <span data-ttu-id="b4708-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4708-138">Requirement</span></span> | <span data-ttu-id="b4708-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4708-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4708-140">Version</span><span class="sxs-lookup"><span data-stu-id="b4708-140">Version</span></span><br/> | <span data-ttu-id="b4708-141">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b4708-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b4708-142">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b4708-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b4708-143">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4708-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="b4708-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b4708-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="b4708-145"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4708-145"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="b4708-146">IID</span><span class="sxs-lookup"><span data-stu-id="b4708-146">IID</span></span><br/>     | <span data-ttu-id="b4708-147">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="b4708-147">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




