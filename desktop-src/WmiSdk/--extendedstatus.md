---
description: Utilisé pour signaler des informations détaillées sur l’État et l’erreur.
ms.assetid: 6bdff9a8-1a7c-4860-a12e-4d3162964ee4
ms.tgt_platform: multiple
title: Classe __ExtendedStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ExtendedStatus
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: cfc364ac6523aad69e53755d96fe220d0109fab8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539755"
---
# <a name="__extendedstatus-class"></a><span data-ttu-id="8dfcb-103">\_\_ExtendedStatus, classe</span><span class="sxs-lookup"><span data-stu-id="8dfcb-103">\_\_ExtendedStatus class</span></span>

<span data-ttu-id="8dfcb-104">La classe système **\_ \_ ExtendedStatus** est utilisée pour signaler des informations détaillées sur l’État et l’erreur.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-104">The **\_\_ExtendedStatus** system class is used to report detailed status and error information.</span></span>

<span data-ttu-id="8dfcb-105">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8dfcb-106">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dfcb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8dfcb-107">Syntax</span></span>

``` syntax
class __ExtendedStatus : __NotifyStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
};
```

## <a name="members"></a><span data-ttu-id="8dfcb-108">Membres</span><span class="sxs-lookup"><span data-stu-id="8dfcb-108">Members</span></span>

<span data-ttu-id="8dfcb-109">La classe **\_ \_ ExtendedStatus** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8dfcb-109">The **\_\_ExtendedStatus** class has these types of members:</span></span>

