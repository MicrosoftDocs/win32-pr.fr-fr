---
description: Identifie le nom du fournisseur d’hébergement pour la carte SIM/le périphérique donné.
ms.assetid: 05d65091-5a1d-427a-8f51-1e1b9d189571
title: Élément HomeProviderName (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HomeProviderName
api_type:
- Schema
ms.openlocfilehash: 3d0af51e4873915838f2d55f683d07e9098aad3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751292"
---
# <a name="homeprovidername-mbnprofile-element"></a><span data-ttu-id="d6242-103">Élément HomeProviderName (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="d6242-103">HomeProviderName (MBNProfile) Element</span></span>

<span data-ttu-id="d6242-104">L’élément **HomeProviderName (MBNProfile)** identifie le nom du fournisseur d’hébergement pour la carte SIM/le périphérique donné.</span><span class="sxs-lookup"><span data-stu-id="d6242-104">The **HomeProviderName (MBNProfile)** element identifies the name of Home provider for the given SIM/Device.</span></span>

<span data-ttu-id="d6242-105">Cet élément est facultatif et est défini par le service haut débit mobile pour une utilisation interne.</span><span class="sxs-lookup"><span data-stu-id="d6242-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="d6242-106">Une application ne doit pas définir ce champ lors de la création ou de la mise à jour d’un profil.</span><span class="sxs-lookup"><span data-stu-id="d6242-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="HomeProviderName"
    type="providerNameType"
 />
```

<span data-ttu-id="d6242-107">L’élément **HomeProviderName** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d6242-107">The **HomeProviderName** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6242-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6242-108">Requirements</span></span>



| <span data-ttu-id="d6242-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6242-109">Requirement</span></span> | <span data-ttu-id="d6242-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6242-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d6242-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6242-111">Minimum supported client</span></span><br/> | <span data-ttu-id="d6242-112">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6242-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d6242-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6242-113">Minimum supported server</span></span><br/> | <span data-ttu-id="d6242-114">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6242-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="d6242-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6242-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6242-116">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="d6242-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d6242-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d6242-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="d6242-118">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="d6242-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d6242-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d6242-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




