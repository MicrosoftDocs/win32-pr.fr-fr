---
title: Élément UserCert (EapType)
description: Fait référence au hachage SHA-1 du certificat qui doit être utilisé pour l’authentification.
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- Élément UserCert EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c23840b489bad1e06bdd0c7eb6e0033bfb1961f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743197"
---
# <a name="usercert-eaptype-element"></a><span data-ttu-id="2abde-104">Élément UserCert (EapType)</span><span class="sxs-lookup"><span data-stu-id="2abde-104">UserCert (EapType) Element</span></span>

<span data-ttu-id="2abde-105">L’élément **UserCert (EapType)** fait référence au hachage SHA-1 du certificat qui doit être utilisé pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="2abde-105">The **UserCert (EapType)** element refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span>

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

<span data-ttu-id="2abde-106">L’élément **UserCert** est défini par l’élément [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2abde-106">The **UserCert** element is defined by the [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2abde-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2abde-107">Requirements</span></span>



| <span data-ttu-id="2abde-108">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2abde-108">Requirement</span></span> | <span data-ttu-id="2abde-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="2abde-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2abde-110">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2abde-110">Minimum supported client</span></span><br/> | <span data-ttu-id="2abde-111">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2abde-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2abde-112">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2abde-112">Minimum supported server</span></span><br/> | <span data-ttu-id="2abde-113">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2abde-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2abde-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2abde-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="2abde-115">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="2abde-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2abde-116">**EapType**</span><span class="sxs-lookup"><span data-stu-id="2abde-116">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="2abde-117">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="2abde-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2abde-118">**EapType**</span><span class="sxs-lookup"><span data-stu-id="2abde-118">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="2abde-119">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="2abde-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2abde-120">Schéma eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2abde-120">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





