---
description: Spécifie si l’appareil haut débit mobile se connecte automatiquement à un réseau.
ms.assetid: a2673ac7-6d70-4005-9ac4-cf670eba26ae
title: Élément AutoConnectOnInternet (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AutoConnectOnInternet
api_type:
- Schema
ms.openlocfilehash: fd08e93572d7d0af8b490ac079e3057413c469ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201537"
---
# <a name="autoconnectoninternet-mbnprofile-element"></a><span data-ttu-id="c4577-103">Élément AutoConnectOnInternet (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="c4577-103">AutoConnectOnInternet (MBNProfile) Element</span></span>

<span data-ttu-id="c4577-104">L’élément **AutoConnectOnInternet (MBNProfile)** spécifie si l’appareil haut débit mobile se connecte automatiquement à un réseau.</span><span class="sxs-lookup"><span data-stu-id="c4577-104">The **AutoConnectOnInternet (MBNProfile)** element specifies whether the Mobile Broadband device will automatically connect to a network.</span></span>

<span data-ttu-id="c4577-105">Si la valeur est **false**, la logique de connexion automatique du service haut débit mobile n’est pas utilisée si une autre connectivité réseau est disponible pour le système.</span><span class="sxs-lookup"><span data-stu-id="c4577-105">If set to **FALSE**, then the Mobile Broadband service's auto connect logic will not be used if there is any other network connectivity available to the system.</span></span> <span data-ttu-id="c4577-106">Si la valeur est **true**, le service haut débit mobile tente de connecter automatiquement l’appareil au réseau en fonction du paramètre de connexion automatique défini dans l’élément [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c4577-106">If set to **TRUE**, then the Mobile Broadband service will try to automatically connect the device to the network based on the auto connection setting defined in the [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md) element.</span></span>

<span data-ttu-id="c4577-107">**Windows 8 et versions ultérieures :** Cet élément est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="c4577-107">**Windows 8 and later:** This element is deprecated.</span></span> <span data-ttu-id="c4577-108">Utilisez la méthode [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) avec le paramètre *Property* défini sur **WCM \_ global \_ Property \_ Minimize \_ Policy** à la place.</span><span class="sxs-lookup"><span data-stu-id="c4577-108">Use the [**WcmSetProperty**](/windows/desktop/api/wcmapi/nf-wcmapi-wcmsetproperty) method with the *Property* parameter set to **wcm\_global\_property\_minimize\_policy** instead.</span></span>

``` syntax
<xs:element name="AutoConnectOnInternet"
    type="boolean"
 />
```

<span data-ttu-id="c4577-109">L’élément **AutoConnectOnInternet** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c4577-109">The **AutoConnectOnInternet** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4577-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4577-110">Requirements</span></span>



| <span data-ttu-id="c4577-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4577-111">Requirement</span></span> | <span data-ttu-id="c4577-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4577-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c4577-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4577-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c4577-114">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c4577-114">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c4577-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4577-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c4577-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4577-116">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c4577-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4577-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="c4577-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="c4577-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c4577-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="c4577-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="c4577-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="c4577-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c4577-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="c4577-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

