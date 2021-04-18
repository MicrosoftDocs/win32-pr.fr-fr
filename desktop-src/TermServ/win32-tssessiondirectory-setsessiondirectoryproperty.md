---
title: Méthode SetSessionDirectoryProperty de la classe Win32_TSSessionDirectory
description: Définit la propriété SessionDirectoryLocation ou la propriété SessionDirectoryClusterName de la classe.
ms.assetid: 728e1991-294f-4b80-86f8-a0c2cfd10e9c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSessionDirectoryProperty
- Services Bureau à distance de la méthode SetSessionDirectoryProperty, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetSessionDirectoryProperty
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32357e662ec9b2edb05d75a2814d5215fc9ec7f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464958"
---
# <a name="setsessiondirectoryproperty-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="4ef7d-106">Méthode SetSessionDirectoryProperty de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="4ef7d-106">SetSessionDirectoryProperty method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="4ef7d-107">Définit la propriété **SessionDirectoryLocation** ou la propriété **SessionDirectoryClusterName** de la classe.</span><span class="sxs-lookup"><span data-stu-id="4ef7d-107">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ef7d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ef7d-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryProperty(
  [in] string PropertyName,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="4ef7d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ef7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ef7d-110">*PropertyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ef7d-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef7d-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4ef7d-111">Type: **string**</span></span>

<span data-ttu-id="4ef7d-112">Spécifie la propriété définie par la méthode.</span><span class="sxs-lookup"><span data-stu-id="4ef7d-112">Specifies the property that the method is setting.</span></span>

<dt>

<span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>

<span data-ttu-id="4ef7d-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span><span class="sxs-lookup"><span data-stu-id="4ef7d-113"><span id="SessionDirectoryLocation"></span><span id="sessiondirectorylocation"></span><span id="SESSIONDIRECTORYLOCATION"></span>**SessionDirectoryLocation**</span></span>


</dt> <dd>

<span data-ttu-id="4ef7d-114">La méthode définit la propriété **SessionDirectoryLocation** .</span><span class="sxs-lookup"><span data-stu-id="4ef7d-114">The method is setting the **SessionDirectoryLocation** property.</span></span>

</dd> <dt>

<span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>

<span data-ttu-id="4ef7d-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span><span class="sxs-lookup"><span data-stu-id="4ef7d-115"><span id="SessionDirectoryClusterName"></span><span id="sessiondirectoryclustername"></span><span id="SESSIONDIRECTORYCLUSTERNAME"></span>**SessionDirectoryClusterName**</span></span>


</dt> <dd>

<span data-ttu-id="4ef7d-116">La méthode définit la propriété **SessionDirectoryClusterName** .</span><span class="sxs-lookup"><span data-stu-id="4ef7d-116">The method is setting the **SessionDirectoryClusterName** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4ef7d-117">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4ef7d-117">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ef7d-118">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4ef7d-118">Type: **string**</span></span>

<span data-ttu-id="4ef7d-119">Nouvelle valeur de la propriété spécifiée par le paramètre *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="4ef7d-119">The new value for the property specified by the *PropertyName* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ef7d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ef7d-120">Return value</span></span>

<span data-ttu-id="4ef7d-121">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4ef7d-121">Type: **uint32**</span></span>

<span data-ttu-id="4ef7d-122">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="4ef7d-122">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4ef7d-123">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4ef7d-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="4ef7d-124">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="4ef7d-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ef7d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="4ef7d-125">Remarks</span></span>

<span data-ttu-id="4ef7d-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="4ef7d-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4ef7d-127">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4ef7d-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4ef7d-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="4ef7d-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4ef7d-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4ef7d-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ef7d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ef7d-130">Requirements</span></span>



| <span data-ttu-id="4ef7d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ef7d-131">Requirement</span></span> | <span data-ttu-id="4ef7d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ef7d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef7d-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ef7d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4ef7d-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ef7d-134">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4ef7d-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4ef7d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4ef7d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ef7d-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4ef7d-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4ef7d-137">Namespace</span></span><br/>                | <span data-ttu-id="4ef7d-138">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="4ef7d-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4ef7d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4ef7d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4ef7d-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4ef7d-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4ef7d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4ef7d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ef7d-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ef7d-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ef7d-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ef7d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ef7d-144">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="4ef7d-144">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

