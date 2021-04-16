---
title: Meilleures pratiques (plateforme de filtrage Windows)
description: La liste suivante contient les meilleures pratiques pour le développement d’applications à l’aide de l’API WFP (Windows Filtering Platform).
ms.assetid: 017ff210-8666-466e-8424-c95e750fd5ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac43f103e0076945d566e26a1706bdec22916db
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508249"
---
# <a name="best-practices-windows-filtering-platform"></a><span data-ttu-id="7508b-103">Meilleures pratiques (plateforme de filtrage Windows)</span><span class="sxs-lookup"><span data-stu-id="7508b-103">Best Practices (Windows Filtering Platform)</span></span>

<span data-ttu-id="7508b-104">La liste suivante contient les meilleures pratiques pour le développement d’applications à l’aide de l’API WFP (Windows Filtering Platform).</span><span class="sxs-lookup"><span data-stu-id="7508b-104">The following list contains best practices for developing applications using the Windows Filtering Platform (WFP) API.</span></span>

-   <span data-ttu-id="7508b-105">Utilisez des sessions dynamiques.</span><span class="sxs-lookup"><span data-stu-id="7508b-105">Use dynamic sessions.</span></span>

    <span data-ttu-id="7508b-106">De nombreuses applications ajoutent des objets de stratégie de filtrage au démarrage, puis suppriment ces objets à l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="7508b-106">Many applications add filtering policy objects at start, and then delete these objects at stop.</span></span> <span data-ttu-id="7508b-107">En utilisant une session dynamique, vous garantissez que ces objets sont supprimés même si l’application se bloque.</span><span class="sxs-lookup"><span data-stu-id="7508b-107">By using a dynamic session, you guarantee that these objects are deleted even if the application crashes.</span></span> <span data-ttu-id="7508b-108">En outre, il est plus efficace de simplement fermer le handle de moteur à l’arrêt que d’effectuer des appels individuels pour supprimer chaque objet.</span><span class="sxs-lookup"><span data-stu-id="7508b-108">Furthermore, simply closing the engine handle at stop is more efficient than making individual calls to delete each object.</span></span>

-   <span data-ttu-id="7508b-109">Gérez les délais d’attente des transactions de manière appropriée ou définissez la session **txnWaitTimeoutInMSec** sur Infinite afin d’éviter les délais d’attente.</span><span class="sxs-lookup"><span data-stu-id="7508b-109">Either handle transaction timeouts gracefully or set the session **txnWaitTimeoutInMSec** to infinite to prevent timeouts.</span></span>

    <span data-ttu-id="7508b-110">Même si vous n’utilisez pas de transactions explicites, la plupart des appels sont toujours exécutés dans le cadre d’une transaction implicite et peuvent donc avoir un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="7508b-110">Even if you do not use explicit transactions, most calls are still executed under an implicit transaction and thus can timeout.</span></span>

-   <span data-ttu-id="7508b-111">Utilisez des transactions explicites pour combiner des opérations d’ajout ou de suppression liées dans une transaction unique.</span><span class="sxs-lookup"><span data-stu-id="7508b-111">Use explicit transactions to combine related add or delete operations into a single transaction.</span></span>

    <span data-ttu-id="7508b-112">Cela est plus efficace et facilite le nettoyage des résultats partiels dans les chemins d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7508b-112">This is more efficient and makes it easy to clean up partial results in error paths.</span></span>

