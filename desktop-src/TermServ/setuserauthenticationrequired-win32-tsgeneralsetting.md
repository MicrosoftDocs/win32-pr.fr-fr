---
title: Méthode SetUserAuthenticationRequired de la classe Win32_TSGeneralSetting
description: Active ou désactive l’exigence selon laquelle les utilisateurs doivent être authentifiés au moment de la connexion en définissant la valeur de la propriété UserAuthenticationRequired.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetUserAuthenticationRequired
- Services Bureau à distance de la méthode SetUserAuthenticationRequired, classe Win32_TSGeneralSetting
- Win32_TSGeneralSetting de la classe Services Bureau à distance, méthode SetUserAuthenticationRequired
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317429"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a><span data-ttu-id="f67ac-106">Méthode SetUserAuthenticationRequired de la \_ classe Win32 TSGeneralSetting</span><span class="sxs-lookup"><span data-stu-id="f67ac-106">SetUserAuthenticationRequired method of the Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="f67ac-107">Active ou désactive la spécification selon laquelle les utilisateurs doivent être authentifiés au moment de la connexion en définissant la valeur de la propriété **UserAuthenticationRequired** dans la classe [**\_ TSGeneralSetting Win32**](win32-tsgeneralsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="f67ac-107">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property in the [**Win32\_TSGeneralSetting**](win32-tsgeneralsetting.md) class.</span></span> <span data-ttu-id="f67ac-108">Si la **valeur est true**, ce qui signifie qu’elle est activée, **UserAuthenticationRequired** nécessite l’authentification de l’utilisateur au moment de la connexion pour augmenter la protection du serveur contre les attaques réseau.</span><span class="sxs-lookup"><span data-stu-id="f67ac-108">If **True**, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="f67ac-109">Seuls les clients protocole RDP (Remote Desktop Protocol) (RDP) qui prennent en charge le protocole RDP version 6,0 ou une version ultérieure sont en mesure de se connecter.</span><span class="sxs-lookup"><span data-stu-id="f67ac-109">Only Remote Desktop Protocol (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="f67ac-110">Pour éviter les interruptions pour les utilisateurs distants, il est recommandé de déployer les clients RDP qui prennent en charge la version de protocole appropriée avant d’activer la propriété.</span><span class="sxs-lookup"><span data-stu-id="f67ac-110">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f67ac-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f67ac-111">Syntax</span></span>


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a><span data-ttu-id="f67ac-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f67ac-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f67ac-113">*UserAuthenticationRequired* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f67ac-113">*UserAuthenticationRequired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f67ac-114">Indique si l’authentification de l’utilisateur est requise.</span><span class="sxs-lookup"><span data-stu-id="f67ac-114">Indicates whether user authentication is required.</span></span>

<dt>

<span data-ttu-id="f67ac-115">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f67ac-115">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f67ac-116">Désactiver l’exigence selon laquelle l’utilisateur doit être authentifié</span><span class="sxs-lookup"><span data-stu-id="f67ac-116">Disable requirement that user must be authenticated</span></span>

</dd> <dt>

<span data-ttu-id="f67ac-117">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f67ac-117">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f67ac-118">Permet d’exiger l’authentification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f67ac-118">Enables requirement that user must be authenticated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f67ac-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f67ac-119">Return value</span></span>

<span data-ttu-id="f67ac-120">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="f67ac-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f67ac-121">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f67ac-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f67ac-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f67ac-122">Remarks</span></span>

<span data-ttu-id="f67ac-123">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f67ac-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f67ac-124">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f67ac-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f67ac-125">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f67ac-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f67ac-126">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f67ac-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f67ac-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f67ac-127">Requirements</span></span>



| <span data-ttu-id="f67ac-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f67ac-128">Requirement</span></span> | <span data-ttu-id="f67ac-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f67ac-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f67ac-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f67ac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f67ac-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f67ac-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f67ac-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f67ac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f67ac-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f67ac-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f67ac-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f67ac-134">Namespace</span></span><br/>                | <span data-ttu-id="f67ac-135">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="f67ac-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f67ac-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f67ac-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f67ac-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f67ac-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f67ac-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f67ac-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f67ac-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f67ac-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f67ac-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f67ac-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f67ac-141">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f67ac-141">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> </dl>

 

