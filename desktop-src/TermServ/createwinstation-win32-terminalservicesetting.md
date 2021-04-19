---
title: Méthode CreateWinstation de la classe Win32_TerminalServiceSetting
description: Crée une pile d’écouteurs basée sur la combinaison unique du nom d’écouteur et de la carte réseau.
ms.assetid: c0a25c22-e0a4-42b1-9c48-c88eebbc55b5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CreateWinstation
- Services Bureau à distance de la méthode CreateWinstation, classe Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de la classe Services Bureau à distance, méthode CreateWinstation
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.CreateWinstation
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 112237a00e9e92a2074ee0b95f9964d73f083e43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511348"
---
# <a name="createwinstation-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="02199-106">Méthode CreateWinstation de la \_ classe Win32 TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="02199-106">CreateWinstation method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="02199-107">La méthode **CreateWinstation** crée une nouvelle pile d’écouteurs en fonction de la combinaison unique du nom d’écouteur et de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="02199-107">The **CreateWinstation** method creates a new listener stack based on the unique combination of listener name and NIC.</span></span>

## <a name="syntax"></a><span data-ttu-id="02199-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02199-108">Syntax</span></span>


```mof
uint32 CreateWinstation(
  [in] string Name,
  [in] string WinstaDriverName,
  [in] uint32 LanaId
);
```



## <a name="parameters"></a><span data-ttu-id="02199-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02199-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02199-110">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02199-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02199-111">Nom de l’écouteur.</span><span class="sxs-lookup"><span data-stu-id="02199-111">Listener name.</span></span>

</dd> <dt>

<span data-ttu-id="02199-112">*WinstaDriverName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02199-112">*WinstaDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02199-113">Nom du pilote de la station de nom.</span><span class="sxs-lookup"><span data-stu-id="02199-113">The winstation driver name.</span></span>

</dd> <dt>

<span data-ttu-id="02199-114">*LanaId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="02199-114">*LanaId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02199-115">Numéro de carte réseau local (LANA) NetBIOS pour la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="02199-115">NetBIOS Local Area Network Adapter (LANA) number for the NIC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02199-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02199-116">Return value</span></span>

<span data-ttu-id="02199-117">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="02199-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="02199-118">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="02199-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="02199-119">Notes</span><span class="sxs-lookup"><span data-stu-id="02199-119">Remarks</span></span>

<span data-ttu-id="02199-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="02199-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="02199-121">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="02199-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="02199-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="02199-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="02199-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="02199-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="02199-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02199-124">Requirements</span></span>



| <span data-ttu-id="02199-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02199-125">Requirement</span></span> | <span data-ttu-id="02199-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="02199-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02199-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02199-127">Minimum supported client</span></span><br/> | <span data-ttu-id="02199-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02199-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02199-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02199-129">Minimum supported server</span></span><br/> | <span data-ttu-id="02199-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02199-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02199-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="02199-131">Namespace</span></span><br/>                | <span data-ttu-id="02199-132">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="02199-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="02199-133">MOF</span><span class="sxs-lookup"><span data-stu-id="02199-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02199-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02199-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="02199-135">DLL</span><span class="sxs-lookup"><span data-stu-id="02199-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02199-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02199-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02199-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02199-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02199-138">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="02199-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

