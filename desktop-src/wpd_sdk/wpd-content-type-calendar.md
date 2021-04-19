---
description: '\_calendrier du \_ type de contenu wpd \_'
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202b21c0ac690c4a0b9621b876f6926c4c0efe5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534688"
---
# <a name="wpd_content_type_calendar"></a><span data-ttu-id="44df2-103">\_calendrier du \_ type de contenu wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-103">WPD\_CONTENT\_TYPE\_CALENDAR</span></span>

<span data-ttu-id="44df2-104">Un objet qui décrit son type comme \_ \_ un calendrier de type de contenu wpd \_ représente un calendrier.</span><span class="sxs-lookup"><span data-stu-id="44df2-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CALENDAR represents a calendar.</span></span> <span data-ttu-id="44df2-105">L’objet peut être un fichier qui contient des informations de calendrier ou un dossier qui contient d’autres objets liés au calendrier, tels que des tâches, des rendez-vous, etc.</span><span class="sxs-lookup"><span data-stu-id="44df2-105">The object can be a file that contains calendar information or a folder that contains other calendar-related objects, such as tasks, appointments, and so on.</span></span>

<span data-ttu-id="44df2-106">Ce type d’objet prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="44df2-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="44df2-107">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="44df2-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="44df2-108">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="44df2-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="44df2-109">\_ID d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="44df2-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="44df2-110">Required.</span></span>                                                             |
| [<span data-ttu-id="44df2-111">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="44df2-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="44df2-112">Required.</span></span>                                                             |
| [<span data-ttu-id="44df2-113">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="44df2-114">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="44df2-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="44df2-115">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="44df2-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="44df2-116">Required.</span></span>                                                             |
| [<span data-ttu-id="44df2-117">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="44df2-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="44df2-118">Required.</span></span>                                                             |
| [<span data-ttu-id="44df2-119">TYPE de contenu de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="44df2-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="44df2-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="44df2-120">Required.</span></span>                                                             |
| [<span data-ttu-id="44df2-121">WPD, \_ objet \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="44df2-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="44df2-122">Obligatoire si l’objet est masqué.</span><span class="sxs-lookup"><span data-stu-id="44df2-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="44df2-123">WPD, \_ objet \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="44df2-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="44df2-124">Obligatoire si l’objet est un objet système (représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="44df2-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="44df2-125">taille de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="44df2-126">Obligatoire si l’objet a au moins une ressource.</span><span class="sxs-lookup"><span data-stu-id="44df2-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="44df2-127">\_nom du \_ fichier d’origine de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="44df2-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="44df2-128">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="44df2-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="44df2-129">\_objet wpd \_ non \_ utilisable</span><span class="sxs-lookup"><span data-stu-id="44df2-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="44df2-130">Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="44df2-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="44df2-131">\_références d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="44df2-132">Obligatoire si l’objet a des références à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="44df2-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="44df2-133">\_Mots clés d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="44df2-134">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="44df2-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="44df2-135">ID de synchronisation de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="44df2-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="44df2-136">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="44df2-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="44df2-137">l' \_ objet \_ wpd \_ est \_ protégé par DRM</span><span class="sxs-lookup"><span data-stu-id="44df2-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="44df2-138">Obligatoire si l’objet est protégé par la technologie DRM.</span><span class="sxs-lookup"><span data-stu-id="44df2-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="44df2-139">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="44df2-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="44df2-140">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="44df2-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="44df2-141">Date de modification de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="44df2-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="44df2-142">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="44df2-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="44df2-143">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="44df2-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="44df2-144">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="44df2-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="44df2-145">\_ \_ références arrière des objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="44df2-146">Recommandé si l’objet est référencé par un autre objet.</span><span class="sxs-lookup"><span data-stu-id="44df2-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="44df2-147">\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="44df2-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="44df2-148">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="44df2-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="44df2-149">\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource</span><span class="sxs-lookup"><span data-stu-id="44df2-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="44df2-150">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="44df2-150">Optional.</span></span>                                                             |
| [<span data-ttu-id="44df2-151">l' \_ objet wpd \_ peut \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="44df2-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="44df2-152">Obligatoire si l’objet peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="44df2-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="44df2-153">\_paramètres régionaux de la langue de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="44df2-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="44df2-154">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="44df2-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="44df2-155">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="44df2-155">Typical Resources</span></span>

<span data-ttu-id="44df2-156">Ces objets incluent généralement les ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="44df2-156">These objects typically include the following resources.</span></span>



| <span data-ttu-id="44df2-157">Nom de la ressource</span><span class="sxs-lookup"><span data-stu-id="44df2-157">Resource Name</span></span>                                          | <span data-ttu-id="44df2-158">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="44df2-158">Required or Optional</span></span>                             | <span data-ttu-id="44df2-159">Description</span><span class="sxs-lookup"><span data-stu-id="44df2-159">Description</span></span>        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [<span data-ttu-id="44df2-160">**\_ressource wpd \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="44df2-160">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="44df2-161">Obligatoire si l’objet est associé à des données binaires.</span><span class="sxs-lookup"><span data-stu-id="44df2-161">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="44df2-162">Contient les données.</span><span class="sxs-lookup"><span data-stu-id="44df2-162">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="44df2-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44df2-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44df2-164">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="44df2-164">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



