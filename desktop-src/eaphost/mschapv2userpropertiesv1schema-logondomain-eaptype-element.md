---
title: Élément LogonDomain (EapType)
description: En savoir plus sur l’élément LogonDomain (EapType). Cet élément identifie le domaine de l’utilisateur ou de l’ordinateur en cours d’authentification.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Élément LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031844"
---
# <a name="logondomain-eaptype-element"></a><span data-ttu-id="900fe-105">Élément LogonDomain (EapType)</span><span class="sxs-lookup"><span data-stu-id="900fe-105">LogonDomain (EapType) Element</span></span>

<span data-ttu-id="900fe-106">L’élément **LogonDomain (EapType)** identifie le domaine de l’utilisateur ou de l’ordinateur en cours d’authentification.</span><span class="sxs-lookup"><span data-stu-id="900fe-106">The **LogonDomain (EapType)** element identifies the domain of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

<span data-ttu-id="900fe-107">L’élément **LogonDomain** est défini par l’élément [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="900fe-107">The **LogonDomain** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="900fe-108">Notes</span><span class="sxs-lookup"><span data-stu-id="900fe-108">Remarks</span></span>

<span data-ttu-id="900fe-109">Si l’élément **LogonDomain (EapType)** n’est pas présent, le domaine de Winlogon est utilisé.</span><span class="sxs-lookup"><span data-stu-id="900fe-109">If the **LogonDomain (EapType)** element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="900fe-110">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="900fe-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="900fe-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="900fe-111">Requirements</span></span>



| <span data-ttu-id="900fe-112">Role</span><span class="sxs-lookup"><span data-stu-id="900fe-112">Role</span></span> | <span data-ttu-id="900fe-113">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="900fe-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="900fe-114">Client</span><span class="sxs-lookup"><span data-stu-id="900fe-114">Client</span></span><br/> | <span data-ttu-id="900fe-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="900fe-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="900fe-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="900fe-116">Server</span></span><br/> | <span data-ttu-id="900fe-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="900fe-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="900fe-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="900fe-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="900fe-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="900fe-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="900fe-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="900fe-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="900fe-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="900fe-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="900fe-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="900fe-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="900fe-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="900fe-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="900fe-124">Schéma mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="900fe-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





