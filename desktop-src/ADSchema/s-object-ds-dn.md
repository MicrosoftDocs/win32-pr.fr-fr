---
title: Syntaxe de l’objet (DS-DN)
description: Chaîne qui contient un nom unique (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Syntaxe d’objet (DS-DN) schéma Active Directory
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104519353"
---
# <a name="objectds-dn-syntax"></a><span data-ttu-id="767ad-104">Syntaxe de l’objet (DS-DN)</span><span class="sxs-lookup"><span data-stu-id="767ad-104">Object(DS-DN) syntax</span></span>

<span data-ttu-id="767ad-105">Chaîne qui contient un nom unique (DN).</span><span class="sxs-lookup"><span data-stu-id="767ad-105">String that contains a distinguished name (DN).</span></span> <span data-ttu-id="767ad-106">Pour les attributs avec cette syntaxe, Active Directory gère les valeurs d’attribut en tant que références à l’objet identifié par le DN et met automatiquement à jour la valeur si l’objet est déplacé ou renommé.</span><span class="sxs-lookup"><span data-stu-id="767ad-106">For attributes with this syntax, Active Directory handles attribute values as references to the object identified by the DN and automatically updates the value if the object is moved or renamed.</span></span> <span data-ttu-id="767ad-107">Pour les requêtes qui incluent des attributs de syntaxe DN dans un filtre, spécifiez des noms uniques complets.</span><span class="sxs-lookup"><span data-stu-id="767ad-107">For queries that include attributes of DN syntax in a filter, specify full distinguished names.</span></span> <span data-ttu-id="767ad-108">Les caractères génériques (par exemple, CN = John \* ) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="767ad-108">Wildcards (for example, cn=John\*) are not supported.</span></span>



| <span data-ttu-id="767ad-109">Entrée</span><span class="sxs-lookup"><span data-stu-id="767ad-109">Entry</span></span> | <span data-ttu-id="767ad-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="767ad-110">Value</span></span> |
|--------------|------------------------------------------------------------------------|
| <span data-ttu-id="767ad-111">Nom</span><span class="sxs-lookup"><span data-stu-id="767ad-111">Name</span></span>         | <span data-ttu-id="767ad-112">Object(DS-DN)</span><span class="sxs-lookup"><span data-stu-id="767ad-112">Object(DS-DN)</span></span>                                                          |
| <span data-ttu-id="767ad-113">ID de syntaxe</span><span class="sxs-lookup"><span data-stu-id="767ad-113">Syntax ID</span></span>    | <span data-ttu-id="767ad-114">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="767ad-114">2.5.5.1</span></span>                                                                |
| <span data-ttu-id="767ad-115">ID OM</span><span class="sxs-lookup"><span data-stu-id="767ad-115">OM ID</span></span>        | <span data-ttu-id="767ad-116">127</span><span class="sxs-lookup"><span data-stu-id="767ad-116">127</span></span>                                                                    |
| <span data-ttu-id="767ad-117">Type MAPI</span><span class="sxs-lookup"><span data-stu-id="767ad-117">MAPI Type</span></span>    | <span data-ttu-id="767ad-118">OBJECT</span><span class="sxs-lookup"><span data-stu-id="767ad-118">OBJECT</span></span>                                                                 |
| <span data-ttu-id="767ad-119">Type ADS</span><span class="sxs-lookup"><span data-stu-id="767ad-119">ADS Type</span></span>     | <span data-ttu-id="767ad-120">\_chaîne DN \_ ADSTYPE</span><span class="sxs-lookup"><span data-stu-id="767ad-120">ADSTYPE\_DN\_STRING</span></span>                                                    |
| <span data-ttu-id="767ad-121">Type de variante</span><span class="sxs-lookup"><span data-stu-id="767ad-121">Variant Type</span></span> | <span data-ttu-id="767ad-122">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="767ad-122">VT\_BSTR</span></span>                                                               |
| <span data-ttu-id="767ad-123">SDS, type</span><span class="sxs-lookup"><span data-stu-id="767ad-123">SDS Type</span></span>     | [<span data-ttu-id="767ad-124">System.String</span><span class="sxs-lookup"><span data-stu-id="767ad-124">System.String</span></span>](/dotnet/api/system.string) |



## <a name="see-also"></a><span data-ttu-id="767ad-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="767ad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767ad-126">System.String</span><span class="sxs-lookup"><span data-stu-id="767ad-126">System.String</span></span>](/dotnet/api/system.string)
</dt> </dl>

 

 
