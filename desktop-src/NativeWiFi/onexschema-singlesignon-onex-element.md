---
description: Spécifie les informations de configuration du réseau de l’authentification unique (SSO).
ms.assetid: c0a26f15-77fd-43e9-a6af-54e9b46f03fa
title: Élément singleSignOn (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- singleSignOn
api_type:
- Schema
api_location: ''
ms.openlocfilehash: fd25767ed311e9a6f0e75f8dec090d4b80d3f0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521554"
---
# <a name="singlesignon-onex-element"></a><span data-ttu-id="bbf2d-103">Élément singleSignOn (OneX)</span><span class="sxs-lookup"><span data-stu-id="bbf2d-103">singleSignOn (OneX) Element</span></span>

<span data-ttu-id="bbf2d-104">L’élément singleSignOn (OneX) spécifie les informations de configuration du réseau de l’authentification unique (SSO).</span><span class="sxs-lookup"><span data-stu-id="bbf2d-104">The singleSignOn (OneX) element specifies single sign-on (SSO) network configuration information.</span></span>

<span data-ttu-id="bbf2d-105">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="bbf2d-105">This element is optional.</span></span> <span data-ttu-id="bbf2d-106">N’utilisez pas l’élément singleSignOn dans un profil si le réseau ne l’exige pas.</span><span class="sxs-lookup"><span data-stu-id="bbf2d-106">Do not use the singleSignOn element in a profile if the network does not require it.</span></span>

<span data-ttu-id="bbf2d-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="bbf2d-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="singleSignOn">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="type"
                minOccurs="1"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="preLogon"
                         />
                        <xs:enumeration
                            value="postLogon"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxDelay"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="0"
                         />
                        <xs:enumeration
                            value="120"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="userBasedVirtualLan"
                type="boolean"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="bbf2d-108">L’élément **singleSignOn** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bbf2d-108">The **singleSignOn** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bbf2d-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bbf2d-109">Child elements</span></span>



| <span data-ttu-id="bbf2d-110">Élément</span><span class="sxs-lookup"><span data-stu-id="bbf2d-110">Element</span></span>                                                                            | <span data-ttu-id="bbf2d-111">Type</span><span class="sxs-lookup"><span data-stu-id="bbf2d-111">Type</span></span>    | <span data-ttu-id="bbf2d-112">Description</span><span class="sxs-lookup"><span data-stu-id="bbf2d-112">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbf2d-113">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="bbf2d-113">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="bbf2d-114">Spécifie, en secondes, le délai maximal avant que la tentative de connexion d’authentification unique échoue.</span><span class="sxs-lookup"><span data-stu-id="bbf2d-114">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="bbf2d-115">**entrer**</span><span class="sxs-lookup"><span data-stu-id="bbf2d-115">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="bbf2d-116">Spécifie quand l’authentification unique est effectuée.</span><span class="sxs-lookup"><span data-stu-id="bbf2d-116">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="bbf2d-117">Lorsque la valeur `preLogon` est définie sur, l’authentification unique est effectuée avant que l’utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="bbf2d-117">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="bbf2d-118">Lorsque la valeur `postLogon` est définie sur, l’authentification unique est effectuée immédiatement après la connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bbf2d-118">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="bbf2d-119">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="bbf2d-119">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="bbf2d-120">boolean</span><span class="sxs-lookup"><span data-stu-id="bbf2d-120">boolean</span></span> | <span data-ttu-id="bbf2d-121">Spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bbf2d-121">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="bbf2d-122">Notes</span><span class="sxs-lookup"><span data-stu-id="bbf2d-122">Remarks</span></span>

<span data-ttu-id="bbf2d-123">Ce paramètre peut être défini sur la ligne de commande à l’aide de la commande **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="bbf2d-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="bbf2d-124">Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="bbf2d-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbf2d-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbf2d-125">Requirements</span></span>



| <span data-ttu-id="bbf2d-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbf2d-126">Requirement</span></span> | <span data-ttu-id="bbf2d-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbf2d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bbf2d-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbf2d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bbf2d-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbf2d-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bbf2d-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbf2d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bbf2d-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbf2d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbf2d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbf2d-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="bbf2d-133">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="bbf2d-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bbf2d-134">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="bbf2d-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="bbf2d-135">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="bbf2d-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bbf2d-136">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="bbf2d-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
