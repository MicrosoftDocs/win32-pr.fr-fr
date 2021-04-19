---
description: L’API de script pour WMI contient des indicateurs, des valeurs communes et des codes d’erreur.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Constantes d’API de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518396"
---
# <a name="scripting-api-constants"></a><span data-ttu-id="cbb45-103">Constantes d’API de script</span><span class="sxs-lookup"><span data-stu-id="cbb45-103">Scripting API Constants</span></span>

<span data-ttu-id="cbb45-104">WMI utilise plusieurs types de constantes dans le paramètre *IFlags* des appels de méthode dans l' [API de script pour WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="cbb45-104">WMI uses several types of constants in the *iflags* parameter of method calls in the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span>

<span data-ttu-id="cbb45-105">Visual Basic applications peuvent inclure la bibliothèque de types pour l’API de script, wbemdisp. tlb.</span><span class="sxs-lookup"><span data-stu-id="cbb45-105">Visual Basic applications can include the type library for the scripting API, Wbemdisp.tlb.</span></span> <span data-ttu-id="cbb45-106">Les scripts ne peuvent pas accéder aux constantes de la bibliothèque de types, sauf s’ils utilisent les <REFERENCE> <OBJECT> balises ou du format de fichier XML WSH (Windows Script Host), comme décrit dans [utilisation de la bibliothèque de types de scripts WMI](using-the-wmi-scripting-type-library.md).</span><span class="sxs-lookup"><span data-stu-id="cbb45-106">Scripts are unable to access constants in the type library unless they use the <REFERENCE> or <OBJECT> tags from the Windows Script Host (WSH) XML file format as described in [Using the WMI Scripting Type Library](using-the-wmi-scripting-type-library.md).</span></span> <span data-ttu-id="cbb45-107">Dans le cas contraire, un script doit utiliser la valeur de la constante.</span><span class="sxs-lookup"><span data-stu-id="cbb45-107">Otherwise, a script must use the value of the constant.</span></span>

## <a name="constants"></a><span data-ttu-id="cbb45-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="cbb45-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cbb45-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-109"><span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-110">Définissez les niveaux d’authentification de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cbb45-110">Define the security authentication levels.</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-111"><span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-112">Définir le mode d’exécution d’une opération d’écriture dans une classe ou une instance.</span><span class="sxs-lookup"><span data-stu-id="cbb45-112">Define how a write operation to a class or an instance is carried out.</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-113"><span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-114">Définissez les types CIM valides d’une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="cbb45-114">Define the valid CIM types of a property value.</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-115"><span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-116">Définissez les paramètres pour la comparaison d’objets et sont utilisés par [**SWbemObject \_ . CompareTo**](swbemobject-compareto-.md).</span><span class="sxs-lookup"><span data-stu-id="cbb45-116">Define the settings for object comparison and are used by [**SWbemObject.CompareTo\_**](swbemobject-compareto-.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-117"><span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-118">Définit un indicateur de sécurité qui est utilisé en tant que paramètre dans les appels à la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) lorsqu’une connexion à WMI sur un ordinateur distant échoue.</span><span class="sxs-lookup"><span data-stu-id="cbb45-118">Defines a security flag that is used as a parameter in calls to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method when a connection to WMI on a remote machine is failing.</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-119"><span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-120">Définissez les erreurs qui peuvent être retournées par l' [API de script pour les appels WMI](scripting-api-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="cbb45-120">Define the errors that may be returned by [Scripting API for WMI](scripting-api-for-wmi.md) calls.</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-121"><span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-122">Définit les constantes utilisées par [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)et [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="cbb45-122">Defines constants that are used by [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md), and [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-123"><span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-124">Définissez les niveaux d’emprunt d’identité de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cbb45-124">Define the security impersonation levels.</span></span> <span data-ttu-id="cbb45-125">Ces constantes sont utilisées avec [**SWbemSecurity**](swbemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="cbb45-125">These constants are used with [**SWbemSecurity**](swbemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-126"><span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-127">Définissez les formats de texte d’objet valides à utiliser par [**SWbemObjectEx \_ . GetText**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="cbb45-127">Define the valid object text formats to be used by [**SWbemObjectEx.GetText\_**](swbemobjectex-gettext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-128"><span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-129">Définir des privilèges.</span><span class="sxs-lookup"><span data-stu-id="cbb45-129">Define privileges.</span></span> <span data-ttu-id="cbb45-130">Ces constantes sont utilisées avec [**SWbemSecurity**](swbemsecurity.md) pour accorder les privilèges requis pour certaines opérations.</span><span class="sxs-lookup"><span data-stu-id="cbb45-130">These constants are used with [**SWbemSecurity**](swbemsecurity.md) to grant the privileges required for some operations.</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-131"><span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-132">Définissez la profondeur de l’énumération ou de la requête, qui détermine le nombre d’objets retournés par un appel.</span><span class="sxs-lookup"><span data-stu-id="cbb45-132">Define the depth of enumeration or query, which determines how many objects are returned by a call.</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span><span class="sxs-lookup"><span data-stu-id="cbb45-133"><span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-134">Définit le contenu du texte de l’objet généré et est utilisé par [**SWbemObject \_ . GetObjectText**](swbemobject-getobjecttext-.md).</span><span class="sxs-lookup"><span data-stu-id="cbb45-134">Defines the content of generated object text and is used by [**SWbemObject.GetObjectText\_**](swbemobject-getobjecttext-.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbb45-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span><span class="sxs-lookup"><span data-stu-id="cbb45-135"><span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)</span></span>
</dt> <dd>

