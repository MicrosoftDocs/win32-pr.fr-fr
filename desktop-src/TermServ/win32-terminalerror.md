---
title: Classe Win32_TerminalError
description: Représente une erreur de terminal.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Win32_TerminalError de la classe Services Bureau à distance
- Win32_TerminalError de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103145"
---
# <a name="win32_terminalerror-class"></a><span data-ttu-id="d2ef9-105">\_Classe TerminalError Win32</span><span class="sxs-lookup"><span data-stu-id="d2ef9-105">Win32\_TerminalError class</span></span>

<span data-ttu-id="d2ef9-106">Représente une erreur de terminal.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-106">Represents a terminal error.</span></span>

<span data-ttu-id="d2ef9-107">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ef9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2ef9-108">Syntax</span></span>

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a><span data-ttu-id="d2ef9-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d2ef9-109">Members</span></span>

<span data-ttu-id="d2ef9-110">La classe **Win32 \_ TerminalError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d2ef9-110">The **Win32\_TerminalError** class has these types of members:</span></span>

-   [<span data-ttu-id="d2ef9-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d2ef9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2ef9-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d2ef9-112">Properties</span></span>

<span data-ttu-id="d2ef9-113">La classe **Win32 \_ TerminalError** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-113">The **Win32\_TerminalError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2ef9-114">**Description**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-114">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ef9-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ef9-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ef9-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ef9-117">Toute chaîne définie par l’utilisateur qui décrit une erreur ou un état opérationnel.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-117">Any user-defined string that describes an error or operational status.</span></span>

<span data-ttu-id="d2ef9-118">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="d2ef9-118">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="d2ef9-119">**Opération**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-119">**Operation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ef9-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ef9-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ef9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ef9-122">Opération qui se produit au moment d’une défaillance ou d’une anomalie.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-122">Operation that takes place at the time of a failure or anomaly.</span></span> <span data-ttu-id="d2ef9-123">En général, WMI définit cette propriété sur le nom d’une API COM pour la méthode WMI, telle que la suivante : [**IWbemServices :: CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span><span class="sxs-lookup"><span data-stu-id="d2ef9-123">Typically, WMI sets this property to the name of a COM API for WMI method such as the following: [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).</span></span>

<span data-ttu-id="d2ef9-124">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="d2ef9-124">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="d2ef9-125">**ParameterInfo**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-125">**ParameterInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ef9-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ef9-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ef9-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ef9-128">Paramètres impliqués dans une modification d’erreur ou d’État.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-128">Parameters involved in an error or status change.</span></span> <span data-ttu-id="d2ef9-129">Par exemple, si une application tente de récupérer une classe qui n’existe pas, cette propriété est définie sur le nom de la classe incriminée.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-129">For example, if an application attempts to retrieve a class that does not exist, this property is set to the offending class name.</span></span>

<span data-ttu-id="d2ef9-130">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="d2ef9-130">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="d2ef9-131">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-131">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ef9-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ef9-133">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ef9-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ef9-134">Identifie le fournisseur qui provoque ou signale une modification d’erreur ou d’État.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-134">Identifies the provider that causes or reports an error or status change.</span></span> <span data-ttu-id="d2ef9-135">Si aucun fournisseur n’est impliqué, cette chaîne est définie sur « Windows Management ».</span><span class="sxs-lookup"><span data-stu-id="d2ef9-135">If a provider is not involved, this string is set to "Windows Management".</span></span>

<span data-ttu-id="d2ef9-136">Cette propriété est héritée de [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span><span class="sxs-lookup"><span data-stu-id="d2ef9-136">This property is inherited from [**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).</span></span>

</dd> <dt>

<span data-ttu-id="d2ef9-137">**StatusCode**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-137">**StatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ef9-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2ef9-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ef9-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ef9-140">Contient une erreur ou un code d’information pour une opération.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-140">Contains an error or information code for an operation.</span></span> <span data-ttu-id="d2ef9-141">Il peut s’agir de n’importe quelle valeur définie par le fournisseur, mais la valeur 0 (zéro) est généralement réservée pour indiquer la réussite.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-141">This can be any value defined by the provider, but the value 0 (zero) is usually reserved to indicate success.</span></span> <span data-ttu-id="d2ef9-142">Cette propriété est héritée de [**\_ \_ NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span><span class="sxs-lookup"><span data-stu-id="d2ef9-142">This property is inherited from [**\_\_NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).</span></span>

</dd> <dt>

<span data-ttu-id="d2ef9-143">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-143">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2ef9-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2ef9-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d2ef9-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d2ef9-146">Nom du sinus du terminal sur lequel l’erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d2ef9-146">The name of the terminal sin which the error occurred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2ef9-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2ef9-147">Requirements</span></span>



| <span data-ttu-id="d2ef9-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2ef9-148">Requirement</span></span> | <span data-ttu-id="d2ef9-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2ef9-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ef9-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2ef9-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ef9-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2ef9-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2ef9-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2ef9-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ef9-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2ef9-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2ef9-154">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d2ef9-154">Namespace</span></span><br/>                | <span data-ttu-id="d2ef9-155">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="d2ef9-155">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d2ef9-156">MOF</span><span class="sxs-lookup"><span data-stu-id="d2ef9-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2ef9-157"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2ef9-157"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2ef9-158">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ef9-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2ef9-159"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2ef9-159"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2ef9-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2ef9-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ef9-161">**\_\_ExtendedStatus**</span><span class="sxs-lookup"><span data-stu-id="d2ef9-161">**\_\_ExtendedStatus**</span></span>](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

