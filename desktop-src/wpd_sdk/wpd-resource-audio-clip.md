---
description: Spécifie un clip audio pour l’objet.
ms.assetid: 24c15df0-4190-4c75-b89b-0c73d645c9ca
title: WPD_RESOURCE_AUDIO_CLIP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7013fb59670c92903f89509f720f7c597ef916fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520714"
---
# <a name="wpd_resource_audio_clip"></a><span data-ttu-id="0691b-103">\_ \_ clip audio de la ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="0691b-103">WPD\_RESOURCE\_AUDIO\_CLIP</span></span>

<span data-ttu-id="0691b-104">Spécifie un clip audio pour l’objet.</span><span class="sxs-lookup"><span data-stu-id="0691b-104">Specifies an audio clip for the object.</span></span>

<span data-ttu-id="0691b-105">Ce type de ressource doit prendre en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="0691b-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="0691b-106">Nom de l'attribut</span><span class="sxs-lookup"><span data-stu-id="0691b-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="0691b-107">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="0691b-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="0691b-108">\_ \_ débit binaire wpd</span><span class="sxs-lookup"><span data-stu-id="0691b-108">WPD\_AUDIO\_BITRATE</span></span>](audio-properties.md)                                                             | <span data-ttu-id="0691b-109">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="0691b-109">Recommended.</span></span>                                           |
| [<span data-ttu-id="0691b-110">\_nombre de \_ canaux \_ audio wpd</span><span class="sxs-lookup"><span data-stu-id="0691b-110">WPD\_AUDIO\_CHANNEL\_COUNT</span></span>](audio-properties.md)                                                | <span data-ttu-id="0691b-111">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0691b-111">Optional.</span></span>                                              |
| [<span data-ttu-id="0691b-112">\_Code de \_ format \_ audio wpd</span><span class="sxs-lookup"><span data-stu-id="0691b-112">WPD\_AUDIO\_FORMAT\_CODE</span></span>](audio-properties.md)                                                    | <span data-ttu-id="0691b-113">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0691b-113">Optional.</span></span>                                              |
| [<span data-ttu-id="0691b-114">\_profondeur de \_ bits \_ audio wpd</span><span class="sxs-lookup"><span data-stu-id="0691b-114">WPD\_AUDIO\_BIT\_DEPTH</span></span>](audio-properties.md)                                                        | <span data-ttu-id="0691b-115">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0691b-115">Optional.</span></span>                                              |
| [<span data-ttu-id="0691b-116">\_alignement des \_ blocs \_ audio wpd</span><span class="sxs-lookup"><span data-stu-id="0691b-116">WPD\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](audio-properties.md)                                            | <span data-ttu-id="0691b-117">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0691b-117">Optional.</span></span>                                              |
| [<span data-ttu-id="0691b-118">\_ \_ \_ taille totale de l’attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="0691b-118">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="0691b-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0691b-119">Required.</span></span>                                              |
| [<span data-ttu-id="0691b-120">l' \_ attribut de ressource wpd \_ \_ peut \_ lire</span><span class="sxs-lookup"><span data-stu-id="0691b-120">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="0691b-121">Obligatoire si les clients peuvent lire cette ressource.</span><span class="sxs-lookup"><span data-stu-id="0691b-121">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="0691b-122">l' \_ attribut de ressource wpd \_ \_ peut \_ écrire</span><span class="sxs-lookup"><span data-stu-id="0691b-122">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="0691b-123">Obligatoire si les clients peuvent écrire dans cette ressource.</span><span class="sxs-lookup"><span data-stu-id="0691b-123">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="0691b-124">l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="0691b-124">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="0691b-125">Obligatoire si les clients peuvent supprimer cette ressource.</span><span class="sxs-lookup"><span data-stu-id="0691b-125">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="0691b-126">\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="0691b-126">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="0691b-127">Obligatoire si les clients ont un accès en lecture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="0691b-127">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="0691b-128">\_taille de \_ la \_ \_ \_ mémoire tampon d’écriture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="0691b-128">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="0691b-129">Obligatoire si les clients ont un accès en écriture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="0691b-129">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="0691b-130">\_format d' \_ attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="0691b-130">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="0691b-131">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0691b-131">Required.</span></span>                                              |
| [<span data-ttu-id="0691b-132">\_clé de \_ ressource d’attribut de ressource wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="0691b-132">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="0691b-133">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="0691b-133">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="0691b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0691b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0691b-135">**Conditions requises pour les ressources**</span><span class="sxs-lookup"><span data-stu-id="0691b-135">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



