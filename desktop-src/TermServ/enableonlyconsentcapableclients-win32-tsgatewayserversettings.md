---
title: Méthode EnableOnlyConsentCapableClients de la classe Win32_TSGatewayServerSettings
description: Définit la propriété OnlyConsentCapableClients.
ms.assetid: abc91ea8-0f3c-4b7c-9091-3c8193e610da
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableOnlyConsentCapableClients
- Services Bureau à distance de la méthode EnableOnlyConsentCapableClients, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode EnableOnlyConsentCapableClients
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableOnlyConsentCapableClients
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb671ccefe98cdc1b569bcde155071ef7cc0d9ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032586"
---
# <a name="enableonlyconsentcapableclients-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="480eb-106">Méthode EnableOnlyConsentCapableClients de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="480eb-106">EnableOnlyConsentCapableClients method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="480eb-107">Définit la propriété **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="480eb-107">Sets the **OnlyConsentCapableClients** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="480eb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="480eb-108">Syntax</span></span>


```mof
uint32 EnableOnlyConsentCapableClients(
  [in] boolean OnlyConsentCapableClients
);
```



## <a name="parameters"></a><span data-ttu-id="480eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="480eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="480eb-110">*OnlyConsentCapableClients* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="480eb-110">*OnlyConsentCapableClients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="480eb-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="480eb-111">Type: **boolean**</span></span>

<span data-ttu-id="480eb-112">Spécifie la nouvelle valeur de la propriété **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="480eb-112">Specifies the new value for the **OnlyConsentCapableClients** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="480eb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="480eb-113">Return value</span></span>

<span data-ttu-id="480eb-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="480eb-114">Type: **uint32**</span></span>

<span data-ttu-id="480eb-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="480eb-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="480eb-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="480eb-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="480eb-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="480eb-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="480eb-118">Notes</span><span class="sxs-lookup"><span data-stu-id="480eb-118">Remarks</span></span>

<span data-ttu-id="480eb-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="480eb-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="480eb-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="480eb-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="480eb-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="480eb-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="480eb-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="480eb-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="480eb-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="480eb-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="480eb-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="480eb-124">Requirements</span></span>



| <span data-ttu-id="480eb-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="480eb-125">Requirement</span></span> | <span data-ttu-id="480eb-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="480eb-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="480eb-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="480eb-127">Minimum supported client</span></span><br/> | <span data-ttu-id="480eb-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="480eb-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="480eb-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="480eb-129">Minimum supported server</span></span><br/> | <span data-ttu-id="480eb-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="480eb-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="480eb-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="480eb-131">Namespace</span></span><br/>                | <span data-ttu-id="480eb-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="480eb-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="480eb-133">MOF</span><span class="sxs-lookup"><span data-stu-id="480eb-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="480eb-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="480eb-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="480eb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="480eb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="480eb-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="480eb-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="480eb-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="480eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="480eb-138">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="480eb-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

