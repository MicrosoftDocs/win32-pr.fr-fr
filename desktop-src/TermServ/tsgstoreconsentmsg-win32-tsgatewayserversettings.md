---
title: Méthode TSGStoreConsentMsg de la classe Win32_TSGatewayServerSettings
description: Met à jour le message de consentement pour le serveur de passerelle.
ms.assetid: b3146d87-95af-4b6b-8c02-5ac4748fbe98
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode TSGStoreConsentMsg
- Services Bureau à distance de la méthode TSGStoreConsentMsg, classe Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, méthode TSGStoreConsentMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907097739d21e1523aca3b719cdb5f18b6f3fa30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465558"
---
# <a name="tsgstoreconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="5468e-106">Méthode TSGStoreConsentMsg de la \_ classe Win32 TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="5468e-106">TSGStoreConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="5468e-107">Met à jour le message de consentement pour le serveur de passerelle.</span><span class="sxs-lookup"><span data-stu-id="5468e-107">Updates the consent message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5468e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5468e-108">Syntax</span></span>


```mof
uint32 TSGStoreConsentMsg(
  [in] string TSGConMsgText
);
```



## <a name="parameters"></a><span data-ttu-id="5468e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5468e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5468e-110">*TSGConMsgText* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5468e-110">*TSGConMsgText* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5468e-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5468e-111">Type: **string**</span></span>

<span data-ttu-id="5468e-112">Texte du message de consentement.</span><span class="sxs-lookup"><span data-stu-id="5468e-112">The consent message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5468e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5468e-113">Return value</span></span>

<span data-ttu-id="5468e-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5468e-114">Type: **uint32**</span></span>

<span data-ttu-id="5468e-115">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="5468e-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="5468e-116">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="5468e-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="5468e-117">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5468e-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5468e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="5468e-118">Remarks</span></span>

<span data-ttu-id="5468e-119">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5468e-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="5468e-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5468e-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5468e-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5468e-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5468e-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5468e-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5468e-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5468e-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5468e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5468e-124">Requirements</span></span>



| <span data-ttu-id="5468e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5468e-125">Requirement</span></span> | <span data-ttu-id="5468e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="5468e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5468e-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5468e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5468e-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5468e-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5468e-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5468e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5468e-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5468e-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="5468e-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5468e-131">Namespace</span></span><br/>                | <span data-ttu-id="5468e-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5468e-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5468e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="5468e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5468e-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5468e-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="5468e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5468e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5468e-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5468e-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="5468e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5468e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5468e-138">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="5468e-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

