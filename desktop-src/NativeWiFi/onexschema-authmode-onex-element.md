---
description: Spécifie le type d’informations d’identification utilisées pour l’authentification.
ms.assetid: a56ce888-ec07-4ce8-a540-6d1890cb338d
title: Élément authMode (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d699b27746226c3eb1550cfd9250e229b40a22e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517694"
---
# <a name="authmode-onex-element"></a><span data-ttu-id="434c7-103">Élément authMode (OneX)</span><span class="sxs-lookup"><span data-stu-id="434c7-103">authMode (OneX) Element</span></span>

<span data-ttu-id="434c7-104">L’élément authMode (OneX) spécifie le type d’informations d’identification utilisées pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="434c7-104">The authMode (OneX) element specifies the type of credentials used for authentication.</span></span> <span data-ttu-id="434c7-105">Le tableau suivant décrit les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="434c7-105">The following table describes the possible values.</span></span>



| <span data-ttu-id="434c7-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="434c7-106">Value</span></span>         | <span data-ttu-id="434c7-107">Description</span><span class="sxs-lookup"><span data-stu-id="434c7-107">Description</span></span>                                                                                                                                                             |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="434c7-108">machineOrUser</span><span class="sxs-lookup"><span data-stu-id="434c7-108">machineOrUser</span></span> | <span data-ttu-id="434c7-109">Utilisez les informations d’identification de l’ordinateur ou de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="434c7-109">Use machine or user credentials.</span></span> <span data-ttu-id="434c7-110">Lorsqu’un utilisateur a ouvert une session, les informations d’identification de l’utilisateur sont utilisées pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="434c7-110">When a user is logged on, the user's credentials are used for authentication.</span></span> <span data-ttu-id="434c7-111">Quand aucun utilisateur n’est connecté, les informations d’identification de l’ordinateur sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="434c7-111">When no user is logged on, machine credentials are used.</span></span> |
| <span data-ttu-id="434c7-112">ordinateur</span><span class="sxs-lookup"><span data-stu-id="434c7-112">machine</span></span>       | <span data-ttu-id="434c7-113">Utiliser uniquement les informations d’identification de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="434c7-113">Use machine credentials only.</span></span>                                                                                                                                           |
| <span data-ttu-id="434c7-114">utilisateur</span><span class="sxs-lookup"><span data-stu-id="434c7-114">user</span></span>          | <span data-ttu-id="434c7-115">Utiliser uniquement les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="434c7-115">Use user credentials only.</span></span>                                                                                                                                              |
| <span data-ttu-id="434c7-116">guest</span><span class="sxs-lookup"><span data-stu-id="434c7-116">guest</span></span>         | <span data-ttu-id="434c7-117">Utilisez uniquement les informations d’identification invité (vide).</span><span class="sxs-lookup"><span data-stu-id="434c7-117">Use guest (empty) credentials only.</span></span>                                                                                                                                     |



 

<span data-ttu-id="434c7-118">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="434c7-118">This element is optional.</span></span> <span data-ttu-id="434c7-119">Quand authMode n’est pas spécifié dans un profil, la valeur `machineOrUser` est utilisée.</span><span class="sxs-lookup"><span data-stu-id="434c7-119">When authMode is not specified in a profile, a value of `machineOrUser` is used.</span></span>

<span data-ttu-id="434c7-120">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="434c7-120">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="machineOrUser"
             />
            <xs:enumeration
                value="machine"
             />
            <xs:enumeration
                value="user"
             />
            <xs:enumeration
                value="guest"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="434c7-121">L’élément **authmode** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="434c7-121">The **authMode** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="434c7-122">Notes</span><span class="sxs-lookup"><span data-stu-id="434c7-122">Remarks</span></span>

<span data-ttu-id="434c7-123">Ce paramètre peut être défini sur la ligne de commande à l’aide de la commande **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="434c7-123">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="434c7-124">Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="434c7-124">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="434c7-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="434c7-125">Requirements</span></span>



| <span data-ttu-id="434c7-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="434c7-126">Requirement</span></span> | <span data-ttu-id="434c7-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="434c7-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="434c7-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="434c7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="434c7-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="434c7-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="434c7-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="434c7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="434c7-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="434c7-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="434c7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="434c7-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="434c7-133">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="434c7-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="434c7-134">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="434c7-134">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="434c7-135">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="434c7-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="434c7-136">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="434c7-136">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
