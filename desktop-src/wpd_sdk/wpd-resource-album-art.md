---
description: Spécifie une image qui représente l’illustration de l’album pour l’objet.
ms.assetid: 7a31ebb6-c4ab-4899-9c2e-c960aac4f0f9
title: WPD_RESOURCE_ALBUM_ART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4b800aa2ae22f2400f3195b85da6bd3bd35b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525905"
---
# <a name="wpd_resource_album_art"></a><span data-ttu-id="5fbff-103">image de l' \_ album des ressources wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="5fbff-103">WPD\_RESOURCE\_ALBUM\_ART</span></span>

<span data-ttu-id="5fbff-104">Spécifie une image qui représente l’illustration de l’album pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="5fbff-104">Specifies an image that represents the album artwork for the object.</span></span>

<span data-ttu-id="5fbff-105">Ce type de ressource doit prendre en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="5fbff-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="5fbff-106">Nom de l'attribut</span><span class="sxs-lookup"><span data-stu-id="5fbff-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="5fbff-107">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="5fbff-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="5fbff-108">\_largeur du média wpd \_</span><span class="sxs-lookup"><span data-stu-id="5fbff-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="5fbff-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5fbff-109">Required.</span></span>                                              |
| [<span data-ttu-id="5fbff-110">\_hauteur du média wpd \_</span><span class="sxs-lookup"><span data-stu-id="5fbff-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="5fbff-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5fbff-111">Required.</span></span>                                              |
| [<span data-ttu-id="5fbff-112">\_ \_ \_ taille totale de l’attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="5fbff-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="5fbff-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5fbff-113">Required.</span></span>                                              |
| [<span data-ttu-id="5fbff-114">l' \_ attribut de ressource wpd \_ \_ peut \_ lire</span><span class="sxs-lookup"><span data-stu-id="5fbff-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="5fbff-115">Obligatoire si les clients peuvent lire cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5fbff-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="5fbff-116">l' \_ attribut de ressource wpd \_ \_ peut \_ écrire</span><span class="sxs-lookup"><span data-stu-id="5fbff-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="5fbff-117">Obligatoire si les clients peuvent écrire dans cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5fbff-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="5fbff-118">l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="5fbff-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="5fbff-119">Obligatoire si les clients peuvent supprimer cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5fbff-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="5fbff-120">\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="5fbff-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="5fbff-121">Obligatoire si les clients ont un accès en lecture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="5fbff-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="5fbff-122">\_taille de \_ la \_ \_ \_ mémoire tampon d’écriture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="5fbff-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="5fbff-123">Obligatoire si les clients ont un accès en écriture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="5fbff-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="5fbff-124">\_format d' \_ attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="5fbff-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="5fbff-125">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5fbff-125">Required.</span></span>                                              |
| [<span data-ttu-id="5fbff-126">\_clé de \_ ressource d’attribut de ressource wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="5fbff-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="5fbff-127">Recommandé</span><span class="sxs-lookup"><span data-stu-id="5fbff-127">Recommended</span></span>                                            |



 

## <a name="see-also"></a><span data-ttu-id="5fbff-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fbff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fbff-129">**Conditions requises pour les ressources**</span><span class="sxs-lookup"><span data-stu-id="5fbff-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



