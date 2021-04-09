---
description: Enregistrement ou rejet des modifications
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Enregistrement ou rejet des modifications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860849"
---
# <a name="saving-or-discarding-changes"></a><span data-ttu-id="84d02-103">Enregistrement ou rejet des modifications</span><span class="sxs-lookup"><span data-stu-id="84d02-103">Saving or Discarding Changes</span></span>

<span data-ttu-id="84d02-104">Lorsque vous définissez des propriétés sur un élément, aucune modification n’est réellement enregistrée dans le catalogue COM+ tant que vous n’avez pas enregistré explicitement les modifications.</span><span class="sxs-lookup"><span data-stu-id="84d02-104">When you set properties on an item, no changes are actually recorded to the COM+ catalog until you explicitly save changes.</span></span> <span data-ttu-id="84d02-105">Pour ce faire, utilisez la méthode [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) pour la collection contenant l’élément.</span><span class="sxs-lookup"><span data-stu-id="84d02-105">You do this using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object for the collection containing the item.</span></span>

<span data-ttu-id="84d02-106">Si vous souhaitez ignorer les modifications qui n’ont pas encore été validées, vous pouvez appeler la méthode [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) sur l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="84d02-106">If you want to discard changes that have not yet been committed, you can call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="84d02-107">Cela lit toutes les données persistantes du catalogue COM+ pour tous les éléments de la collection, en supprimant efficacement les modifications en attente.</span><span class="sxs-lookup"><span data-stu-id="84d02-107">This reads in all persistent data from the COM+ catalog for all items in the collection, effectively deleting any pending changes.</span></span>

<span data-ttu-id="84d02-108">Lorsque vous utilisez [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), les incohérences dans les paramètres de propriété que vous avez choisi entraînent une erreur et **SaveChanges** ne parvient pas à écrire l’objet qui a retourné l’erreur.</span><span class="sxs-lookup"><span data-stu-id="84d02-108">When you use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), any inconsistencies in property settings that you have chosen result in an error, and **SaveChanges** fails to write the object that returned the error.</span></span> <span data-ttu-id="84d02-109">Toutes les propriétés d’un élément donné sont écrites ou ne peuvent pas être écrites dans leur ensemble.</span><span class="sxs-lookup"><span data-stu-id="84d02-109">All properties on a given item either are written or fail to be written as a whole.</span></span>

<span data-ttu-id="84d02-110">Toutefois, lorsque des erreurs d’écriture se produisent, elles peuvent ne pas être dues à des paramètres incompatibles. une autre défaillance s’est peut-être produite.</span><span class="sxs-lookup"><span data-stu-id="84d02-110">However, when write errors occur, they might not be due to incompatible settings; some other failure might have occurred.</span></span> <span data-ttu-id="84d02-111">Vous devez inspecter les détails de l’échec pour être certain.</span><span class="sxs-lookup"><span data-stu-id="84d02-111">You need to inspect the details of the failure to be certain.</span></span> <span data-ttu-id="84d02-112">Pour plus d’informations, consultez [gestion des erreurs d’administration com+](handling-com--administration-errors.md) et des [interdépendances entre les propriétés](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="84d02-112">For more information, see [Handling COM+ Administration Errors](handling-com--administration-errors.md) and [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="84d02-113">En règle générale, plus vous essayez d’enregistrer en une seule fois, en particulier les modifications apportées à plusieurs objets, plus il est probable que vous obteniez une erreur et plus il est difficile d’effectuer le suivi.</span><span class="sxs-lookup"><span data-stu-id="84d02-113">As a general rule, the more changes you attempt to save at once, particularly changes to multiple objects, the more likely you are to get an error and the more difficult it is to track down.</span></span>

<span data-ttu-id="84d02-114">En outre, entre les appels à [**remplir**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) et [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), vous n’avez pas de verrou sur les éléments de la collection ; les conflits sont possibles.</span><span class="sxs-lookup"><span data-stu-id="84d02-114">Additionally, between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), you do not have a lock on the items in the collection; contention is possible.</span></span> <span data-ttu-id="84d02-115">Pour plus d’informations, consultez [obtention et définition des propriétés](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="84d02-115">For more details, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84d02-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84d02-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84d02-117">Obtention et définition des propriétés</span><span class="sxs-lookup"><span data-stu-id="84d02-117">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="84d02-118">Interdépendances entre les propriétés</span><span class="sxs-lookup"><span data-stu-id="84d02-118">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="84d02-119">Interrogation des propriétés disponibles</span><span class="sxs-lookup"><span data-stu-id="84d02-119">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> </dl>

 

 



