---
title: Modification d’attributs avec ADSI
description: Pour modifier des valeurs d’attribut, ADSI fournit les méthodes IADs. put et IADs. biais. Ces méthodes modifient les données dans le cache côté client. La méthode IADs. SetInfo doit être appelée pour valider les modifications apportées au répertoire.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modification d’attributs avec ADSI
- Attributs ADSI, modification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4f3b24b151d9991e1346cd18d396892f828f4dc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382856"
---
# <a name="modifying-attributes-with-adsi"></a><span data-ttu-id="cc53d-107">Modification d’attributs avec ADSI</span><span class="sxs-lookup"><span data-stu-id="cc53d-107">Modifying Attributes with ADSI</span></span>

<span data-ttu-id="cc53d-108">Pour modifier des valeurs d’attribut, ADSI fournit les méthodes [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) et [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-putex) biais.</span><span class="sxs-lookup"><span data-stu-id="cc53d-108">To modify attribute values, ADSI provides the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) and [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) methods.</span></span> <span data-ttu-id="cc53d-109">Ces méthodes modifient les données dans le cache côté client.</span><span class="sxs-lookup"><span data-stu-id="cc53d-109">These methods modify the data on the client-side cache.</span></span> <span data-ttu-id="cc53d-110">La méthode [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) doit être appelée pour valider les modifications apportées au répertoire.</span><span class="sxs-lookup"><span data-stu-id="cc53d-110">The [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method must be called to commit the changes to the directory.</span></span>

> [!Note]  
> <span data-ttu-id="cc53d-111">Lorsque plusieurs modifications d’attribut sont validées dans un seul appel à [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), si un attribut unique ne peut pas être modifié, aucun des attributs ne sera modifié.</span><span class="sxs-lookup"><span data-stu-id="cc53d-111">When multiple attribute changes are committed in a single call to [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), if any single attribute cannot be modified, none of the attributes will be modified.</span></span> <span data-ttu-id="cc53d-112">Par exemple, si vous modifiez les attributs [**sn**](/windows/desktop/ADSchema/a-sn) et [**GivenName**](/windows/desktop/ADSchema/a-givenname) et que vous effacez l’attribut [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) d’un objet User sans les appels suivants à la méthode **setinfo** , les modifications sont entrées lorsque vous appelez **setinfo**.</span><span class="sxs-lookup"><span data-stu-id="cc53d-112">For example, if you modify the [**sn**](/windows/desktop/ADSchema/a-sn) and [**givenName**](/windows/desktop/ADSchema/a-givenname) attributes and clear the [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) attribute of a user object without any subsequent calls to the **SetInfo** method, the changes are entered when you call **SetInfo**.</span></span> <span data-ttu-id="cc53d-113">Si une ou plusieurs modifications ne sont pas autorisées et ne peuvent donc pas être effectuées, aucune des modifications collectives apportées aux attributs n’est entrée lors de l’appel à **setinfo**.</span><span class="sxs-lookup"><span data-stu-id="cc53d-113">If one or more of the modifications are not allowed and therefore cannot be performed, then none of the collective modifications made to the attributes are entered during the call to **SetInfo**.</span></span>

 

<span data-ttu-id="cc53d-114">La méthode [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) prend un nom d’attribut et un paramètre Variant.</span><span class="sxs-lookup"><span data-stu-id="cc53d-114">The [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method takes an attribute name and a variant parameter.</span></span> <span data-ttu-id="cc53d-115">Utilisez cette méthode pour définir des attributs qui contiennent à la fois des valeurs uniques et multiples.</span><span class="sxs-lookup"><span data-stu-id="cc53d-115">Use this method to set attributes that contain both single and multiple values.</span></span>

<span data-ttu-id="cc53d-116">La méthode [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-putex) 2D fournit un contrôle sur les opérations sur les attributs à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="cc53d-116">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method provides control over operations on multi-valued attributes.</span></span> <span data-ttu-id="cc53d-117">Vous pouvez ajouter, supprimer, mettre à jour et effacer les valeurs existantes.</span><span class="sxs-lookup"><span data-stu-id="cc53d-117">You can append, delete, update, and clear existing values.</span></span> <span data-ttu-id="cc53d-118">La méthode **IADs .Ed** attend toujours un tableau variant de valeurs d’attribut.</span><span class="sxs-lookup"><span data-stu-id="cc53d-118">The **IADs.PutEx** method always expects a variant array of attribute values.</span></span> <span data-ttu-id="cc53d-119">Toutefois, vous pouvez utiliser cette méthode pour définir un attribut avec une seule valeur.</span><span class="sxs-lookup"><span data-stu-id="cc53d-119">However, you can use this method to set an attribute with a single value as well.</span></span>

<span data-ttu-id="cc53d-120">La méthode [**IADs.**](/windows/desktop/api/Iads/nf-iads-iads-putex) ciblage utilise les opérations spécifiées par l’énumération enum de l' [**opération de \_ propriété \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .</span><span class="sxs-lookup"><span data-stu-id="cc53d-120">The [**IADs.PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method uses the operations specified by the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

 

 