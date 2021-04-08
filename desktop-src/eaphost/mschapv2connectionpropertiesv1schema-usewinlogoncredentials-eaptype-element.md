---
title: Élément UseWinLogonCredentials (EapType)
description: En savoir plus sur l’élément UseWinLogonCredentials (EapType). Cet élément contrôle l’utilisation des informations d’identification winlogin.
ms.assetid: 8ebd87ce-7d2b-4305-b50c-239bb9c7af75
keywords:
- Élément UseWinLogonCredentials EAPHost
topic_type:
- apiref
api_name:
- UseWinLogonCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f17520d4eaee64d3dd9809ecb465ca8e39690fc4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730372"
---
# <a name="usewinlogoncredentials-eaptype-element"></a><span data-ttu-id="88fca-105">Élément UseWinLogonCredentials (EapType)</span><span class="sxs-lookup"><span data-stu-id="88fca-105">UseWinLogonCredentials (EapType) Element</span></span>

<span data-ttu-id="88fca-106">L’élément **UseWinLogonCredentials (EapType)** contrôle l’utilisation des informations d’identification winlogin.</span><span class="sxs-lookup"><span data-stu-id="88fca-106">The **UseWinLogonCredentials (EapType)** element controls use of the winlogin credentials.</span></span>

``` syntax
<xs:element name="UseWinLogonCredentials"
    type="boolean"
 />
```

<span data-ttu-id="88fca-107">L’élément **UseWinLogonCredentials** est défini par l’élément [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="88fca-107">The **UseWinLogonCredentials** element is defined by the [**EapType**](mschapv2connectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="88fca-108">Notes</span><span class="sxs-lookup"><span data-stu-id="88fca-108">Remarks</span></span>

<span data-ttu-id="88fca-109">Si la valeur est TRUE, EAP MS-CHAPv2 obtient les informations d’identification de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="88fca-109">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="88fca-110">Si la valeur est FALSe, EAP MS-CHAPv2 obtient les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="88fca-110">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <span data-ttu-id="88fca-111">L’élément **UseWinLogonCredentials (EapType)** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="88fca-111">The **UseWinLogonCredentials (EapType)** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="88fca-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88fca-112">Requirements</span></span>



| <span data-ttu-id="88fca-113">Role</span><span class="sxs-lookup"><span data-stu-id="88fca-113">Role</span></span> | <span data-ttu-id="88fca-114">Versions de système d’exploitation minimales prises en charge</span><span class="sxs-lookup"><span data-stu-id="88fca-114">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="88fca-115">Client</span><span class="sxs-lookup"><span data-stu-id="88fca-115">Client</span></span><br/> | <span data-ttu-id="88fca-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88fca-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88fca-117">Serveur</span><span class="sxs-lookup"><span data-stu-id="88fca-117">Server</span></span><br/> | <span data-ttu-id="88fca-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88fca-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88fca-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88fca-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="88fca-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="88fca-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="88fca-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="88fca-121">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="88fca-122">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="88fca-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="88fca-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="88fca-123">**EapType**</span></span>](mschapv2connectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="88fca-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="88fca-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="88fca-125">Schéma mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="88fca-125">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





