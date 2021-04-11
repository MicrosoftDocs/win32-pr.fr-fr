---
description: Spécifie une petite image&\# 8212 ; généralement une plus petite version d’une plus grande image dans l’objet.
ms.assetid: ad1eac9d-b182-49b2-bd2c-2d76e2026d80
title: WPD_RESOURCE_THUMBNAIL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc26af624f756f55ccb10ccf3f8c7bf3e6a6035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112830"
---
# <a name="wpd_resource_thumbnail"></a><span data-ttu-id="e13b4-103">\_miniature des ressources wpd \_</span><span class="sxs-lookup"><span data-stu-id="e13b4-103">WPD\_RESOURCE\_THUMBNAIL</span></span>

<span data-ttu-id="e13b4-104">Spécifie une petite image, en général une plus petite version d’une plus grande image dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="e13b4-104">Specifies a small picture—typically a smaller version of a larger picture in the object.</span></span>

<span data-ttu-id="e13b4-105">Ce type de ressource doit prendre en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="e13b4-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="e13b4-106">Nom de l'attribut</span><span class="sxs-lookup"><span data-stu-id="e13b4-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="e13b4-107">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="e13b4-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e13b4-108">\_largeur du média wpd \_</span><span class="sxs-lookup"><span data-stu-id="e13b4-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="e13b4-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e13b4-109">Required.</span></span>                                              |
| [<span data-ttu-id="e13b4-110">\_hauteur du média wpd \_</span><span class="sxs-lookup"><span data-stu-id="e13b4-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="e13b4-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e13b4-111">Required.</span></span>                                              |
| [<span data-ttu-id="e13b4-112">\_ \_ \_ taille totale de l’attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="e13b4-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="e13b4-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e13b4-113">Required.</span></span>                                              |
| [<span data-ttu-id="e13b4-114">l' \_ attribut de ressource wpd \_ \_ peut \_ lire</span><span class="sxs-lookup"><span data-stu-id="e13b4-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="e13b4-115">Obligatoire si les clients peuvent lire cette ressource.</span><span class="sxs-lookup"><span data-stu-id="e13b4-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="e13b4-116">l' \_ attribut de ressource wpd \_ \_ peut \_ écrire</span><span class="sxs-lookup"><span data-stu-id="e13b4-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="e13b4-117">Obligatoire si les clients peuvent écrire dans cette ressource.</span><span class="sxs-lookup"><span data-stu-id="e13b4-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="e13b4-118">l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="e13b4-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="e13b4-119">Obligatoire si les clients peuvent supprimer cette ressource.</span><span class="sxs-lookup"><span data-stu-id="e13b4-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="e13b4-120">\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="e13b4-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="e13b4-121">Obligatoire si les clients ont un accès en lecture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="e13b4-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="e13b4-122">\_taille de \_ la \_ \_ \_ mémoire tampon d’écriture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="e13b4-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="e13b4-123">Obligatoire si les clients ont un accès en écriture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="e13b4-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="e13b4-124">\_format d' \_ attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="e13b4-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="e13b4-125">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e13b4-125">Required.</span></span>                                              |
| [<span data-ttu-id="e13b4-126">\_clé de \_ ressource d’attribut de ressource wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="e13b4-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="e13b4-127">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="e13b4-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="e13b4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e13b4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13b4-129">**Conditions requises pour les ressources**</span><span class="sxs-lookup"><span data-stu-id="e13b4-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



