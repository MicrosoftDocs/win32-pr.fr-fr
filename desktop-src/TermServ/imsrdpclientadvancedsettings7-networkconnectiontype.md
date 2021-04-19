---
title: IMsRdpClientAdvancedSettings7 propriété NetworkConnectionType
description: Obtient ou définit le type de connexion réseau utilisé entre le client et le serveur. Les informations sur le type de connexion réseau transmises au serveur permettent au serveur d’ajuster plusieurs paramètres en fonction du type de connexion réseau.
ms.assetid: 4dd4fa17-f121-412d-a30d-1c01f4c892b0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété NetworkConnectionType
- Services Bureau à distance de la propriété NetworkConnectionType, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété NetworkConnectionType
- Services Bureau à distance de la propriété NetworkConnectionType, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété NetworkConnectionType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.NetworkConnectionType
- IMsRdpClientAdvancedSettings7.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings7.put_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.NetworkConnectionType
- IMsRdpClientAdvancedSettings8.get_NetworkConnectionType
- IMsRdpClientAdvancedSettings8.put_NetworkConnectionType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df4c1e944920759f56f5d4b493b9cd47e7ebc29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509726"
---
# <a name="imsrdpclientadvancedsettings7networkconnectiontype-property"></a><span data-ttu-id="3a90e-109">IMsRdpClientAdvancedSettings7 :: NetworkConnectionType, propriété</span><span class="sxs-lookup"><span data-stu-id="3a90e-109">IMsRdpClientAdvancedSettings7::NetworkConnectionType property</span></span>

<span data-ttu-id="3a90e-110">Obtient ou définit le type de connexion réseau utilisé entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="3a90e-110">Gets or sets the type of network connection used between the client and server.</span></span> <span data-ttu-id="3a90e-111">Les informations sur le type de connexion réseau transmises au serveur permettent au serveur d’ajuster plusieurs paramètres en fonction du type de connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="3a90e-111">The network connection type information passed on to the server helps the server tune several parameters based on the network connection type.</span></span>

<span data-ttu-id="3a90e-112">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3a90e-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a90e-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a90e-113">Syntax</span></span>


```C++
HRESULT put_NetworkConnectionType(
  [in]          UINT connectionType
);

HRESULT get_NetworkConnectionType(
  [out, retval] UINT *pConnectionType
);
```



## <a name="property-value"></a><span data-ttu-id="3a90e-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3a90e-114">Property value</span></span>

<span data-ttu-id="3a90e-115">Type de connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="3a90e-115">The network connection type.</span></span>

<dt>

<span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>

<span data-ttu-id="3a90e-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**Connexion \_ TAPEZ \_ modem** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="3a90e-116"><span id="CONNECTION_TYPE_MODEM"></span><span id="connection_type_modem"></span>**CONNECTION\_TYPE\_MODEM** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="3a90e-117">Modem (56 Kbits/s)</span><span class="sxs-lookup"><span data-stu-id="3a90e-117">Modem (56 Kbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>

<span data-ttu-id="3a90e-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**Connexion \_ TAPEZ \_ haut débit \_ bas** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="3a90e-118"><span id="CONNECTION_TYPE_BROADBAND_LOW"></span><span id="connection_type_broadband_low"></span>**CONNECTION\_TYPE\_BROADBAND\_LOW** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="3a90e-119">Bande passante basse vitesse (256 kbits/s à 2 Mbits/s)</span><span class="sxs-lookup"><span data-stu-id="3a90e-119">Low-speed broadband (256 Kbps to 2 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>

<span data-ttu-id="3a90e-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**Connexion \_ TYPE \_ satellite** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="3a90e-120"><span id="CONNECTION_TYPE_SATELLITE"></span><span id="connection_type_satellite"></span>**CONNECTION\_TYPE\_SATELLITE** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="3a90e-121">Satellite (2 Mbits/s à 16 Mbits/s, avec une latence élevée)</span><span class="sxs-lookup"><span data-stu-id="3a90e-121">Satellite (2 Mbps to 16 Mbps, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>

<span data-ttu-id="3a90e-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**Connexion \_ TYPE haut \_ débit \_ élevé** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="3a90e-122"><span id="CONNECTION_TYPE_BROADBAND_HIGH"></span><span id="connection_type_broadband_high"></span>**CONNECTION\_TYPE\_BROADBAND\_HIGH** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="3a90e-123">Haut débit haute vitesse (2 Mbits/s à 10 Mbits/s)</span><span class="sxs-lookup"><span data-stu-id="3a90e-123">High-speed broadband (2 Mbps to 10 Mbps)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>

<span data-ttu-id="3a90e-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**Connexion \_ TYPE \_ WAN** (5 (0x5))</span><span class="sxs-lookup"><span data-stu-id="3a90e-124"><span id="CONNECTION_TYPE_WAN"></span><span id="connection_type_wan"></span>**CONNECTION\_TYPE\_WAN** (5 (0x5))</span></span>


</dt> <dd>

<span data-ttu-id="3a90e-125">Réseau étendu (WAN) (10 Mbits/s ou plus, avec une latence élevée)</span><span class="sxs-lookup"><span data-stu-id="3a90e-125">Wide area network (WAN) (10 Mbps or higher, with high latency)</span></span>

</dd> <dt>

<span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>

<span data-ttu-id="3a90e-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**Connexion \_ TAPEZ \_ LAN** (6 (0x6))</span><span class="sxs-lookup"><span data-stu-id="3a90e-126"><span id="CONNECTION_TYPE_LAN"></span><span id="connection_type_lan"></span>**CONNECTION\_TYPE\_LAN** (6 (0x6))</span></span>


</dt> <dd>

<span data-ttu-id="3a90e-127">Réseau local (LAN) (10 Mbits/s ou plus)</span><span class="sxs-lookup"><span data-stu-id="3a90e-127">Local area network (LAN) (10 Mbps or higher)</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a90e-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a90e-128">Requirements</span></span>



| <span data-ttu-id="3a90e-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a90e-129">Requirement</span></span> | <span data-ttu-id="3a90e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a90e-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a90e-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a90e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3a90e-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a90e-132">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="3a90e-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a90e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3a90e-134">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3a90e-134">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="3a90e-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3a90e-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="3a90e-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a90e-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3a90e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="3a90e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a90e-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a90e-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="3a90e-139">IID</span><span class="sxs-lookup"><span data-stu-id="3a90e-139">IID</span></span><br/>                      | <span data-ttu-id="3a90e-140">IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="3a90e-140">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a90e-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a90e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a90e-142">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3a90e-142">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3a90e-143">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3a90e-143">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