-   <span data-ttu-id="7508b-113">Utilisez des chaînes compatibles avec MUI.</span><span class="sxs-lookup"><span data-stu-id="7508b-113">Use MUI compliant strings.</span></span>

    <span data-ttu-id="7508b-114">Toutes les chaînes localisables sont stockées dans une structure de données commune : [**FWPM \_ Display \_ DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span><span class="sxs-lookup"><span data-stu-id="7508b-114">All the localizable strings are stored in a common data structure: [**FWPM\_DISPLAY\_DATA0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwpm_display_data0).</span></span> <span data-ttu-id="7508b-115">Les chaînes de cette structure peuvent être des chaînes indirectes du type pris en charge par [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span><span class="sxs-lookup"><span data-stu-id="7508b-115">The strings within this structure can be indirect strings of the type supported by [**SHLoadIndirectString**](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span> <span data-ttu-id="7508b-116">Avant qu’une structure **\_ \_ DATA0 d’affichage FWPM** ne soit retournée par l’une des fonctions, les chaînes indirectes sont résolues en la ressource de chaîne spécifiée à l’aide des paramètres régionaux de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="7508b-116">Before an **FWPM\_DISPLAY\_DATA0** structure is returned by any of the functions, the indirect strings are resolved to the specified string resource using the caller's locale.</span></span>

-   <span data-ttu-id="7508b-117">Associez tous les objets à un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="7508b-117">Associate all objects to a provider.</span></span>

    <span data-ttu-id="7508b-118">Lorsque plusieurs fournisseurs sont installés sur le système, il est plus facile pour les outils de diagnostic de déterminer qui a ajouté quoi.</span><span class="sxs-lookup"><span data-stu-id="7508b-118">When multiple providers are installed on the system, this makes it is easier for diagnostic tools to determine who added what.</span></span>

-   <span data-ttu-id="7508b-119">Ajoutez des filtres à votre propre sous-couche.</span><span class="sxs-lookup"><span data-stu-id="7508b-119">Add filters to your own sublayer.</span></span>

    <span data-ttu-id="7508b-120">Une fois qu’un filtre de fin dans une sous-couche est atteint, aucun autre filtre dans cette sous-couche n’est évalué.</span><span class="sxs-lookup"><span data-stu-id="7508b-120">Once a terminating filter in a sublayer is hit, no more filters in that sublayer are evaluated.</span></span> <span data-ttu-id="7508b-121">Ainsi, si vous ajoutez vos filtres à la même sous-couche qu’un autre fournisseur, vous risquez d’empêcher l’appel de ces filtres, ce qui aboutit à des résultats inattendus.</span><span class="sxs-lookup"><span data-stu-id="7508b-121">Thus, if you add your filters to the same sublayer as another provider, you may prevent each other's filters from being invoked, resulting in unexpected results.</span></span>

-   <span data-ttu-id="7508b-122">Utilisez la contrainte de mise en conformité de la couche application (ALE) plutôt que le filtrage orienté paquets.</span><span class="sxs-lookup"><span data-stu-id="7508b-122">Use Application Layer Enforcement (ALE) rather than packet-oriented filtering.</span></span>

    <span data-ttu-id="7508b-123">Le filtrage au niveau de la couche de paquets est lent.</span><span class="sxs-lookup"><span data-stu-id="7508b-123">Filtering at the packet layer is slow.</span></span>

-   <span data-ttu-id="7508b-124">Filtrez les erreurs ICMP et les événements RST avant qu’ils ne soient générés.</span><span class="sxs-lookup"><span data-stu-id="7508b-124">Filter ICMP errors and RST events before they are generated.</span></span>

    <span data-ttu-id="7508b-125">Il est plus efficace de filtrer ces événements une fois qu’ils sont générés.</span><span class="sxs-lookup"><span data-stu-id="7508b-125">This is more efficient that filtering these events after they are generated.</span></span>

-   <span data-ttu-id="7508b-126">Effectuer l’inspection des paquets au niveau de la couche de données de flux/datagramme plutôt qu’au niveau de la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="7508b-126">Perform packet inspection at Stream/Datagram Data layer rather than at the Transport layer.</span></span>

    <span data-ttu-id="7508b-127">Cela s’applique au développement de légendes.</span><span class="sxs-lookup"><span data-stu-id="7508b-127">This applies to developing callouts.</span></span> <span data-ttu-id="7508b-128">Pour plus d’informations, consultez Considérations sur la [programmation du pilote Callout](/windows-hardware/drivers/network/callout-driver-programming-considerations) dans le kit de pilotes Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="7508b-128">For more information, see [Callout Driver Programming Considerations](/windows-hardware/drivers/network/callout-driver-programming-considerations) in the Windows Driver Kit (WDK).</span></span>

-   <span data-ttu-id="7508b-129">Tenez compte des implications en termes de performances lors de l’utilisation de filtres complexes.</span><span class="sxs-lookup"><span data-stu-id="7508b-129">Consider performance implications when using complex filters.</span></span>

    <span data-ttu-id="7508b-130">À compter de Windows 7 et de Windows Server 2008 R2, les filtres peuvent être créés avec plusieurs conditions qui utilisent la même clé de champ.</span><span class="sxs-lookup"><span data-stu-id="7508b-130">Starting in Windows 7 and Windows Server 2008 R2, filters can be created with multiple conditions which use the same field key.</span></span> <span data-ttu-id="7508b-131">Cela permet de créer des stratégies complexes avec moins de filtres.</span><span class="sxs-lookup"><span data-stu-id="7508b-131">This allows complex policies to be created with fewer filters.</span></span> <span data-ttu-id="7508b-132">Toutefois, ces filtres complexes peuvent entraîner une baisse des performances du moteur de filtre WFP.</span><span class="sxs-lookup"><span data-stu-id="7508b-132">However such complex filters might incur a slower performance for the WFP filter engine to classify.</span></span> <span data-ttu-id="7508b-133">Une évaluation doit être effectuée pour déterminer si l’utilisation de ces filtres entraîne un effet néfaste sur les performances globales de votre solution.</span><span class="sxs-lookup"><span data-stu-id="7508b-133">An evaluation should be made to determine whether use of such filters causes an adverse effect on the overall performance of your solution.</span></span>

 

 
