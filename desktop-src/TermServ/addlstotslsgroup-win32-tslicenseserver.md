---
title: Méthode AddLStoTSLSGroup de la classe Win32_TSLicenseServer
description: Ajoute le Bureau à distance serveur de licences au groupe serveurs de licences Connexion Bureau à distance Broker (RD Connection Broker) sur un contrôleur de domaine dans le même domaine que le serveur de licences Bureau à distance.
ms.assetid: 65c6b7cf-324a-44f1-8dfc-40e35ed45d4f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddLStoTSLSGroup
- Services Bureau à distance de la méthode AddLStoTSLSGroup, classe Win32_TSLicenseServer
- Win32_TSLicenseServer de la classe Services Bureau à distance, méthode AddLStoTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.AddLStoTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53934f6682d1a23f99916588aa4eac3b18526c06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384339"
---
# <a name="addlstotslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="97795-106">Méthode AddLStoTSLSGroup de la \_ classe Win32 TSLicenseServer</span><span class="sxs-lookup"><span data-stu-id="97795-106">AddLStoTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="97795-107">Ajoute le Bureau à distance serveur de licences au groupe serveurs de licences Connexion Bureau à distance Broker (RD Connection Broker) sur un contrôleur de domaine dans le même domaine que le serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="97795-107">Adds the Remote Desktop license server to the Remote Desktop Connection Broker (RD Connection Broker) License Servers group on a domain controller in the same domain as the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="97795-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97795-108">Syntax</span></span>


```mof
uint32 AddLStoTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="97795-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97795-109">Parameters</span></span>

<span data-ttu-id="97795-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="97795-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="97795-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97795-111">Return value</span></span>

<span data-ttu-id="97795-112">Si la méthode est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="97795-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="97795-113">Si la méthode échoue, elle retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="97795-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="97795-114">Pour obtenir la liste des codes d’erreur, consultez [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="97795-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="97795-115">Notes</span><span class="sxs-lookup"><span data-stu-id="97795-115">Remarks</span></span>

<span data-ttu-id="97795-116">Vous devez être membre du groupe Admins du domaine pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="97795-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="97795-117">Le serveur de licences doit être membre du groupe Bureau à distance les serveurs de licences si le serveur est configuré pour utiliser l’étendue de la découverte du domaine ou de la forêt.</span><span class="sxs-lookup"><span data-stu-id="97795-117">The license server should be a member of the Remote Desktop license servers group if the server is configured to use the domain or forest discovery scope.</span></span>

<span data-ttu-id="97795-118">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="97795-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="97795-119">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="97795-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="97795-120">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="97795-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="97795-121">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="97795-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="97795-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97795-122">Requirements</span></span>



| <span data-ttu-id="97795-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97795-123">Requirement</span></span> | <span data-ttu-id="97795-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="97795-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="97795-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97795-125">Minimum supported client</span></span><br/> | <span data-ttu-id="97795-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="97795-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="97795-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97795-127">Minimum supported server</span></span><br/> | <span data-ttu-id="97795-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97795-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="97795-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="97795-129">Namespace</span></span><br/>                | <span data-ttu-id="97795-130">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="97795-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="97795-131">MOF</span><span class="sxs-lookup"><span data-stu-id="97795-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97795-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97795-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="97795-133">DLL</span><span class="sxs-lookup"><span data-stu-id="97795-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97795-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97795-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97795-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97795-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97795-136">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="97795-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="97795-137">**IsLSinTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="97795-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 

