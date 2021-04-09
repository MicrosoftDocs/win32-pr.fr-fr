---
description: Retourne une représentation XML d’un objet ou d’une instance. Le fichier texte est mis en forme au format XML spécifié comme indiqué dans WbemObjectTextFormatEnum.
ms.assetid: 98961d94-8360-4ed7-b1b1-20b4fca45d45
ms.tgt_platform: multiple
title: Méthode SWbemObjectEx.GetText_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
- ISWbemObjectEx.GetText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6f174397b1ace85acd90ffe3def6b8122bf8d7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035199"
---
# <a name="swbemobjectexgettext_-method"></a><span data-ttu-id="af40f-104">SWbemObjectEx. GetText, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="af40f-104">SWbemObjectEx.GetText\_ method</span></span>

<span data-ttu-id="af40f-105">La **méthode \_ gettext** de l’objet [**SWBEMOBJECTEX**](swbemobjectex.md) retourne une représentation XML d’un objet ou d’une instance.</span><span class="sxs-lookup"><span data-stu-id="af40f-105">The **GetText\_** method of the [**SWbemObjectEx**](swbemobjectex.md) object returns an XML representation of an object or instance.</span></span> <span data-ttu-id="af40f-106">Le fichier texte est mis en forme au format XML spécifié comme indiqué dans [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span><span class="sxs-lookup"><span data-stu-id="af40f-106">The text file is formatted in the XML format specified as shown in [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum).</span></span>

<span data-ttu-id="af40f-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="af40f-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="af40f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af40f-108">Syntax</span></span>


```VB
strObj = .GetText_( _
  ByVal iTextFormat, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="af40f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af40f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af40f-110">*iTextFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af40f-110">*iTextFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af40f-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="af40f-111">Required.</span></span> <span data-ttu-id="af40f-112">Valeur de [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) qui spécifie le format XML obtenu.</span><span class="sxs-lookup"><span data-stu-id="af40f-112">A value from [**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum) that specifies the resulting XML format.</span></span>

</dd> <dt>

<span data-ttu-id="af40f-113">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="af40f-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="af40f-114">Indicateurs d’opération réservée.</span><span class="sxs-lookup"><span data-stu-id="af40f-114">Reserved operation flags.</span></span> <span data-ttu-id="af40f-115">La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="af40f-115">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="af40f-116">*objWbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="af40f-116">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="af40f-117">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui définit le contexte de l’opération.</span><span class="sxs-lookup"><span data-stu-id="af40f-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span> <span data-ttu-id="af40f-118">La valeur par défaut est null.</span><span class="sxs-lookup"><span data-stu-id="af40f-118">The default is null.</span></span> <span data-ttu-id="af40f-119">Pour plus d’informations sur les paires nom/valeur autorisées, consultez la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="af40f-119">For more information about the name/value pairs permitted, see Remarks below.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af40f-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af40f-120">Return value</span></span>

<span data-ttu-id="af40f-121">Cette méthode n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="af40f-121">This method has no return values.</span></span>

## <a name="error-codes"></a><span data-ttu-id="af40f-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="af40f-122">Error codes</span></span>

<span data-ttu-id="af40f-123">Une fois la méthode **gettext \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="af40f-123">After completion of the **GetText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="af40f-124">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="af40f-124">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="af40f-125">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="af40f-125">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="af40f-126">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="af40f-126">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="af40f-127">Le format demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="af40f-127">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="af40f-128">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="af40f-128">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="af40f-129">Un des paramètres de l'appel n'est pas correct.</span><span class="sxs-lookup"><span data-stu-id="af40f-129">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="af40f-130">**wbemErrCriticalError** -2147749898 (0x8004100A)</span><span class="sxs-lookup"><span data-stu-id="af40f-130">**wbemErrCriticalError** - 2147749898 (0x8004100A)</span></span>
</dt> <dd>

<span data-ttu-id="af40f-131">Une erreur interne, critique et inattendue est survenue.</span><span class="sxs-lookup"><span data-stu-id="af40f-131">An internal, critical, and unexpected error occurred.</span></span> <span data-ttu-id="af40f-132">Signalez cette erreur au Support technique Microsoft.</span><span class="sxs-lookup"><span data-stu-id="af40f-132">Report this error to Microsoft Technical Support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="af40f-133">Notes</span><span class="sxs-lookup"><span data-stu-id="af40f-133">Remarks</span></span>

<span data-ttu-id="af40f-134">Lors de la construction de votre [**SWbemNamedValueSet**](swbemnamedvalueset.md), seules les paires nom/valeur suivantes sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="af40f-134">When constructing your [**SWbemNamedValueSet**](swbemnamedvalueset.md), only the following name/value pairs are permitted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af40f-135">Nom</span><span class="sxs-lookup"><span data-stu-id="af40f-135">Name</span></span></th>
<th><span data-ttu-id="af40f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="af40f-136">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af40f-137">LocalOnly</span><span class="sxs-lookup"><span data-stu-id="af40f-137">LocalOnly</span></span></td>
<td><span data-ttu-id="af40f-138"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="af40f-138"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="af40f-139">Si la <strong>valeur est true</strong>, seules les propriétés et les méthodes définies localement sont présentes dans le XML résultant.</span><span class="sxs-lookup"><span data-stu-id="af40f-139">If <strong>TRUE</strong>, only locally defined properties and methods are present in the resulting XML.</span></span> <span data-ttu-id="af40f-140">La valeur par défaut est <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="af40f-140">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af40f-141">IncludeQualifiers</span><span class="sxs-lookup"><span data-stu-id="af40f-141">IncludeQualifiers</span></span></td>
<td><span data-ttu-id="af40f-142"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="af40f-142"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="af40f-143">Si la <strong>valeur est true</strong>, les qualificateurs des classes, instances, propriétés et méthodes sont inclus dans le XML résultant.</span><span class="sxs-lookup"><span data-stu-id="af40f-143">If <strong>TRUE</strong>, qualifiers of classes, instances, properties, and methods are included in the resulting XML.</span></span> <span data-ttu-id="af40f-144">La valeur par défaut est <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="af40f-144">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af40f-145">PathLevel</span><span class="sxs-lookup"><span data-stu-id="af40f-145">PathLevel</span></span></td>
<td><span data-ttu-id="af40f-146"><strong>VT-I4</strong></span><span class="sxs-lookup"><span data-stu-id="af40f-146"><strong>VT-I4</strong></span></span><br/> <span data-ttu-id="af40f-147">La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="af40f-147">Default is 0 (zero).</span></span> <span data-ttu-id="af40f-148">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="af40f-148">Possible values are:</span></span><br/>
<ul>
<li><span data-ttu-id="af40f-149">0 : un <CLASS> <INSTANCE> élément ou est créé selon que l’objet est une classe ou une instance.</span><span class="sxs-lookup"><span data-stu-id="af40f-149">0: A <CLASS> or <INSTANCE> element is created depending on whether the object is a class or instance.</span></span></li>
<li><span data-ttu-id="af40f-150">1 : un <VALUE.NAMEDOBJECT> élément est généré.</span><span class="sxs-lookup"><span data-stu-id="af40f-150">1: A <VALUE.NAMEDOBJECT> element is generated.</span></span></li>
<li><span data-ttu-id="af40f-151">2 : un <VALUE.OBJECTWITHLOCALPATH> élément est généré.</span><span class="sxs-lookup"><span data-stu-id="af40f-151">2: A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span></li>
<li><span data-ttu-id="af40f-152">3 : un <VALUE.OBJECTWITHPATH> élément est généré.</span><span class="sxs-lookup"><span data-stu-id="af40f-152">3: A <VALUE.OBJECTWITHPATH> element is generated.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af40f-153">ExcludeSystemProperties</span><span class="sxs-lookup"><span data-stu-id="af40f-153">ExcludeSystemProperties</span></span></td>
<td><span data-ttu-id="af40f-154"><strong>VT-BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="af40f-154"><strong>VT-BOOL</strong></span></span><br/> <span data-ttu-id="af40f-155">Si la <strong>valeur est true</strong>, les propriétés système, comme __NAMESPACE, sont exclues de la sortie.</span><span class="sxs-lookup"><span data-stu-id="af40f-155">If <strong>TRUE</strong>, system properties, like __NAMESPACE, are excluded from the output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af40f-156">IncludeClassOrigin</span><span class="sxs-lookup"><span data-stu-id="af40f-156">IncludeClassOrigin</span></span></td>
<td><span data-ttu-id="af40f-157"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="af40f-157"><strong>VT_BOOL</strong></span></span><br/> <span data-ttu-id="af40f-158">Si la <strong>valeur est true</strong>, l’attribut Origin de la classe est défini sur les <PROPERTY> éléments et <METHOD> .</span><span class="sxs-lookup"><span data-stu-id="af40f-158">If <strong>TRUE</strong>, the class origin attribute is set on the <PROPERTY> and <METHOD> elements.</span></span> <span data-ttu-id="af40f-159">La valeur par défaut est <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="af40f-159">The default is <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="af40f-160">Pour plus d’informations sur la création d’un [**SWbemNamedValueSet**](swbemnamedvalueset.md), consultez [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md).</span><span class="sxs-lookup"><span data-stu-id="af40f-160">For more information about creating an [**SWbemNamedValueSet**](swbemnamedvalueset.md), see [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md).</span></span>

## <a name="examples"></a><span data-ttu-id="af40f-161">Exemples</span><span class="sxs-lookup"><span data-stu-id="af40f-161">Examples</span></span>

<span data-ttu-id="af40f-162">Le script suivant montre comment obtenir une représentation XML de la définition de classe [**\_ BIOS Win32**](/windows/desktop/CIMWin32Prov/win32-bios) .</span><span class="sxs-lookup"><span data-stu-id="af40f-162">The following script shows how to obtain an XML representation of the [**Win32\_Bios**](/windows/desktop/CIMWin32Prov/win32-bios) class definition.</span></span> <span data-ttu-id="af40f-163">En spécifiant une instance particulière **du \_ BIOS Win32**, vous pouvez obtenir les données de cet objet en XML.</span><span class="sxs-lookup"><span data-stu-id="af40f-163">By specifying a particular instance of **Win32\_Bios**, you can obtain that object's data in XML.</span></span>


```VB
' Connect to the default namespace (root\cimv2) with the default
' impersonation level ("impersonate") and obtain a Win32_Bios class
' object.
Set obj = GetObject("winmgmts:win32_bios")

' Use the value for the desired XML CIM DTD format. 
XMLDtd = 1
Text = obj.GetText_(XMLDtd)
wscript.echo Text
```



## <a name="requirements"></a><span data-ttu-id="af40f-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af40f-164">Requirements</span></span>



| <span data-ttu-id="af40f-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af40f-165">Requirement</span></span> | <span data-ttu-id="af40f-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="af40f-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af40f-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af40f-167">Minimum supported client</span></span><br/> | <span data-ttu-id="af40f-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="af40f-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="af40f-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af40f-169">Minimum supported server</span></span><br/> | <span data-ttu-id="af40f-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af40f-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="af40f-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="af40f-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="af40f-172"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="af40f-172"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="af40f-173">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="af40f-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="af40f-174"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="af40f-174"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="af40f-175">DLL</span><span class="sxs-lookup"><span data-stu-id="af40f-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af40f-176"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af40f-176"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="af40f-177">CLSID</span><span class="sxs-lookup"><span data-stu-id="af40f-177">CLSID</span></span><br/>                    | <span data-ttu-id="af40f-178">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="af40f-178">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="af40f-179">IID</span><span class="sxs-lookup"><span data-stu-id="af40f-179">IID</span></span><br/>                      | <span data-ttu-id="af40f-180">IID \_ ISWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="af40f-180">IID\_ISWbemObjectEx</span></span><br/>                                                          |



 

