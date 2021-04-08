---
title: Méthode SelectNetworkAdapter de la classe Win32_TSVirtualIP
description: Définit l’adresse MAC de la carte réseau à utiliser pour la virtualisation IP.
ms.assetid: ad67445c-6a8b-4980-997a-56aceb70965f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SelectNetworkAdapter
- Services Bureau à distance de la méthode SelectNetworkAdapter, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode SelectNetworkAdapter
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SelectNetworkAdapter
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a362bea1a5cacbfd727f23504f19164c79ce65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942046"
---
# <a name="selectnetworkadapter-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="5472c-106">Méthode SelectNetworkAdapter de la \_ classe Win32 TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="5472c-106">SelectNetworkAdapter method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="5472c-107">Définit l’adresse MAC de la carte réseau à utiliser pour la virtualisation IP.</span><span class="sxs-lookup"><span data-stu-id="5472c-107">Sets the MAC address of the network adapter to use for IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="5472c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5472c-108">Syntax</span></span>


```mof
uint32 SelectNetworkAdapter(
  [in] string NetworkAdapterMacAddress
);
```



## <a name="parameters"></a><span data-ttu-id="5472c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5472c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5472c-110">*NetworkAdapterMacAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5472c-110">*NetworkAdapterMacAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5472c-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5472c-111">Type: **string**</span></span>

<span data-ttu-id="5472c-112">Spécifie l’adresse MAC de la carte réseau.</span><span class="sxs-lookup"><span data-stu-id="5472c-112">Specifies the MAC address of the network adapter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5472c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5472c-113">Return value</span></span>

<span data-ttu-id="5472c-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5472c-114">Type: **uint32**</span></span>

<span data-ttu-id="5472c-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="5472c-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="5472c-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="5472c-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

<span data-ttu-id="5472c-117">Si l’adresse MAC n’est pas valide ou n’existe pas, ou si le mode de virtualisation IP est par session, une erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="5472c-117">If the MAC address is invalid or does not exist, or if the IP virtualization mode is per-session, an error is returned.</span></span>

<span data-ttu-id="5472c-118">La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="5472c-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="5472c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5472c-119">Requirements</span></span>



| <span data-ttu-id="5472c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5472c-120">Requirement</span></span> | <span data-ttu-id="5472c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5472c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5472c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5472c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5472c-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5472c-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5472c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5472c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5472c-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5472c-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="5472c-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5472c-126">Namespace</span></span><br/>                | <span data-ttu-id="5472c-127">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5472c-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5472c-128">MOF</span><span class="sxs-lookup"><span data-stu-id="5472c-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5472c-129"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5472c-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5472c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5472c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5472c-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5472c-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5472c-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5472c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5472c-133">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="5472c-133">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





