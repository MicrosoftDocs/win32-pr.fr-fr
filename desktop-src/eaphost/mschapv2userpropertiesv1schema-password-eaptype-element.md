---
title: Élément Password (EapType)
description: En savoir plus sur l’élément Password (EapType). Cet élément identifie le mot de passe de l’utilisateur ou de l’ordinateur en cours d’authentification.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Élément Password EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031874"
---
# <a name="password-eaptype-element"></a><span data-ttu-id="6fa78-105">Élément Password (EapType)</span><span class="sxs-lookup"><span data-stu-id="6fa78-105">Password (EapType) Element</span></span>

<span data-ttu-id="6fa78-106">L’élément **Password (EapType)** identifie le mot de passe de l’utilisateur ou de l’ordinateur en cours d’authentification.</span><span class="sxs-lookup"><span data-stu-id="6fa78-106">The **Password (EapType)** element identifies the password of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="6fa78-107">L’élément **Password** est défini par l’élément [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6fa78-107">The **Password** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fa78-108">Notes</span><span class="sxs-lookup"><span data-stu-id="6fa78-108">Remarks</span></span>

<span data-ttu-id="6fa78-109">Si l’élément **Password (EapType)** n’est pas présent, le hachage de mot de passe est obtenu à partir de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="6fa78-109">If the **Password (EapType)** element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="6fa78-110">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6fa78-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa78-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fa78-111">Requirements</span></span>



| <span data-ttu-id="6fa78-112">Role</span><span class="sxs-lookup"><span data-stu-id="6fa78-112">Role</span></span> | <span data-ttu-id="6fa78-113">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="6fa78-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="6fa78-114">Client</span><span class="sxs-lookup"><span data-stu-id="6fa78-114">Client</span></span><br/> | <span data-ttu-id="6fa78-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fa78-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6fa78-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="6fa78-116">Server</span></span><br/> | <span data-ttu-id="6fa78-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fa78-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6fa78-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fa78-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="6fa78-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="6fa78-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6fa78-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="6fa78-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="6fa78-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="6fa78-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6fa78-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="6fa78-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="6fa78-123">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="6fa78-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6fa78-124">Schéma mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6fa78-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





