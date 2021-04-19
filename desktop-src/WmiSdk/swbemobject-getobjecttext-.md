---
description: La \_ méthode GetObjectText de l’objet SWbemObject retourne un rendu textuel de l’objet.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: Méthode SWbemObject.GetObjectText_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2447d8361d02626e1f5ea8fae1928ffd563d52ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524562"
---
# <a name="swbemobjectgetobjecttext_-method"></a><span data-ttu-id="23781-103">SWbemObject. GetObjectText, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="23781-103">SWbemObject.GetObjectText\_ method</span></span>

<span data-ttu-id="23781-104">La **méthode \_ GetObjectText** de l’objet [**SWbemObject**](swbemobject.md) retourne un rendu textuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="23781-104">The **GetObjectText\_** method of the [**SWbemObject**](swbemobject.md) object returns a textual rendering of the object.</span></span> <span data-ttu-id="23781-105">Cet objet peut être utilisé pour afficher le contenu d’un objet.</span><span class="sxs-lookup"><span data-stu-id="23781-105">This object can be used to display an object's contents.</span></span> <span data-ttu-id="23781-106">À l’heure actuelle, seule la syntaxe MOF est prise en charge comme format de sortie.</span><span class="sxs-lookup"><span data-stu-id="23781-106">Currently, only the MOF syntax is supported as an output format.</span></span> <span data-ttu-id="23781-107">Notez que le texte MOF retourné ne contient pas toutes les informations relatives à l’objet. le texte MOF contient uniquement des informations suffisantes pour permettre au compilateur MOF de recréer l’objet d’origine.</span><span class="sxs-lookup"><span data-stu-id="23781-107">Notice that the MOF text returned does not contain all the information about the object; the MOF text contains only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="23781-108">Par exemple, il n’y a pas d’informations sur les qualificateurs propagés ou les propriétés de la classe parente.</span><span class="sxs-lookup"><span data-stu-id="23781-108">For instance, there is no information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="23781-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="23781-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="23781-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23781-110">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="23781-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23781-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23781-112">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="23781-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="23781-113">Réservé et doit avoir la valeur 0 (zéro) si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="23781-113">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23781-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23781-114">Return value</span></span>

<span data-ttu-id="23781-115">En cas de réussite, cette méthode retourne une chaîne qui contient le texte de sortie.</span><span class="sxs-lookup"><span data-stu-id="23781-115">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="23781-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="23781-116">Error codes</span></span>

<span data-ttu-id="23781-117">À la fin de la **méthode \_ GetObjectText** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="23781-117">After the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="23781-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="23781-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="23781-119">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="23781-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="23781-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="23781-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="23781-121">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="23781-121">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="23781-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="23781-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="23781-123">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="23781-123">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="23781-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="23781-124">Examples</span></span>

<span data-ttu-id="23781-125">Le code suivant, extrait de la [liste de la définition d’une classe WMI dans](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) l’exemple de code VBScript au format MOF dans la Galerie TechNet, récupère et affiche la représentation textuelle d’une définition de classe WMI dans la syntaxe mof (format MOF).</span><span class="sxs-lookup"><span data-stu-id="23781-125">The following code, taken from the [List the Definition of a WMI Class in MOF Format](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) VBScript code sample in the TechNet Gallery, retrieves and displays the textual representation of a WMI class definition in MOF (Managed Object Format) syntax.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a><span data-ttu-id="23781-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23781-126">Requirements</span></span>



| <span data-ttu-id="23781-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23781-127">Requirement</span></span> | <span data-ttu-id="23781-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="23781-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23781-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23781-129">Minimum supported client</span></span><br/> | <span data-ttu-id="23781-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="23781-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="23781-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23781-131">Minimum supported server</span></span><br/> | <span data-ttu-id="23781-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="23781-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="23781-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="23781-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="23781-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="23781-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="23781-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="23781-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="23781-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23781-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23781-137">DLL</span><span class="sxs-lookup"><span data-stu-id="23781-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23781-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23781-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="23781-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="23781-139">CLSID</span></span><br/>                    | <span data-ttu-id="23781-140">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="23781-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="23781-141">IID</span><span class="sxs-lookup"><span data-stu-id="23781-141">IID</span></span><br/>                      | <span data-ttu-id="23781-142">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="23781-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




