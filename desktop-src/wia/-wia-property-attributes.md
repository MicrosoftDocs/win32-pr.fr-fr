---
description: Tous les objets Item ont des propriétés.
ms.assetid: 00e04790-e319-41b3-b88f-8064912b91b1
title: Attributs de propriété (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c635cb0d4e21fe2a1d65a3f21254f8e9c04d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485057"
---
# <a name="property-attributes-wia"></a><span data-ttu-id="68421-103">Attributs de propriété (WIA)</span><span class="sxs-lookup"><span data-stu-id="68421-103">Property Attributes (WIA)</span></span>

<span data-ttu-id="68421-104">Tous les objets Item ont des propriétés.</span><span class="sxs-lookup"><span data-stu-id="68421-104">All item objects have properties.</span></span> <span data-ttu-id="68421-105">Les propriétés ont des attributs.</span><span class="sxs-lookup"><span data-stu-id="68421-105">The properties have attributes.</span></span> <span data-ttu-id="68421-106">Par exemple, les attributs de propriété indiquent si une propriété est lue, écrite ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="68421-106">For instance, property attributes indicate whether a property is read from, written to, or deleted.</span></span> <span data-ttu-id="68421-107">Ils indiquent également les valeurs de propriété valides.</span><span class="sxs-lookup"><span data-stu-id="68421-107">They also indicate the valid property values.</span></span> <span data-ttu-id="68421-108">Les constantes suivantes sont des attributs de propriété valides :</span><span class="sxs-lookup"><span data-stu-id="68421-108">The following constants are valid property attributes:</span></span> 

| <span data-ttu-id="68421-109">Attribut de propriété</span><span class="sxs-lookup"><span data-stu-id="68421-109">Property Attribute</span></span>        | <span data-ttu-id="68421-110">Signification</span><span class="sxs-lookup"><span data-stu-id="68421-110">Meaning</span></span>                                                                                                  |
|---------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68421-111">WIA \_ prop \_ cacheable</span><span class="sxs-lookup"><span data-stu-id="68421-111">WIA\_PROP\_CACHEABLE</span></span>      | <span data-ttu-id="68421-112">L’appareil peut mettre en cache la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="68421-112">The device can cache the property's value.</span></span>                                                               |
| <span data-ttu-id="68421-113">\_indicateur de prop WIA \_</span><span class="sxs-lookup"><span data-stu-id="68421-113">WIA\_PROP\_FLAG</span></span>           | <span data-ttu-id="68421-114">La propriété a une liste de valeurs d’indicateur autorisées.</span><span class="sxs-lookup"><span data-stu-id="68421-114">The property has a list of legal flag values.</span></span> <span data-ttu-id="68421-115">Les valeurs d’indicateur sont combinées à l’aide d' **une opération or** au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="68421-115">Flag values are combined using a bitwise **OR** operation.</span></span> |
| <span data-ttu-id="68421-116">\_liste de propriétés WIA \_</span><span class="sxs-lookup"><span data-stu-id="68421-116">WIA\_PROP\_LIST</span></span>           | <span data-ttu-id="68421-117">La propriété a une liste de valeurs autorisées.</span><span class="sxs-lookup"><span data-stu-id="68421-117">The property has a list of legal values.</span></span>                                                                 |
| <span data-ttu-id="68421-118">WIA \_ prop \_ None</span><span class="sxs-lookup"><span data-stu-id="68421-118">WIA\_PROP\_NONE</span></span>           | <span data-ttu-id="68421-119">Aucune valeur valide n’est associée à la propriété.</span><span class="sxs-lookup"><span data-stu-id="68421-119">The property does not have any valid values associated with it.</span></span>                                          |
| <span data-ttu-id="68421-120">\_plage de prop WIA \_</span><span class="sxs-lookup"><span data-stu-id="68421-120">WIA\_PROP\_RANGE</span></span>          | <span data-ttu-id="68421-121">La propriété a une plage de valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="68421-121">The property has a range of valid values.</span></span>                                                                |
| <span data-ttu-id="68421-122">\_lecture WIA prop \_</span><span class="sxs-lookup"><span data-stu-id="68421-122">WIA\_PROP\_READ</span></span>           | <span data-ttu-id="68421-123">L’application peut lire la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="68421-123">The application can read the property's value.</span></span>                                                           |
| <span data-ttu-id="68421-124">WIA \_ prop \_ RW</span><span class="sxs-lookup"><span data-stu-id="68421-124">WIA\_PROP\_RW</span></span>             | <span data-ttu-id="68421-125">L’application peut lire et écrire la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="68421-125">The application can read and write the property's value.</span></span>                                                 |
| <span data-ttu-id="68421-126">\_synchronisation WIA \_ prop \_ requise</span><span class="sxs-lookup"><span data-stu-id="68421-126">WIA\_PROP\_SYNC\_REQUIRED</span></span> | <span data-ttu-id="68421-127">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="68421-127">Do not use.</span></span>                                                                                              |
| <span data-ttu-id="68421-128">\_écriture WIA prop \_</span><span class="sxs-lookup"><span data-stu-id="68421-128">WIA\_PROP\_WRITE</span></span>          | <span data-ttu-id="68421-129">L’application peut écrire la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="68421-129">The application can write the property's value.</span></span>                                                          |



 

 

 



