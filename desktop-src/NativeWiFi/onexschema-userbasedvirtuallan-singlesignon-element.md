---
description: Spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur.
ms.assetid: 4ac92954-adb2-4b0c-9c4e-81f772ea03ed
title: Élément userBasedVirtualLan (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- userBasedVirtualLan
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ef421e35f7fa121c31e58cfeba4eee969a1b6fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113615"
---
# <a name="userbasedvirtuallan-singlesignon-element"></a><span data-ttu-id="8f7a0-103">Élément userBasedVirtualLan (singleSignOn)</span><span class="sxs-lookup"><span data-stu-id="8f7a0-103">userBasedVirtualLan (singleSignOn) Element</span></span>

<span data-ttu-id="8f7a0-104">L’élément userBasedVirtualLan (singleSignOn) spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f7a0-104">The userBasedVirtualLan (singleSignOn) element specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span> <span data-ttu-id="8f7a0-105">Certains périphériques NAS (Network Access Server) modifient le réseau local virtuel après l’authentification d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f7a0-105">Some network access server (NAS) devices change the VLAN after a user authenticates.</span></span> <span data-ttu-id="8f7a0-106">Quand userBasedVirtualLan a la valeur TRUE, le NAS peut modifier le réseau local virtuel d’un appareil après l’authentification d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8f7a0-106">When userBasedVirtualLan is TRUE, the NAS may change a device's VLAN after a user authenticates.</span></span>

<span data-ttu-id="8f7a0-107">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="8f7a0-107">This element is optional.</span></span> <span data-ttu-id="8f7a0-108">Quand userBasedVirtualLan n’est pas spécifié dans un profil, la valeur FALSe est utilisée.</span><span class="sxs-lookup"><span data-stu-id="8f7a0-108">When userBasedVirtualLan is not specified in a profile, a value of FALSE is used.</span></span>

<span data-ttu-id="8f7a0-109">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="8f7a0-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="userBasedVirtualLan"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="8f7a0-110">L’élément **userBasedVirtualLan** est défini par l’élément [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8f7a0-110">The **userBasedVirtualLan** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f7a0-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8f7a0-111">Remarks</span></span>

<span data-ttu-id="8f7a0-112">Ce paramètre peut être défini sur la ligne de commande à l’aide de la commande **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="8f7a0-112">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="8f7a0-113">Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="8f7a0-113">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f7a0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f7a0-114">Requirements</span></span>



| <span data-ttu-id="8f7a0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f7a0-115">Requirement</span></span> | <span data-ttu-id="8f7a0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f7a0-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8f7a0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f7a0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8f7a0-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f7a0-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8f7a0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f7a0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8f7a0-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f7a0-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8f7a0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f7a0-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f7a0-122">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="8f7a0-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8f7a0-123">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="8f7a0-123">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="8f7a0-124">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="8f7a0-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8f7a0-125">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="8f7a0-125">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
