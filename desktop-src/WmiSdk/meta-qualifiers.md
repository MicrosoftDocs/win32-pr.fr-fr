---
description: Les méta-qualificateurs affinent la définition des méta-constructions dans le modèle CIM en clarifiant l’utilisation réelle d’une déclaration de classe ou de propriété dans la syntaxe MOF.
ms.assetid: 3674a051-3756-4d09-a70e-46a57b442104
ms.tgt_platform: multiple
title: Qualificateurs méta
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8618ef8258f403a43e08be54b3acbd5bb1e923c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521827"
---
# <a name="meta-qualifiers"></a><span data-ttu-id="80fd5-103">Qualificateurs méta</span><span class="sxs-lookup"><span data-stu-id="80fd5-103">Meta Qualifiers</span></span>

<span data-ttu-id="80fd5-104">Les méta-qualificateurs affinent la définition des méta-constructions dans le modèle CIM en clarifiant l’utilisation réelle d’une déclaration de classe ou de propriété dans la syntaxe MOF.</span><span class="sxs-lookup"><span data-stu-id="80fd5-104">Meta qualifiers refine the definition of meta-constructs in the CIM model by clarifying the actual usage of a class or property declaration within the MOF syntax.</span></span>

<dt>

<span data-ttu-id="80fd5-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Association**</span><span class="sxs-lookup"><span data-stu-id="80fd5-105"><span id="Association"></span><span id="association"></span><span id="ASSOCIATION"></span>**Association**</span></span>
</dt> <dd>

<span data-ttu-id="80fd5-106">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80fd5-106">Data type: **boolean**</span></span>

<span data-ttu-id="80fd5-107">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="80fd5-107">Applies to: classes</span></span>

<span data-ttu-id="80fd5-108">Indique si la classe est une classe d’association utilisée pour décrire une relation entre deux autres classes.</span><span class="sxs-lookup"><span data-stu-id="80fd5-108">Indicates whether the class is an association class used to describe a relationship between two other classes.</span></span> <span data-ttu-id="80fd5-109">L’absence de ce qualificateur indique que la classe n’est pas une classe d’association.</span><span class="sxs-lookup"><span data-stu-id="80fd5-109">The absence of this qualifier indicates that the class is not an association class.</span></span> <span data-ttu-id="80fd5-110">Ce qualificateur s’exclut mutuellement avec l' **indication**.</span><span class="sxs-lookup"><span data-stu-id="80fd5-110">This qualifier is mutually exclusive with **Indication**.</span></span> <span data-ttu-id="80fd5-111">Pour plus d’informations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="80fd5-111">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span>

</dd> <dt>

<span data-ttu-id="80fd5-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indication**</span><span class="sxs-lookup"><span data-stu-id="80fd5-112"><span id="Indication"></span><span id="indication"></span><span id="INDICATION"></span>**Indication**</span></span>
</dt> <dd>

<span data-ttu-id="80fd5-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80fd5-113">Data type: **boolean**</span></span>

<span data-ttu-id="80fd5-114">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="80fd5-114">Applies to: classes</span></span>

<span data-ttu-id="80fd5-115">Indique si la classe d’objets définit une indication.</span><span class="sxs-lookup"><span data-stu-id="80fd5-115">Indicates whether the object class defines an indication.</span></span> <span data-ttu-id="80fd5-116">Ce qualificateur s’exclut mutuellement avec l' **Association**.</span><span class="sxs-lookup"><span data-stu-id="80fd5-116">This qualifier is mutually exclusive with **Association**.</span></span> <span data-ttu-id="80fd5-117">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="80fd5-117">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80fd5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80fd5-118">Requirements</span></span>



| <span data-ttu-id="80fd5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80fd5-119">Requirement</span></span> | <span data-ttu-id="80fd5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="80fd5-120">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="80fd5-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80fd5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="80fd5-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80fd5-122">Windows Vista</span></span><br/>       |
| <span data-ttu-id="80fd5-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80fd5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="80fd5-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80fd5-124">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80fd5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80fd5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80fd5-126">Qualificateurs WMI</span><span class="sxs-lookup"><span data-stu-id="80fd5-126">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="80fd5-127">Ajout d’un qualificateur</span><span class="sxs-lookup"><span data-stu-id="80fd5-127">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




