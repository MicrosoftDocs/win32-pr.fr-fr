---
description: Spécifie les paramètres requis pour configurer une connexion de données.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Élément context (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516272"
---
# <a name="context-mbnprofile-element"></a><span data-ttu-id="2534f-103">Élément context (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="2534f-103">Context (MBNProfile) Element</span></span>

<span data-ttu-id="2534f-104">L’élément **Context (MBNProfile)** spécifie les paramètres requis pour configurer une connexion de données.</span><span class="sxs-lookup"><span data-stu-id="2534f-104">The **Context (MBNProfile)** element specifies the parameters required to setup a data connection.</span></span>

<span data-ttu-id="2534f-105">L’élément peut avoir les éléments enfants suivants.</span><span class="sxs-lookup"><span data-stu-id="2534f-105">The element can have the following child elements.</span></span>

-   [<span data-ttu-id="2534f-106">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="2534f-106">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)
-   [<span data-ttu-id="2534f-107">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="2534f-107">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
-   [<span data-ttu-id="2534f-108">**Compressé**</span><span class="sxs-lookup"><span data-stu-id="2534f-108">**Compression**</span></span>](schema-compression-contexttype-element.md)
-   [<span data-ttu-id="2534f-109">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="2534f-109">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)

<span data-ttu-id="2534f-110">Cet élément peut avoir au maximum une occurrence.</span><span class="sxs-lookup"><span data-stu-id="2534f-110">This element can have a maximum of one occurrence.</span></span>

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

<span data-ttu-id="2534f-111">L’élément **Context** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2534f-111">The **Context** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2534f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2534f-112">Requirements</span></span>



| <span data-ttu-id="2534f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2534f-113">Requirement</span></span> | <span data-ttu-id="2534f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="2534f-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="2534f-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2534f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2534f-116">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2534f-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2534f-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2534f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2534f-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2534f-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="2534f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2534f-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="2534f-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="2534f-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2534f-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="2534f-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="2534f-122">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="2534f-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2534f-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="2534f-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




