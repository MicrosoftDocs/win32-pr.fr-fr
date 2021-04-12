---
description: Spécifie si les réseaux refusés s’affichent dans l’Assistant Connexion à un réseau.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Élément showDeniedNetwork (globalFlags)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527801"
---
# <a name="showdeniednetwork-globalflags-element"></a><span data-ttu-id="623e8-103">Élément showDeniedNetwork (globalFlags)</span><span class="sxs-lookup"><span data-stu-id="623e8-103">showDeniedNetwork (globalFlags) Element</span></span>

<span data-ttu-id="623e8-104">L’élément **showDeniedNetwork** (globalFlags) spécifie si les réseaux refusés s’affichent dans l’Assistant **connexion à un réseau** .</span><span class="sxs-lookup"><span data-stu-id="623e8-104">The **showDeniedNetwork** (globalFlags) element specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <span data-ttu-id="623e8-105">Les réseaux peuvent être refusés par la stratégie de groupe ou par les paramètres utilisateur.</span><span class="sxs-lookup"><span data-stu-id="623e8-105">Networks may be denied by group policy or by user settings.</span></span> <span data-ttu-id="623e8-106">Lorsque **showDeniedNetwork** a la valeur true, les réseaux refusés s’affichent dans l’Assistant **connexion à un réseau** . dans le cas contraire, les réseaux refusés n’apparaissent pas dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="623e8-106">When **showDeniedNetwork** has a value of TRUE, denied networks appear in the **Connect to a Network** wizard; otherwise, denied networks do not appear in the wizard.</span></span>

<span data-ttu-id="623e8-107">Cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="623e8-107">This element is mandatory.</span></span> <span data-ttu-id="623e8-108">Lorsqu’un profil est créé par le service de configuration automatique, cet élément prend la valeur par défaut FALSe.</span><span class="sxs-lookup"><span data-stu-id="623e8-108">When a profile is created by the AutoConfig service, this element will take the default value of FALSE.</span></span>

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

<span data-ttu-id="623e8-109">L’élément **showDeniedNetwork** est défini par l’élément [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="623e8-109">The **showDeniedNetwork** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="623e8-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="623e8-110">Requirements</span></span>



| <span data-ttu-id="623e8-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="623e8-111">Requirement</span></span> | <span data-ttu-id="623e8-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="623e8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="623e8-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="623e8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="623e8-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="623e8-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="623e8-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="623e8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="623e8-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="623e8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="623e8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="623e8-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="623e8-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="623e8-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="623e8-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="623e8-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="623e8-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="623e8-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="623e8-121">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="623e8-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