-   [<span data-ttu-id="8dfcb-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8dfcb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8dfcb-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8dfcb-111">Properties</span></span>

<span data-ttu-id="8dfcb-112">La classe **\_ \_ ExtendedStatus** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-112">The **\_\_ExtendedStatus** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8dfcb-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-113">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfcb-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfcb-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8dfcb-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dfcb-116">Toute chaîne définie par l’utilisateur qui décrit une erreur ou un état opérationnel.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-116">Any user-defined string that describes an error or operational status.</span></span>

</dd> <dt>

<span data-ttu-id="8dfcb-117">**Opération**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-117">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfcb-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfcb-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8dfcb-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dfcb-120">Opération qui se produit au moment d’une défaillance ou d’une anomalie.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-120">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="8dfcb-121">En règle générale, Windows Management Instrumentation (WMI) définit cette propriété sur le nom d’une API COM pour la méthode WMI, telle que la suivante : [**IWbemServices :: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="8dfcb-121">Typically, Windows Management Instrumentation (WMI) sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

</dd> <dt>

<span data-ttu-id="8dfcb-122">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-122">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfcb-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfcb-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8dfcb-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dfcb-125">Paramètres impliqués dans une modification d’erreur ou d’État.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-125">Parameters involved in an error or status change.</span></span> <span data-ttu-id="8dfcb-126">Par exemple, si une application tente de récupérer une classe qui n’existe pas, cette propriété est définie sur le nom de la classe incriminée.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-126">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

</dd> <dt>

<span data-ttu-id="8dfcb-127">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-127">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfcb-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8dfcb-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8dfcb-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dfcb-130">Identifie le fournisseur qui provoque ou signale une modification d’erreur ou d’État.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-130">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="8dfcb-131">Si aucun fournisseur n’est impliqué, cette chaîne est définie sur « Windows Management ».</span><span class="sxs-lookup"><span data-stu-id="8dfcb-131">If a provider is not involved, this string is set to "Windows Management".</span></span>

</dd> <dt>

<span data-ttu-id="8dfcb-132">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-132">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8dfcb-133">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="8dfcb-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8dfcb-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8dfcb-135">Contient une erreur ou un code d’information pour une opération.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-135">Contains an error or information code for an operation.</span></span> <span data-ttu-id="8dfcb-136">Il peut s’agir de n’importe quelle valeur définie par le fournisseur, mais la valeur 0 (zéro) est généralement réservée pour indiquer la réussite.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-136">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="8dfcb-137">Cette propriété est héritée de [**\_ \_ NotifyStatus**](--notifystatus.md).</span><span class="sxs-lookup"><span data-stu-id="8dfcb-137">This property is inherited from [**\_\_NotifyStatus**](--notifystatus.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8dfcb-138">Notes</span><span class="sxs-lookup"><span data-stu-id="8dfcb-138">Remarks</span></span>

<span data-ttu-id="8dfcb-139">La classe **\_ \_ ExtendedStatus** est dérivée de la classe [**\_ \_ NotifyStatus**](--notifystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="8dfcb-139">The **\_\_ExtendedStatus** class is derived from the [**\_\_NotifyStatus**](--notifystatus.md) class.</span></span>

<span data-ttu-id="8dfcb-140">Utilisez la classe **\_ \_ ExtendedStatus** pour signaler des informations plus complexes qu’un code de résultat simple.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-140">Use the **\_\_ExtendedStatus** class to report information that is more complex than a simple result code.</span></span> <span data-ttu-id="8dfcb-141">Les fournisseurs peuvent dériver leurs propres classes à partir de **\_ \_ ExtendedStatus** s’ils requièrent plus de propriétés pour décrire les erreurs.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-141">Providers can derive their own classes from **\_\_ExtendedStatus** if they require more properties to describe the errors.</span></span>

<span data-ttu-id="8dfcb-142">La propriété **statusCode** , héritée de la classe parente [**\_ \_ NotifyStatus**](--notifystatus.md) , est un entier non signé qui représente la valeur de l’erreur ou de l’État.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-142">The **StatusCode** property, inherited from the [**\_\_NotifyStatus**](--notifystatus.md) parent class, is an unsigned integer that represents the error or status value.</span></span> <span data-ttu-id="8dfcb-143">Lorsque des instances de cette classe sont retournées par un fournisseur dynamique à partir d’une méthode, les propriétés **statusCode** et **Description** sont définies par le fournisseur, et les autres propriétés sont définies par WMI.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-143">When instances of this class are returned from a method by a dynamic provider, the **StatusCode** and **Description** properties are set by the provider, and the other properties are set by WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="8dfcb-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="8dfcb-144">Examples</span></span>

<span data-ttu-id="8dfcb-145">L’exemple de code suivant, extrait de l’exemple de code [FND : How to handle Configuration Manager des erreurs asynchrones à l’aide](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) de code WMI VBScript dans la Galerie TechNet, décrit l’utilisation de **\_ \_ ExtendedStatus** pour récupérer des informations d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8dfcb-145">The following code sample, taken from the [FND:How to Handle Configuration Manager Asynchronous Errors by Using WMI](https://Gallery.TechNet.Microsoft.Com/0bc05d07-1479-43c9-8e01-0f01d0fc3daa) VBScript code example on TechNet Gallery, describes using **\_\_ExtendedStatus** to retrieve error information.</span></span>


```VB
Sub sink_OnCompleted(HResult, oErr, oCtx) 
    WScript.Echo "All collections returned" 
  
    if HResult <> 0 Then  
    ' Determine the type of error. 
        If oErr.Path_.Class = "__ExtendedStatus" Then 
            WScript.Echo "WMI Error: "& oErr.Description             
        ElseIf ExtendedStatus.Path_.Class = "SMS_ExtendedStatus" Then 
            WScript.Echo "Provider Error: "& oErr.Description 
            WScript.Echo "Code: " & oErr.ErrorCode 
        End If 
    End If     
    bdone = true 
End sub
```



## <a name="requirements"></a><span data-ttu-id="8dfcb-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dfcb-146">Requirements</span></span>



| <span data-ttu-id="8dfcb-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dfcb-147">Requirement</span></span> | <span data-ttu-id="8dfcb-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dfcb-148">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8dfcb-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dfcb-149">Minimum supported client</span></span><br/> | <span data-ttu-id="8dfcb-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8dfcb-150">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8dfcb-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dfcb-151">Minimum supported server</span></span><br/> | <span data-ttu-id="8dfcb-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8dfcb-152">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8dfcb-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8dfcb-153">Namespace</span></span><br/>                | <span data-ttu-id="8dfcb-154">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="8dfcb-154">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="8dfcb-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dfcb-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dfcb-156">**\_\_NotifyStatus**</span><span class="sxs-lookup"><span data-stu-id="8dfcb-156">**\_\_NotifyStatus**</span></span>](/windows/desktop/WmiSdk/--notifystatus)
</dt> <dt>

[<span data-ttu-id="8dfcb-157">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="8dfcb-157">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

