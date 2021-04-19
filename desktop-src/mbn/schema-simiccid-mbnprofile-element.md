---
description: Identifie le numéro d’identification SIM pour les appareils GSM.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: Élément SimIccID (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532085"
---
# <a name="simiccid-mbnprofile-element"></a><span data-ttu-id="b97d8-103">Élément SimIccID (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="b97d8-103">SimIccID (MBNProfile) Element</span></span>

<span data-ttu-id="b97d8-104">L’élément **SimIccID (MBNProfile)** identifie le numéro d’identification SIM pour les appareils GSM.</span><span class="sxs-lookup"><span data-stu-id="b97d8-104">The **SimIccID (MBNProfile)** element identifies the SIM Identification number for GSM devices.</span></span>

<span data-ttu-id="b97d8-105">Cet élément est facultatif et est défini par le service haut débit mobile pour une utilisation interne.</span><span class="sxs-lookup"><span data-stu-id="b97d8-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="b97d8-106">Une application ne doit pas définir ce champ lors de la création ou de la mise à jour d’un profil.</span><span class="sxs-lookup"><span data-stu-id="b97d8-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

<span data-ttu-id="b97d8-107">L’élément **SimIccID** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b97d8-107">The **SimIccID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="b97d8-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b97d8-108">Requirements</span></span>



| <span data-ttu-id="b97d8-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b97d8-109">Requirement</span></span> | <span data-ttu-id="b97d8-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b97d8-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="b97d8-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b97d8-111">Minimum supported client</span></span><br/> | <span data-ttu-id="b97d8-112">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b97d8-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="b97d8-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b97d8-113">Minimum supported server</span></span><br/> | <span data-ttu-id="b97d8-114">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b97d8-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="b97d8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b97d8-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="b97d8-116">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="b97d8-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="b97d8-117">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="b97d8-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="b97d8-118">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="b97d8-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="b97d8-119">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="b97d8-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




