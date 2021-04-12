---
title: Constantes d’énumération (WSManDisp. h)
description: L’énumération contient des constantes, telles qu’elles sont répertoriées dans la liste suivante, utilisées dans le paramètre flags par des appels à l’énumération de session. Enumerate et IWSManSession.
ms.assetid: c0f2763b-a549-43d5-84a6-8cebf33a1ea2
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagReturnObject
- WSManFlagNonXmlText
- EnumerationFlagReturnEPR
- WSManFlagReturnObjectAndEPR
- WSManFlagHierarchyDeep
- WSManFlagHierarchyShallow
- WSManFlagHierarchyDeepBasePropsOnly
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422f688fea992ee2d9b1d0d25af00a1d24ad798
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384267"
---
# <a name="enumeration-constants"></a><span data-ttu-id="ce434-103">Constantes d’énumération</span><span class="sxs-lookup"><span data-stu-id="ce434-103">Enumeration Constants</span></span>

<span data-ttu-id="ce434-104">L’énumération **\_ \_ WSManEnumFlags** contient des constantes, telles qu’elles sont répertoriées dans la liste suivante, utilisées dans le paramètre *Flags* par des appels à [**session. Enumerate**](session-enumerate.md) et [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="ce434-104">The **\_\_WSManEnumFlags** enumeration contains constants, as listed in the following list, used in the *flags* parameter by calls to [**Session.Enumerate**](session-enumerate.md) and [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

<span data-ttu-id="ce434-105">Sachez que **WSManFlagReturnObject** et **WSManFlagHierarchyDeep** sont la valeur par défaut si le paramètre *Flags* n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="ce434-105">Be aware that **WSManFlagReturnObject** and **WSManFlagHierarchyDeep** are the default if the *flags* parameter is not specified.</span></span>

<dl> <dt>

<span data-ttu-id="ce434-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span><span class="sxs-lookup"><span data-stu-id="ce434-106"><span id="WSManFlagReturnObject"></span><span id="wsmanflagreturnobject"></span><span id="WSMANFLAGRETURNOBJECT"></span>**WSManFlagReturnObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce434-107">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ce434-107">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="ce434-108">Les lots contiennent les instances XML demandées.</span><span class="sxs-lookup"><span data-stu-id="ce434-108">Batches contain the requested XML instances.</span></span> <span data-ttu-id="ce434-109">Il s’agit de la valeur par défaut pour le paramètre flag.</span><span class="sxs-lookup"><span data-stu-id="ce434-109">This is the default value for the flag parameter.</span></span>

<span data-ttu-id="ce434-110">La méthode de script associée est [**WSMan. EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) et la méthode C++ est [**IWSManEx. EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span><span class="sxs-lookup"><span data-stu-id="ce434-110">The associated scripting method is [**WSMan.EnumerationFlagReturnObject**](wsman-enumerationflagreturnobject.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObject**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobject).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce434-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span><span class="sxs-lookup"><span data-stu-id="ce434-111"><span id="WSManFlagNonXmlText"></span><span id="wsmanflagnonxmltext"></span><span id="WSMANFLAGNONXMLTEXT"></span>**WSManFlagNonXmlText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce434-112">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="ce434-112">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="ce434-113">Cet indicateur contrôle la manière dont le paramètre de *filtre* dans l’appel à [**session. Enumerate**](session-enumerate.md) est interprété par WinRM.</span><span class="sxs-lookup"><span data-stu-id="ce434-113">This flag controls how the *filter* parameter in the call to [**Session.Enumerate**](session-enumerate.md) is interpreted by WinRM.</span></span>

<span data-ttu-id="ce434-114">Le format du filtre peut être un fragment XML ou une chaîne de texte brut.</span><span class="sxs-lookup"><span data-stu-id="ce434-114">The format of the filter may be an XML fragment or a string of plain text.</span></span> <span data-ttu-id="ce434-115">Le format est déterminé par le [*dialecte de filtre*](windows-remote-management-glossary.md) du [*filtre*](windows-remote-management-glossary.md) utilisé dans l’appel à [**session. Enumerate**](session-enumerate.md) ou [**IWSManSession :: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), qui est spécifique à l’opération effectuée.</span><span class="sxs-lookup"><span data-stu-id="ce434-115">The format is determined by the [*filter dialect*](windows-remote-management-glossary.md) of the [*filter*](windows-remote-management-glossary.md) used in the call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate), which is specific to the operation performed.</span></span>

<span data-ttu-id="ce434-116">Si le paramètre de *dialecte* n’est pas spécifié, WinRM tente de déterminer le dialecte en fonction du premier caractère du filtre.</span><span class="sxs-lookup"><span data-stu-id="ce434-116">If the *dialect* parameter is not specified, WinRM attempts to determine the dialect based on the first character of the filter.</span></span> <span data-ttu-id="ce434-117">Si le premier caractère est <, mais que le filtre n’est pas en fait un fragment XML, cet indicateur doit être défini.</span><span class="sxs-lookup"><span data-stu-id="ce434-117">If the first character is <, but the filter is not actually an XML fragment, then this flag should be set.</span></span> <span data-ttu-id="ce434-118">Par exemple, un filtre au format suivant nécessite que vous dédéfinissez **WSManFlagNonXmlText** pour que le filtre soit correctement interprété :</span><span class="sxs-lookup"><span data-stu-id="ce434-118">For example, a filter in the following format requires that you set **WSManFlagNonXmlText** so that the filter is correctly interpreted:</span></span>

`<25 && > 1`

<span data-ttu-id="ce434-119">Si le filtre est un fragment XML, cet indicateur n’est pas nécessaire, car le fragment commence par <, que WinRM interprète correctement comme XML.</span><span class="sxs-lookup"><span data-stu-id="ce434-119">If the filter is an XML fragment, then this flag is not required because the fragment starts with <, which WinRM correctly interprets as XML.</span></span> <span data-ttu-id="ce434-120">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="ce434-120">For example,</span></span>

`<filter>select * from aDataStructure</filter>`

<span data-ttu-id="ce434-121">Si le filtre est en texte brut qui ne commence pas par <, cet indicateur n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ce434-121">If the filter is in plain text that does not start with <, then this flag is not required.</span></span> <span data-ttu-id="ce434-122">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="ce434-122">For example,</span></span>

`select * from aDataStructure`

<span data-ttu-id="ce434-123">La méthode de script associée est [**WSMan. EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) et la méthode C++ est [**IWSManEx. EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span><span class="sxs-lookup"><span data-stu-id="ce434-123">The associated scripting method is [**WSMan.EnumerationFlagNonXmlText**](wsman-enumerationflagnonxmltext.md) and the C++ method is [**IWSManEx.EnumerationFlagNonXmlText**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagnonxmltext).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce434-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span><span class="sxs-lookup"><span data-stu-id="ce434-124"><span id="EnumerationFlagReturnEPR"></span><span id="enumerationflagreturnepr"></span><span id="ENUMERATIONFLAGRETURNEPR"></span>**EnumerationFlagReturnEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce434-125">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="ce434-125">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="ce434-126">Les lots contiennent des références de point de terminaison (ERP) pour les instances XML correspondantes, mais pas les instances réelles.</span><span class="sxs-lookup"><span data-stu-id="ce434-126">Batches contain endpoint references (EPRs) for the corresponding XML instances, but not the actual instances.</span></span>

<span data-ttu-id="ce434-127">La méthode de script associée est [**WSMan. EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) et la méthode C++ est [**IWSManEx. EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span><span class="sxs-lookup"><span data-stu-id="ce434-127">The associated scripting method is [**WSMan.EnumerationFlagReturnEPR**](wsman-enumerationflagreturnepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce434-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span><span class="sxs-lookup"><span data-stu-id="ce434-128"><span id="WSManFlagReturnObjectAndEPR"></span><span id="wsmanflagreturnobjectandepr"></span><span id="WSMANFLAGRETURNOBJECTANDEPR"></span>**WSManFlagReturnObjectAndEPR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce434-129">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="ce434-129">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="ce434-130">Les lots contiennent à la fois les instances XML demandées et les ERP correspondants contenus dans un élément [*WSMan : items*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="ce434-130">Batches contain both the requested XML instances and the corresponding EPRs contained in a [*wsman:Items*](windows-remote-management-glossary.md) element.</span></span>

<span data-ttu-id="ce434-131">La méthode de script associée est [**WSMan. EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) et la méthode C++ est [**IWSManEx. EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span><span class="sxs-lookup"><span data-stu-id="ce434-131">The associated scripting method is [**WSMan.EnumerationFlagReturnObjectAndEPR**](wsman-enumerationflagreturnobjectandepr.md) and the C++ method is [**IWSManEx.EnumerationFlagReturnObjectAndEPR**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflagreturnobjectandepr).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce434-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span><span class="sxs-lookup"><span data-stu-id="ce434-132"><span id="WSManFlagHierarchyDeep"></span><span id="wsmanflaghierarchydeep"></span><span id="WSMANFLAGHIERARCHYDEEP"></span>**WSManFlagHierarchyDeep**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce434-133">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="ce434-133">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="ce434-134">Les instances de classe dérivée sont incluses et sont représentées en fonction de leurs schémas réels.</span><span class="sxs-lookup"><span data-stu-id="ce434-134">Derived class instances are included and are represented according to their actual schemas.</span></span>

<span data-ttu-id="ce434-135">La méthode de script associée est [**WSMan. EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) et la méthode C++ est [**IWSManEx. EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span><span class="sxs-lookup"><span data-stu-id="ce434-135">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeep**](wsman-enumerationflaghierarchydeep.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeep**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeep).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce434-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span><span class="sxs-lookup"><span data-stu-id="ce434-136"><span id="WSManFlagHierarchyShallow"></span><span id="wsmanflaghierarchyshallow"></span><span id="WSMANFLAGHIERARCHYSHALLOW"></span>**WSManFlagHierarchyShallow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce434-137">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="ce434-137">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="ce434-138">Les instances de classes dérivées sont exclues.</span><span class="sxs-lookup"><span data-stu-id="ce434-138">Derived class instances are excluded.</span></span> <span data-ttu-id="ce434-139">Seules les instances du type demandé sont affichées.</span><span class="sxs-lookup"><span data-stu-id="ce434-139">Only instances of the requested type are shown.</span></span>

<span data-ttu-id="ce434-140">La méthode de script associée est [**WSMan. EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) et la méthode C++ est [**IWSManEx. EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span><span class="sxs-lookup"><span data-stu-id="ce434-140">The associated scripting method is [**WSMan.EnumerationFlagHierarchyShallow**](wsman-enumerationflaghierarchyshallow.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyShallow**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchyshallow).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce434-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span><span class="sxs-lookup"><span data-stu-id="ce434-141"><span id="WSManFlagHierarchyDeepBasePropsOnly"></span><span id="wsmanflaghierarchydeepbasepropsonly"></span><span id="WSMANFLAGHIERARCHYDEEPBASEPROPSONLY"></span>**WSManFlagHierarchyDeepBasePropsOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce434-142">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="ce434-142">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="ce434-143">Les instances de classe dérivée sont incluses et sont représentées en fonction du schéma de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="ce434-143">Derived class instances are included and are represented according to the base class schema.</span></span> <span data-ttu-id="ce434-144">Les propriétés définies dans la classe dérivée ne sont pas affichées.</span><span class="sxs-lookup"><span data-stu-id="ce434-144">Properties defined in the derived class are not shown.</span></span>

<span data-ttu-id="ce434-145">La méthode de script associée est [**WSMan. EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) et la méthode C++ est [**IWSManEx. EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span><span class="sxs-lookup"><span data-stu-id="ce434-145">The associated scripting method is [**WSMan.EnumerationFlagHierarchyDeepBasePropsOnly**](wsman-enumerationflaghierarchydeepbasepropsonly.md) and the C++ method is [**IWSManEx.EnumerationFlagHierarchyDeepBasePropsOnly**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-enumerationflaghierarchydeepbasepropsonly).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce434-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce434-146">Requirements</span></span>



| <span data-ttu-id="ce434-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce434-147">Requirement</span></span> | <span data-ttu-id="ce434-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce434-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce434-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce434-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ce434-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce434-150">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ce434-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce434-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ce434-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce434-152">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ce434-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce434-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce434-154"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce434-154"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce434-155">MIDL</span><span class="sxs-lookup"><span data-stu-id="ce434-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ce434-156"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ce434-156"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce434-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce434-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce434-158">Constantes et énumérations WinRM</span><span class="sxs-lookup"><span data-stu-id="ce434-158">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="ce434-159">Énumération ou liste de toutes les instances d’une ressource</span><span class="sxs-lookup"><span data-stu-id="ce434-159">Enumerating or Listing All the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="ce434-160">Interrogation d’instances spécifiques d’une ressource</span><span class="sxs-lookup"><span data-stu-id="ce434-160">Querying for Specific Instances of a Resource</span></span>](querying-for-specific-instances-of-a-resource.md)
</dt> </dl>

 

 





