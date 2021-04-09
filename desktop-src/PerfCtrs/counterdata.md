---
description: La table CounterData contient une ligne pour chaque compteur qui est collecté à un moment donné. Il y aura un grand nombre de ces lignes.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: CounterData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865126"
---
# <a name="counterdata"></a><span data-ttu-id="cd3a4-104">CounterData</span><span class="sxs-lookup"><span data-stu-id="cd3a4-104">CounterData</span></span>

<span data-ttu-id="cd3a4-105">La table **CounterData** contient une ligne pour chaque compteur qui est collecté à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-105">The **CounterData** table contains a row for each counter that is collected at a particular time.</span></span> <span data-ttu-id="cd3a4-106">Il y aura un grand nombre de ces lignes.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-106">There will be a large number of these rows.</span></span>

<span data-ttu-id="cd3a4-107">La table **CounterData** définit les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="cd3a4-107">The **CounterData** table defines the following fields:</span></span>

-   <span data-ttu-id="cd3a4-108">**GUID :** GUID de ce jeu de données.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-108">**GUID:** GUID for this data set.</span></span> <span data-ttu-id="cd3a4-109">Utilisez cette clé pour joindre la table [**DisplayToID**](displaytoid.md) .</span><span class="sxs-lookup"><span data-stu-id="cd3a4-109">Use this key to join with the [**DisplayToID**](displaytoid.md) table.</span></span>
-   <span data-ttu-id="cd3a4-110">**CounterID :** Identifie le compteur.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-110">**CounterID:** Identifies the counter.</span></span> <span data-ttu-id="cd3a4-111">Utilisez cette clé pour joindre la table [**CounterDetails**](counterdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="cd3a4-111">Use this key to join with the [**CounterDetails**](counterdetails.md) table.</span></span>
-   <span data-ttu-id="cd3a4-112">**RecordIndex :** L’exemple d’index pour un identificateur de compteur et un GUID de collection spécifiques.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-112">**RecordIndex:** The sample index for a specific counter identifier and collection GUID.</span></span> <span data-ttu-id="cd3a4-113">La valeur augmente pour chaque échantillon successif dans ce fichier journal.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-113">The value increases for each successive sample in this log file.</span></span>
-   <span data-ttu-id="cd3a4-114">**CounterDateTime :** Heure à laquelle la collection a été démarrée, en heure UTC.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-114">**CounterDateTime:** The time the collection was started, in UTC time.</span></span>
-   <span data-ttu-id="cd3a4-115">**CounterValue :** Valeur mise en forme du compteur.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-115">**CounterValue:** The formatted value of the counter.</span></span> <span data-ttu-id="cd3a4-116">Cette valeur peut être égale à zéro pour le premier enregistrement si le compteur requiert deux exemples pour calculer une valeur affichable.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-116">This value may be zero for the first record if the counter requires two sample to compute a displayable value.</span></span>
-   <span data-ttu-id="cd3a4-117">**FirstValueA :** Associez cette valeur 32 bits à la valeur de **FirstValueB** pour créer le membre **FirstValue** du [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="cd3a4-117">**FirstValueA:** Combine this 32-bit value with the value of **FirstValueB** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="cd3a4-118">**FirstValueA** contient les bits de poids faible.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-118">**FirstValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="cd3a4-119">**FirstValueB :** Associez cette valeur 32 bits à la valeur de **FirstValueA** pour créer le membre **FirstValue** du [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="cd3a4-119">**FirstValueB:** Combine this 32-bit value with the value of **FirstValueA** to create the **FirstValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="cd3a4-120">**FirstValueB** contient les bits de poids fort.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-120">**FirstValueB** contains the high order bits.</span></span>
-   <span data-ttu-id="cd3a4-121">**SecondValueA :** Associez cette valeur 32 bits à la valeur de **SecondValueB** pour créer le membre **SecondValue** du [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="cd3a4-121">**SecondValueA:** Combine this 32-bit value with the value of **SecondValueB** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="cd3a4-122">**SecondValueA** contient les bits de poids faible.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-122">**SecondValueA** contains the low order bits.</span></span>
-   <span data-ttu-id="cd3a4-123">**SecondValueB :** Associez cette valeur 32 bits à la valeur de **SecondValueA** pour créer le membre **SecondValue** du [**\_ \_ compteur brut PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span><span class="sxs-lookup"><span data-stu-id="cd3a4-123">**SecondValueB:** Combine this 32-bit value with the value of **SecondValueA** to create the **SecondValue** member of [**PDH\_RAW\_COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter).</span></span> <span data-ttu-id="cd3a4-124">**SecondValueB** contient les bits de poids fort.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-124">**SecondValueB** contains the high order bits.</span></span>

<span data-ttu-id="cd3a4-125">Les champs **GUID**, **CounterID** et **RecordIndex** constituent la clé primaire de cette table.</span><span class="sxs-lookup"><span data-stu-id="cd3a4-125">The **GUID**, **CounterID**, and **RecordIndex** fields make up the primary key for this table.</span></span>

 

 



