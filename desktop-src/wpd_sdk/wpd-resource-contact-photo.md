---
description: Spécifie une image qui représente une photo de la personne à laquelle il est question dans l’objet contact.
ms.assetid: e26487d8-cd21-4d4a-ba68-ae915eff1304
title: WPD_RESOURCE_CONTACT_PHOTO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ee8a283492eba61989eca3f3bfa96bdba2f0ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517482"
---
# <a name="wpd_resource_contact_photo"></a><span data-ttu-id="54bdb-103">PHOTO du contact de la \_ ressource wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="54bdb-103">WPD\_RESOURCE\_CONTACT\_PHOTO</span></span>

<span data-ttu-id="54bdb-104">Spécifie une image qui représente une photo de la personne à laquelle il est question dans l’objet contact.</span><span class="sxs-lookup"><span data-stu-id="54bdb-104">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>

<span data-ttu-id="54bdb-105">Ce type de ressource doit prendre en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="54bdb-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="54bdb-106">Nom de l'attribut</span><span class="sxs-lookup"><span data-stu-id="54bdb-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="54bdb-107">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="54bdb-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="54bdb-108">\_largeur du média wpd \_</span><span class="sxs-lookup"><span data-stu-id="54bdb-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="54bdb-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="54bdb-109">Required.</span></span>                                              |
| [<span data-ttu-id="54bdb-110">\_hauteur du média wpd \_</span><span class="sxs-lookup"><span data-stu-id="54bdb-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="54bdb-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="54bdb-111">Required.</span></span>                                              |
| [<span data-ttu-id="54bdb-112">\_ \_ \_ taille totale de l’attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="54bdb-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="54bdb-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="54bdb-113">Required.</span></span>                                              |
| [<span data-ttu-id="54bdb-114">l' \_ attribut de ressource wpd \_ \_ peut \_ lire</span><span class="sxs-lookup"><span data-stu-id="54bdb-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="54bdb-115">Obligatoire si les clients peuvent lire cette ressource.</span><span class="sxs-lookup"><span data-stu-id="54bdb-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="54bdb-116">l' \_ attribut de ressource wpd \_ \_ peut \_ écrire</span><span class="sxs-lookup"><span data-stu-id="54bdb-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="54bdb-117">Obligatoire si les clients peuvent écrire dans cette ressource.</span><span class="sxs-lookup"><span data-stu-id="54bdb-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="54bdb-118">l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="54bdb-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="54bdb-119">Obligatoire si les clients peuvent supprimer cette ressource.</span><span class="sxs-lookup"><span data-stu-id="54bdb-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="54bdb-120">\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="54bdb-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="54bdb-121">Obligatoire si les clients ont un accès en lecture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="54bdb-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="54bdb-122">\_taille de \_ la \_ \_ \_ mémoire tampon d’écriture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="54bdb-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="54bdb-123">Obligatoire si les clients ont un accès en écriture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="54bdb-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="54bdb-124">\_format d' \_ attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="54bdb-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="54bdb-125">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="54bdb-125">Required.</span></span>                                              |
| [<span data-ttu-id="54bdb-126">\_clé de \_ ressource d’attribut de ressource wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="54bdb-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="54bdb-127">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="54bdb-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="54bdb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54bdb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54bdb-129">**Conditions requises pour les ressources**</span><span class="sxs-lookup"><span data-stu-id="54bdb-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



