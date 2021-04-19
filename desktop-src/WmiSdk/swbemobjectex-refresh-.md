---
description: Met à jour les données pour les objets qui ont des données fournies par un fournisseur de performances, telles que les classes de compteur de performance. Vous pouvez obtenir des données mises à jour plus rapidement et sans appel à SWbemServices. obtenir \_ .
ms.assetid: 6aeaa336-fb98-4eda-b746-fc958198d8ae
ms.tgt_platform: multiple
title: Méthode SWbemObjectEx.Refresh_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
- ISWbemObjectEx.Refresh_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 904e2b7f9b256596555c8396a699220108d4f37b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527803"
---
# <a name="swbemobjectexrefresh_-method"></a><span data-ttu-id="01f4b-104">SWbemObjectEx. Refresh, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="01f4b-104">SWbemObjectEx.Refresh\_ method</span></span>

<span data-ttu-id="01f4b-105">La **méthode \_ Refresh** de [**SWbemObjectEx**](swbemobjectex.md) met à jour les données pour les objets qui ont des données fournies par un fournisseur de performances, telles que les [classes de compteur de performance](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span><span class="sxs-lookup"><span data-stu-id="01f4b-105">The **Refresh\_** method of [**SWbemObjectEx**](swbemobjectex.md) updates the data for objects that have data supplied by a performance provider, such as the [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="01f4b-106">Vous pouvez obtenir des données mises à jour plus rapidement et sans appel à [**SWbemServices \_ . obtenir**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="01f4b-106">You can obtain updated data more quickly and without a call to [**SWbemServices.Get\_**](swbemservices-get.md).</span></span>

<span data-ttu-id="01f4b-107">Pour plus d’informations sur cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="01f4b-107">For more information about this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="01f4b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01f4b-108">Syntax</span></span>


```VB
SWbemObjectEx.Refresh_( _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="01f4b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01f4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01f4b-110">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="01f4b-110">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01f4b-111">Indicateurs d’opération réservée qui, s’ils sont spécifiés, doivent avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="01f4b-111">Reserved operation flags which, if specified, must be 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="01f4b-112">*objWbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="01f4b-112">*objWbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="01f4b-113">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui définit le contexte de l’opération.</span><span class="sxs-lookup"><span data-stu-id="01f4b-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that sets context for the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01f4b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="01f4b-114">Return value</span></span>

<span data-ttu-id="01f4b-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="01f4b-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01f4b-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="01f4b-116">Error codes</span></span>

<span data-ttu-id="01f4b-117">Une fois la méthode **Refresh \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="01f4b-117">After completion of the **Refresh\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="01f4b-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="01f4b-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="01f4b-119">Le fournisseur a échoué en interne, même si l’opération est valide.</span><span class="sxs-lookup"><span data-stu-id="01f4b-119">The provider failed internally, even though the operation was valid.</span></span>

</dd> <dt>

<span data-ttu-id="01f4b-120">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="01f4b-120">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="01f4b-121">Le format demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="01f4b-121">The requested format was not found.</span></span>

</dd> <dt>

<span data-ttu-id="01f4b-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="01f4b-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="01f4b-123">Un des paramètres de l'appel n'est pas correct.</span><span class="sxs-lookup"><span data-stu-id="01f4b-123">One of the parameters to the call is not correct.</span></span>

</dd> <dt>

<span data-ttu-id="01f4b-124">**wbemErrRefresherBusy** -2147749975 (0x80041057)</span><span class="sxs-lookup"><span data-stu-id="01f4b-124">**wbemErrRefresherBusy** - 2147749975 (0x80041057)</span></span>
</dt> <dd>

<span data-ttu-id="01f4b-125">L'actualisateur est occupé par une autre opération.</span><span class="sxs-lookup"><span data-stu-id="01f4b-125">The refresher is busy with another operation.</span></span>

</dd> <dt>

<span data-ttu-id="01f4b-126">**wbemPartialResults** -2147745808 (0x80040010)</span><span class="sxs-lookup"><span data-stu-id="01f4b-126">**wbemPartialResults** - 2147745808 (0x80040010)</span></span>
</dt> <dd>

<span data-ttu-id="01f4b-127">Les objets, les énumérateurs ou les actualisateurs imbriqués n’ont pas tous été mis à jour.</span><span class="sxs-lookup"><span data-stu-id="01f4b-127">Not all of the objects, enumerators, or nested refreshers were successfully updated.</span></span> <span data-ttu-id="01f4b-128">Ce retour n’est pas une erreur, mais indique que l’opération n’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="01f4b-128">This return is not an error but an indication that the operation was incomplete.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="01f4b-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="01f4b-129">Examples</span></span>

<span data-ttu-id="01f4b-130">L’exemple de code de script suivant montre comment obtenir des compteurs de performances bruts et cuisinés pour le processus système.</span><span class="sxs-lookup"><span data-stu-id="01f4b-130">The following script code example shows how to obtain both raw and cooked performance counters for the system process.</span></span> <span data-ttu-id="01f4b-131">Les objets sont actualisés toutes les deux secondes et les propriétés affichées.</span><span class="sxs-lookup"><span data-stu-id="01f4b-131">The objects are refreshed every two seconds and the properties displayed.</span></span>


```VB
' Get the performance counter instance for the System process
set PerfRaw = GetObject( _
    "winmgmts:win32_perfrawdata_perfproc_process.name='system'")
set PerfCooked = GetObject( _
    "winmgmts:win32_perfformatteddata_perfproc_process.name='system'")

' Display some properties in a loop
for I = 1 to 5
    Wscript.Echo "HandleCount = "& PerfRaw.HandleCount & _
         " Raw ThreadCount = " & PerfRaw.ThreadCount & _
        " Cooked ThreadCount = " & PerfCooked.ThreadCount
    
    Wscript.Sleep 2000
    
' Refresh the objects
    PerfRaw.Refresh_
    PerfCooked.Refresh_
next
```



## <a name="requirements"></a><span data-ttu-id="01f4b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01f4b-132">Requirements</span></span>



| <span data-ttu-id="01f4b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01f4b-133">Requirement</span></span> | <span data-ttu-id="01f4b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="01f4b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01f4b-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01f4b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="01f4b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01f4b-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01f4b-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01f4b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="01f4b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01f4b-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01f4b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="01f4b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="01f4b-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="01f4b-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="01f4b-141">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="01f4b-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="01f4b-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="01f4b-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="01f4b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="01f4b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01f4b-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01f4b-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="01f4b-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="01f4b-145">CLSID</span></span><br/>                    | <span data-ttu-id="01f4b-146">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="01f4b-146">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="01f4b-147">IID</span><span class="sxs-lookup"><span data-stu-id="01f4b-147">IID</span></span><br/>                      | <span data-ttu-id="01f4b-148">IID \_ ISWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="01f4b-148">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="01f4b-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01f4b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f4b-150">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="01f4b-150">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="01f4b-151">Analyse des données de performances</span><span class="sxs-lookup"><span data-stu-id="01f4b-151">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> </dl>

 

