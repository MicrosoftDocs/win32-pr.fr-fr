---
description: Spécifie si les informations d’identification de l’utilisateur sont mises en cache pour les connexions suivantes.
ms.assetid: 65ed03f1-f61e-46f8-a666-91b393618de3
title: Élément cacheUserData (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- cacheUserData
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8650bb2e5899e96f921d57460c8ba49ffab0ea66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951900"
---
# <a name="cacheuserdata-onex-element"></a><span data-ttu-id="43349-103">Élément cacheUserData (OneX)</span><span class="sxs-lookup"><span data-stu-id="43349-103">cacheUserData (OneX) Element</span></span>

<span data-ttu-id="43349-104">L’élément cacheUserData (OneX) spécifie si les informations d’identification de l’utilisateur sont mises en cache pour les connexions suivantes.</span><span class="sxs-lookup"><span data-stu-id="43349-104">The cacheUserData (OneX) element specifies whether the user credentials are cached for subsequent connections.</span></span> <span data-ttu-id="43349-105">Quand cacheUserData a la valeur TRUE, les informations d’identification sont mises en cache.</span><span class="sxs-lookup"><span data-stu-id="43349-105">When cacheUserData is TRUE, the credentials are cached.</span></span> <span data-ttu-id="43349-106">Quand cacheUserData a la valeur FALSe, les informations d’identification ne sont pas mises en cache et l’utilisateur peut être invité à entrer des informations d’identification lors des tentatives de connexion suivantes.</span><span class="sxs-lookup"><span data-stu-id="43349-106">When cacheUserData is FALSE, the credentials are not cached and the user may be prompted for credentials on subsequent connection attempts.</span></span>

<span data-ttu-id="43349-107">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="43349-107">This element is optional.</span></span> <span data-ttu-id="43349-108">Quand cacheUserData n’est pas spécifié dans un profil, les informations d’identification de l’utilisateur sont mises en cache.</span><span class="sxs-lookup"><span data-stu-id="43349-108">When cacheUserData is not specified in a profile, the user credentials are cached.</span></span>

<span data-ttu-id="43349-109">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="43349-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="cacheUserData"
    type="boolean"
 />
```

<span data-ttu-id="43349-110">L’élément **cacheUserData** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="43349-110">The **cacheUserData** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="43349-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43349-111">Requirements</span></span>



| <span data-ttu-id="43349-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43349-112">Requirement</span></span> | <span data-ttu-id="43349-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="43349-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43349-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43349-114">Minimum supported client</span></span><br/> | <span data-ttu-id="43349-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43349-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="43349-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43349-116">Minimum supported server</span></span><br/> | <span data-ttu-id="43349-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43349-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43349-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43349-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="43349-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="43349-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="43349-120">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="43349-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="43349-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="43349-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="43349-122">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="43349-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




