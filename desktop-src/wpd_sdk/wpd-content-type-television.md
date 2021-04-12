---
description: Objet qui décrit son type de télévision de \_ type de contenu wpd \_ \_ représente un enregistrement de télévision.
ms.assetid: b8e8da1a-94a9-4540-a4eb-fe0c0cd383f9
title: WPD_CONTENT_TYPE_TELEVISION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5141be847c0701f8828af0de8df41b8be21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319929"
---
# <a name="wpd_content_type_television"></a><span data-ttu-id="7e854-103">\_télévision du \_ type de contenu wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-103">WPD\_CONTENT\_TYPE\_TELEVISION</span></span>

<span data-ttu-id="7e854-104">Objet qui décrit son type de télévision de \_ type de contenu wpd \_ \_ représente un enregistrement de télévision.</span><span class="sxs-lookup"><span data-stu-id="7e854-104">An object that describes its type as WPD\_CONTENT\_TYPE\_TELEVISION represents a television recording.</span></span>

<span data-ttu-id="7e854-105">Ce type d’objet doit héberger les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e854-105">This type of object should host the following properties.</span></span>



| <span data-ttu-id="7e854-106">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="7e854-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="7e854-107">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="7e854-107">Required or Optional</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="7e854-108">\_ID d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="7e854-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7e854-109">Required.</span></span>                                                                    |
| [<span data-ttu-id="7e854-110">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="7e854-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7e854-111">Required.</span></span>                                                                    |
| [<span data-ttu-id="7e854-112">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="7e854-113">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="7e854-113">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="7e854-114">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="7e854-115">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7e854-115">Required.</span></span>                                                                    |
| [<span data-ttu-id="7e854-116">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="7e854-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7e854-117">Required.</span></span>                                                                    |
| [<span data-ttu-id="7e854-118">TYPE de contenu de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="7e854-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="7e854-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7e854-119">Required.</span></span>                                                                    |
| [<span data-ttu-id="7e854-120">WPD, \_ objet \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="7e854-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="7e854-121">Obligatoire si l’objet est masqué.</span><span class="sxs-lookup"><span data-stu-id="7e854-121">Required if the object is hidden.</span></span>                                            |
| [<span data-ttu-id="7e854-122">WPD, \_ objet \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="7e854-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="7e854-123">Obligatoire si l’objet est un objet système (représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="7e854-123">Required if the object is a system object (represents a system file).</span></span>        |
| [<span data-ttu-id="7e854-124">taille de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="7e854-125">Obligatoire si l’objet a au moins une ressource.</span><span class="sxs-lookup"><span data-stu-id="7e854-125">Required if the object has at least one resource.</span></span>                            |
| [<span data-ttu-id="7e854-126">\_nom du \_ fichier d’origine de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="7e854-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="7e854-127">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="7e854-127">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="7e854-128">\_objet wpd \_ non \_ utilisable</span><span class="sxs-lookup"><span data-stu-id="7e854-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="7e854-129">Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7e854-129">Recommended if the object is not meant for consumption by the device.</span></span>        |
| [<span data-ttu-id="7e854-130">\_références d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="7e854-131">Obligatoire si l’objet a des références à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="7e854-131">Required if the object has references to other objects.</span></span>                      |
| [<span data-ttu-id="7e854-132">\_Mots clés d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="7e854-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7e854-133">Optional.</span></span>                                                                    |
| [<span data-ttu-id="7e854-134">ID de synchronisation de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="7e854-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="7e854-135">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7e854-135">Optional.</span></span>                                                                    |
| [<span data-ttu-id="7e854-136">l' \_ objet \_ wpd \_ est \_ protégé par DRM</span><span class="sxs-lookup"><span data-stu-id="7e854-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="7e854-137">Obligatoire si l’objet est protégé par la technologie de Rights Management numérique.</span><span class="sxs-lookup"><span data-stu-id="7e854-137">Required if the object is protected by Digital Rights Management technology.</span></span> |
| [<span data-ttu-id="7e854-138">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="7e854-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="7e854-139">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7e854-139">Optional.</span></span>                                                                    |
| [<span data-ttu-id="7e854-140">Date de modification de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="7e854-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="7e854-141">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="7e854-141">Recommended.</span></span>                                                                 |
| [<span data-ttu-id="7e854-142">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="7e854-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="7e854-143">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7e854-143">Optional.</span></span>                                                                    |
| [<span data-ttu-id="7e854-144">\_ \_ références arrière des objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="7e854-145">Recommandé si l’objet est référencé par un autre objet.</span><span class="sxs-lookup"><span data-stu-id="7e854-145">Recommended if the object is referenced by another object.</span></span>                   |
| [<span data-ttu-id="7e854-146">\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="7e854-147">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7e854-147">Optional.</span></span>                                                                    |
| [<span data-ttu-id="7e854-148">\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="7e854-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="7e854-149">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7e854-149">Optional.</span></span>                                                                    |
| [<span data-ttu-id="7e854-150">\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource</span><span class="sxs-lookup"><span data-stu-id="7e854-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="7e854-151">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="7e854-151">Optional.</span></span>                                                                    |
| [<span data-ttu-id="7e854-152">l' \_ objet wpd \_ peut \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="7e854-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="7e854-153">Obligatoire si l’objet ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="7e854-153">Required if the object cannot be deleted.</span></span>                                    |



 

## <a name="typical-resources"></a><span data-ttu-id="7e854-154">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="7e854-154">Typical Resources</span></span>

<span data-ttu-id="7e854-155">Aucun</span><span class="sxs-lookup"><span data-stu-id="7e854-155">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="7e854-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e854-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e854-157">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="7e854-157">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



