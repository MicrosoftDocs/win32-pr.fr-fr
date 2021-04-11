---
description: Conditions requises pour les ressources
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Conditions requises pour les ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204027"
---
# <a name="requirements-for-resources"></a><span data-ttu-id="5c94d-103">Conditions requises pour les ressources</span><span class="sxs-lookup"><span data-stu-id="5c94d-103">Requirements for Resources</span></span>

<span data-ttu-id="5c94d-104">Les appareils mobiles Windows définissent les catégories de ressources suivantes comme des valeurs **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="5c94d-104">Windows Portable Devices defines the following resource categories as **PROPERTYKEY** values.</span></span> <span data-ttu-id="5c94d-105">Ces valeurs sont utilisées pour décrire des ressources individuelles dans un objet.</span><span class="sxs-lookup"><span data-stu-id="5c94d-105">These values are used to describe individual resources in an object.</span></span> <span data-ttu-id="5c94d-106">Le membre *PID* de la clé de propriété peut être différent pour décrire des ressources différentes du même type pour tous les types, à l’exception de la **\_ ressource wpd \_ par défaut**, qui ne peut décrire qu’une seule ressource.</span><span class="sxs-lookup"><span data-stu-id="5c94d-106">The *pid* member of the property key can be different to describe different resources of the same type for all types except **WPD\_RESOURCE\_DEFAULT**, which can only describe one resource.</span></span> <span data-ttu-id="5c94d-107">La page Description liée pour chaque type de ressource répertorie les attributs pris en charge par cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5c94d-107">The linked description page for each resource type lists the attributes supported by that resource.</span></span>



| <span data-ttu-id="5c94d-108">Ressource PROPERTYKEY</span><span class="sxs-lookup"><span data-stu-id="5c94d-108">Resource PROPERTYKEY</span></span>                                                | <span data-ttu-id="5c94d-109">Description</span><span class="sxs-lookup"><span data-stu-id="5c94d-109">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c94d-110">**\_ressource wpd \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="5c94d-110">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md)              | <span data-ttu-id="5c94d-111">Spécifie l’ensemble du fichier situé derrière l’objet.</span><span class="sxs-lookup"><span data-stu-id="5c94d-111">Specifies the whole file behind the object.</span></span> <span data-ttu-id="5c94d-112">Il s’agit de la seule ressource requise pour un objet avec une ressource.</span><span class="sxs-lookup"><span data-stu-id="5c94d-112">This is the only required resource for any object with a resource.</span></span> |
| [<span data-ttu-id="5c94d-113">**image de l' \_ album des ressources wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c94d-113">**WPD\_RESOURCE\_ALBUM\_ART**</span></span>](wpd-resource-album-art.md)         | <span data-ttu-id="5c94d-114">Spécifie une image qui représente l’illustration de l’album pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="5c94d-114">Specifies an image that represents the album artwork for the object.</span></span>                                           |
| [<span data-ttu-id="5c94d-115">**\_ \_ clip audio de la ressource wpd \_**</span><span class="sxs-lookup"><span data-stu-id="5c94d-115">**WPD\_RESOURCE\_AUDIO\_CLIP**</span></span>](wpd-resource-audio-clip.md)       | <span data-ttu-id="5c94d-116">Spécifie un clip audio pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="5c94d-116">Specifies an audio clip for the object.</span></span>                                                                        |
| [<span data-ttu-id="5c94d-117">**PHOTO du contact de la \_ ressource wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5c94d-117">**WPD\_RESOURCE\_CONTACT\_PHOTO**</span></span>](wpd-resource-contact-photo.md) | <span data-ttu-id="5c94d-118">Spécifie une image qui représente une photo de la personne à laquelle il est question dans l’objet contact.</span><span class="sxs-lookup"><span data-stu-id="5c94d-118">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>                |
| [<span data-ttu-id="5c94d-119">**\_ressource wpd \_ générique**</span><span class="sxs-lookup"><span data-stu-id="5c94d-119">**WPD\_RESOURCE\_GENERIC**</span></span>](wpd-resource-generic.md)              | <span data-ttu-id="5c94d-120">Ressource générique de type de données non défini.</span><span class="sxs-lookup"><span data-stu-id="5c94d-120">A generic resource of undefined data type.</span></span> <span data-ttu-id="5c94d-121">Ce doit être traité comme un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="5c94d-121">This should be treated as a byte array.</span></span>                             |
| [<span data-ttu-id="5c94d-122">**\_icône de ressource wpd \_**</span><span class="sxs-lookup"><span data-stu-id="5c94d-122">**WPD\_RESOURCE\_ICON**</span></span>](wpd-resource-icon.md)                    | <span data-ttu-id="5c94d-123">icône ;</span><span class="sxs-lookup"><span data-stu-id="5c94d-123">An icon.</span></span>                                                                                                       |
| [<span data-ttu-id="5c94d-124">**\_miniature des ressources wpd \_**</span><span class="sxs-lookup"><span data-stu-id="5c94d-124">**WPD\_RESOURCE\_THUMBNAIL**</span></span>](wpd-resource-thumbnail.md)          | <span data-ttu-id="5c94d-125">Une image miniature.</span><span class="sxs-lookup"><span data-stu-id="5c94d-125">A thumbnail image.</span></span>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="5c94d-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c94d-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c94d-127">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="5c94d-127">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



