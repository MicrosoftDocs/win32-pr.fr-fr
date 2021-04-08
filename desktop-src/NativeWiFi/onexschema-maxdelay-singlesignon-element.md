---
description: Spécifie, en secondes, le délai maximal avant que la tentative de connexion d’authentification unique échoue.
ms.assetid: ba8c137e-dd05-4ebc-9a83-cd612f65d4dc
title: Élément maxDelay (singleSignOn)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxDelay
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8efd069687a2db4b06b90aa594ec31132ce6fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864813"
---
# <a name="maxdelay-singlesignon-element"></a><span data-ttu-id="da065-103">Élément maxDelay (singleSignOn)</span><span class="sxs-lookup"><span data-stu-id="da065-103">maxDelay (singleSignOn) Element</span></span>

<span data-ttu-id="da065-104">L’élément maxDelay (singleSignOn) spécifie, en secondes, le délai maximal avant que la tentative de connexion d’authentification unique échoue.</span><span class="sxs-lookup"><span data-stu-id="da065-104">The maxDelay (singleSignOn) element specifies, in seconds, the maximum delay before the single sign on connection attempt fails.</span></span>

<span data-ttu-id="da065-105">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="da065-105">This element is optional.</span></span> <span data-ttu-id="da065-106">Quand maxDelay n’est pas spécifié dans un profil, une valeur de 10 secondes est utilisée.</span><span class="sxs-lookup"><span data-stu-id="da065-106">When maxDelay is not specified in a profile, a value of 10 seconds is used.</span></span>

<span data-ttu-id="da065-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="da065-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxDelay">
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
```

<span data-ttu-id="da065-108">L’élément **maxDelay** est défini par l’élément [**singleSignOn**](onexschema-singlesignon-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="da065-108">The **maxDelay** element is defined by the [**singleSignOn**](onexschema-singlesignon-onex-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="da065-109">Notes</span><span class="sxs-lookup"><span data-stu-id="da065-109">Remarks</span></span>

<span data-ttu-id="da065-110">Ce paramètre peut être défini sur la ligne de commande à l’aide de la commande **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="da065-110">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="da065-111">Pour plus d’informations, consultez [commandes netsh pour réseau local sans fil (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="da065-111">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="da065-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da065-112">Requirements</span></span>



| <span data-ttu-id="da065-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da065-113">Requirement</span></span> | <span data-ttu-id="da065-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="da065-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da065-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da065-115">Minimum supported client</span></span><br/> | <span data-ttu-id="da065-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da065-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da065-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da065-117">Minimum supported server</span></span><br/> | <span data-ttu-id="da065-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da065-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="da065-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da065-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="da065-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="da065-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="da065-121">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="da065-121">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> <dt>

<span data-ttu-id="da065-122">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="da065-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="da065-123">**singleSignOn (OneX)**</span><span class="sxs-lookup"><span data-stu-id="da065-123">**singleSignOn (OneX)**</span></span>](onexschema-singlesignon-onex-element.md)
</dt> </dl>

 

 