<span data-ttu-id="cbb45-136">Définit les constantes de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="cbb45-136">Defines the time-out constants.</span></span> <span data-ttu-id="cbb45-137">Cette constante est utilisée par [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md).</span><span class="sxs-lookup"><span data-stu-id="cbb45-137">This constant is used by [**SWbemEventSource.NextEvent**](swbemeventsource-nextevent.md).</span></span>

</dd> </dl>

## <a name="combining-flags"></a><span data-ttu-id="cbb45-138">Combinaison d’indicateurs</span><span class="sxs-lookup"><span data-stu-id="cbb45-138">Combining Flags</span></span>

<span data-ttu-id="cbb45-139">Vous pouvez combiner des indicateurs pour affecter plusieurs aspects de l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="cbb45-139">You can combine flags to affect more than one aspect of the API call.</span></span>

<span data-ttu-id="cbb45-140">Par exemple, pour créer un [*appel semi-synchrone*](gloss-s.md) , le paramètre *IFlags* dans un appel [**cQuery \_SWbemServices.Exe**](swbemservices-execquery.md) doit contenir deux indicateurs : **WbemFlagReturnImmediately** et **WbemFlagForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="cbb45-140">For example, to create a [*semisynchronous*](gloss-s.md) call, the *iFlags* parameter in an [**SWbemServices.ExecQuery\_**](swbemservices-execquery.md) call must contain two flags: **WbemFlagReturnImmediately** and **WbemFlagForwardOnly**.</span></span> <span data-ttu-id="cbb45-141">La valeur de **WbemFlagReturnImmediately** est 16 et la valeur de **WbemFlagForwardOnly** est 32.</span><span class="sxs-lookup"><span data-stu-id="cbb45-141">The value of **WbemFlagReturnImmediately** is 16 and the value of **WbemFlagForwardOnly** is 32.</span></span> <span data-ttu-id="cbb45-142">Étant donné que les constantes ne sont pas accessibles par leur nom, les valeurs de ces indicateurs sont combinées, produisant une valeur *IFlags* de 48.</span><span class="sxs-lookup"><span data-stu-id="cbb45-142">Because the constants cannot be accessed by name, the values of these flags are combined, producing an *iFlags* value of 48.</span></span>

<span data-ttu-id="cbb45-143">L’exemple de script suivant illustre l’appel.</span><span class="sxs-lookup"><span data-stu-id="cbb45-143">The following script example shows the call.</span></span>


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



<span data-ttu-id="cbb45-144">Tous les indicateurs ne peuvent pas être combinés, car de nombreux sont mutuellement exclusifs et peuvent produire des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="cbb45-144">Not all flags can be combined since many are mutually exclusive and may produce unpredictable results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbb45-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cbb45-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbb45-146">API de script pour WMI</span><span class="sxs-lookup"><span data-stu-id="cbb45-146">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 



