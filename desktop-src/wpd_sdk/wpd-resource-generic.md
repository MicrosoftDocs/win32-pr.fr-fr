---
description: Spécifie un type de ressource qui n’est pas défini autrement par les appareils mobiles Windows.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112831"
---
# <a name="wpd_resource_generic"></a><span data-ttu-id="06299-103">\_ressource wpd \_ générique</span><span class="sxs-lookup"><span data-stu-id="06299-103">WPD\_RESOURCE\_GENERIC</span></span>

<span data-ttu-id="06299-104">Spécifie un type de ressource qui n’est pas défini autrement par les appareils mobiles Windows.</span><span class="sxs-lookup"><span data-stu-id="06299-104">Specifies a resource type not otherwise defined by Windows Portable Devices.</span></span> <span data-ttu-id="06299-105">Vous pouvez définir vos propres ressources personnalisées qui prennent en charge tous les attributs définis par des appareils mobiles ou Windows.</span><span class="sxs-lookup"><span data-stu-id="06299-105">You can define your own custom resources that support any custom or Windows Portable Devices-defined attributes.</span></span> <span data-ttu-id="06299-106">Toutefois, toutes les ressources que vous créez doivent prendre en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="06299-106">However, any resource you create must support the following attributes.</span></span>



| <span data-ttu-id="06299-107">Nom de l'attribut</span><span class="sxs-lookup"><span data-stu-id="06299-107">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="06299-108">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="06299-108">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="06299-109">\_ \_ \_ taille totale de l’attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="06299-109">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="06299-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="06299-110">Required.</span></span>                                              |
| [<span data-ttu-id="06299-111">l' \_ attribut de ressource wpd \_ \_ peut \_ lire</span><span class="sxs-lookup"><span data-stu-id="06299-111">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="06299-112">Obligatoire si les clients peuvent lire cette ressource.</span><span class="sxs-lookup"><span data-stu-id="06299-112">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="06299-113">l' \_ attribut de ressource wpd \_ \_ peut \_ écrire</span><span class="sxs-lookup"><span data-stu-id="06299-113">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="06299-114">Obligatoire si les clients peuvent écrire dans cette ressource.</span><span class="sxs-lookup"><span data-stu-id="06299-114">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="06299-115">l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="06299-115">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="06299-116">Obligatoire si les clients peuvent supprimer cette ressource.</span><span class="sxs-lookup"><span data-stu-id="06299-116">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="06299-117">\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="06299-117">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="06299-118">Obligatoire si les clients ont un accès en lecture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="06299-118">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="06299-119">\_taille de \_ la \_ \_ \_ mémoire tampon d’écriture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="06299-119">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="06299-120">Obligatoire si les clients ont un accès en écriture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="06299-120">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="06299-121">\_format d' \_ attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="06299-121">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="06299-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="06299-122">Required.</span></span>                                              |
| [<span data-ttu-id="06299-123">\_clé de \_ ressource d’attribut de ressource wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="06299-123">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="06299-124">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="06299-124">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="06299-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06299-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06299-126">**Conditions requises pour les ressources**</span><span class="sxs-lookup"><span data-stu-id="06299-126">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



