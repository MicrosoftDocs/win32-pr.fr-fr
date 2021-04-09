---
description: La table CounterDetails décrit un compteur spécifique sur un ordinateur particulier.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: CounterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952018"
---
# <a name="counterdetails"></a><span data-ttu-id="fd973-103">CounterDetails</span><span class="sxs-lookup"><span data-stu-id="fd973-103">CounterDetails</span></span>

<span data-ttu-id="fd973-104">La table **CounterDetails** décrit un compteur spécifique sur un ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="fd973-104">The **CounterDetails** table describes a specific counter on a particular computer.</span></span>

<span data-ttu-id="fd973-105">La table **CounterDetails** définit les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="fd973-105">The **CounterDetails** table defines the following fields:</span></span>

-   <span data-ttu-id="fd973-106">**CounterID :** Identificateur unique dans la base de données qui mappe à une chaîne de texte de nom de compteur spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd973-106">**CounterID:** A unique identifier in the database that maps to a specific counter name text string.</span></span> <span data-ttu-id="fd973-107">Ce champ est la clé primaire de cette table.</span><span class="sxs-lookup"><span data-stu-id="fd973-107">This field is the primary key of this table.</span></span>
-   <span data-ttu-id="fd973-108">**MachineName :** Nom de l’ordinateur qui a enregistré ce jeu de données.</span><span class="sxs-lookup"><span data-stu-id="fd973-108">**MachineName:** The name of the computer that logged this data set.</span></span>
-   <span data-ttu-id="fd973-109">**ObjectName :** Nom de l’objet de performance.</span><span class="sxs-lookup"><span data-stu-id="fd973-109">**ObjectName:** The name of the performance object.</span></span>
-   <span data-ttu-id="fd973-110">**CounterName :** Nom du compteur.</span><span class="sxs-lookup"><span data-stu-id="fd973-110">**CounterName:** The name of the counter.</span></span>
-   <span data-ttu-id="fd973-111">Au-dessus de **:** Type de compteur.</span><span class="sxs-lookup"><span data-stu-id="fd973-111">**CounterType:** The counter type.</span></span> <span data-ttu-id="fd973-112">Pour obtenir la liste des types de compteurs et leurs formules, consultez la section types de compteurs du [Kit de déploiement de Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="fd973-112">For a list of counter types and their formulas, see the Counter Types section of the [Windows Server 2003 Deployment Kit](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).</span></span>
-   <span data-ttu-id="fd973-113">**DEFAULTSCALE :** Mise à l’échelle par défaut à appliquer aux données de compteur de performances brutes.</span><span class="sxs-lookup"><span data-stu-id="fd973-113">**DefaultScale:** The default scaling to be applied to the raw performance counter data.</span></span>
-   <span data-ttu-id="fd973-114">**Nom_instance :** Nom de l’instance de compteur.</span><span class="sxs-lookup"><span data-stu-id="fd973-114">**InstanceName:** The name of the counter instance.</span></span>
-   <span data-ttu-id="fd973-115">**InstanceIndex :** Numéro d’index de l’instance de compteur.</span><span class="sxs-lookup"><span data-stu-id="fd973-115">**InstanceIndex:** The index number of the counter instance.</span></span>
-   <span data-ttu-id="fd973-116">**ParentName :** Certains compteurs sont logiquement associés à d’autres, et sont appelés parents.</span><span class="sxs-lookup"><span data-stu-id="fd973-116">**ParentName:** Some counters are logically associated with others, and are referred to as parents.</span></span> <span data-ttu-id="fd973-117">Par exemple, le parent d’un thread est un processus et le parent d’un pilote de disque logique est un lecteur physique.</span><span class="sxs-lookup"><span data-stu-id="fd973-117">For example, the parent of a thread is a process and the parent of a logical disk driver is a physical drive.</span></span> <span data-ttu-id="fd973-118">Ce champ contient le nom du parent.</span><span class="sxs-lookup"><span data-stu-id="fd973-118">This field contains the name of the parent.</span></span> <span data-ttu-id="fd973-119">Soit la valeur de ce champ, soit le champ **ParentObjectID** identifie une instance parent spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd973-119">Either the value in this field or the **ParentObjectID** field identifies a specific parent instance.</span></span> <span data-ttu-id="fd973-120">Si la valeur de ce champ est **null**, la valeur du champ **ParentObjectID** doit être vérifiée pour identifier le parent.</span><span class="sxs-lookup"><span data-stu-id="fd973-120">If the value in this field is **NULL**, the value in the **ParentObjectID** field must be checked to identify the parent.</span></span> <span data-ttu-id="fd973-121">Si les valeurs des deux champs sont **null**, le compteur n’a pas de parent.</span><span class="sxs-lookup"><span data-stu-id="fd973-121">If the values in both fields are **NULL**, the counter does not have a parent.</span></span>
-   <span data-ttu-id="fd973-122">**ParentObjectID :** Identificateur unique du parent.</span><span class="sxs-lookup"><span data-stu-id="fd973-122">**ParentObjectID:** The unique identifier of the parent.</span></span> <span data-ttu-id="fd973-123">La valeur de ce champ ou du champ **ParentName** identifie une instance parent spécifique.</span><span class="sxs-lookup"><span data-stu-id="fd973-123">The value in either this field or the **ParentName** field identifies a specific parent instance.</span></span> <span data-ttu-id="fd973-124">Si la valeur de ce champ est **null**, la valeur du champ **ParentName** doit être vérifiée pour identifier le parent.</span><span class="sxs-lookup"><span data-stu-id="fd973-124">If the value in this field is **NULL**, the value in the **ParentName** field must be checked to identify the parent.</span></span>

 

 
