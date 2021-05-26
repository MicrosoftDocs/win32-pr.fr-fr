---
description: '\_programme de \_ type de contenu wpd \_'
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ddf3c5d406c16891c692e84fb37c4d21757f702
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423769"
---
# <a name="wpd_content_type_program"></a><span data-ttu-id="f0fa7-103">\_programme de \_ type de contenu wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-103">WPD\_CONTENT\_TYPE\_PROGRAM</span></span>

<span data-ttu-id="f0fa7-104">Un objet qui décrit son type comme \_ un programme de type de contenu wpd \_ \_ représente un programme exécutable.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-104">An object that describes its type as WPD\_CONTENT\_TYPE\_PROGRAM represents an executable program.</span></span>

<span data-ttu-id="f0fa7-105">Ce type d’objet prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="f0fa7-106">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="f0fa7-106">Property Name</span></span>     | <span data-ttu-id="f0fa7-107">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="f0fa7-107">Required or Optional</span></span>      |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0fa7-108">\_ID d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="f0fa7-109">Obligatoire, mais en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-109">Required, but read-only.</span></span> <span data-ttu-id="f0fa7-110">Un client ne peut pas définir cette propriété, même au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="f0fa7-111">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="f0fa7-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-112">Required.</span></span>                                                                          |
| [<span data-ttu-id="f0fa7-113">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="f0fa7-114">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-114">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="f0fa7-115">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="f0fa7-116">Obligatoire, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-116">Required, read-only.</span></span> <span data-ttu-id="f0fa7-117">Un client ne peut pas définir cette propriété même au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-117">A client cannot set this property even at creation time.</span></span>      |
| [<span data-ttu-id="f0fa7-118">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="f0fa7-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-119">Required.</span></span>                                                                          |
| [<span data-ttu-id="f0fa7-120">TYPE de contenu de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="f0fa7-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-121">Required.</span></span>                                                                          |
| [<span data-ttu-id="f0fa7-122">WPD, \_ objet \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="f0fa7-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="f0fa7-123">Obligatoire si l’objet est masqué.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-123">Required if the object is hidden.</span></span>                                                  |
| [<span data-ttu-id="f0fa7-124">WPD, \_ objet \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="f0fa7-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="f0fa7-125">Obligatoire si l’objet est un objet système (représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="f0fa7-125">Required if the object is a system object (represents a system file).</span></span>              |
| [<span data-ttu-id="f0fa7-126">taille de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="f0fa7-127">Obligatoire si l’objet a au moins une ressource.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-127">Required if the object has at least one resource.</span></span>                                  |
| [<span data-ttu-id="f0fa7-128">\_nom du \_ fichier d’origine de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="f0fa7-129">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-129">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="f0fa7-130">\_objet wpd \_ non \_ utilisable</span><span class="sxs-lookup"><span data-stu-id="f0fa7-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="f0fa7-131">Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-131">Recommended if the object is not meant for consumption by the device.</span></span>              |
| [<span data-ttu-id="f0fa7-132">\_références d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="f0fa7-133">Obligatoire si l’objet a des références à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-133">Required if the object has references to other objects.</span></span>                            |
| [<span data-ttu-id="f0fa7-134">\_Mots clés d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="f0fa7-135">facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-135">Optional.</span></span>                                                                          |
| [<span data-ttu-id="f0fa7-136">ID de synchronisation de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="f0fa7-137">facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-137">Optional.</span></span>                                                                          |
| [<span data-ttu-id="f0fa7-138">l' \_ objet \_ wpd \_ est \_ protégé par DRM</span><span class="sxs-lookup"><span data-stu-id="f0fa7-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="f0fa7-139">Obligatoire si l’objet est protégé par la technologie DRM.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-139">Required if the object is protected by DRM technology.</span></span>                             |
| [<span data-ttu-id="f0fa7-140">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="f0fa7-141">facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-141">Optional.</span></span>                                                                          |
| [<span data-ttu-id="f0fa7-142">Date de modification de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="f0fa7-143">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-143">Recommended.</span></span>                                                                       |
| [<span data-ttu-id="f0fa7-144">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="f0fa7-145">facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-145">Optional.</span></span>                                                                          |
| [<span data-ttu-id="f0fa7-146">\_ \_ références arrière des objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="f0fa7-147">Recommandé si l’objet est référencé par un autre objet.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-147">Recommended if the object is referenced by another object.</span></span>                         |
| [<span data-ttu-id="f0fa7-148">\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="f0fa7-149">facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-149">Optional.</span></span>                                                                          |
| [<span data-ttu-id="f0fa7-150">\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource</span><span class="sxs-lookup"><span data-stu-id="f0fa7-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="f0fa7-151">facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-151">Optional.</span></span>                                                                          |
| [<span data-ttu-id="f0fa7-152">l' \_ objet wpd \_ peut \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="f0fa7-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="f0fa7-153">Obligatoire si l’objet ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-153">Required if the object cannot be deleted.</span></span>                                          |
| [<span data-ttu-id="f0fa7-154">\_paramètres régionaux de la langue de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="f0fa7-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="f0fa7-155">facultatif.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-155">Optional.</span></span>                                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="f0fa7-156">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="f0fa7-156">Typical Resources</span></span>

<span data-ttu-id="f0fa7-157">Ces objets incluent généralement les ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="f0fa7-158">Nom de la ressource</span><span class="sxs-lookup"><span data-stu-id="f0fa7-158">Resource Name</span></span>                                          | <span data-ttu-id="f0fa7-159">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="f0fa7-159">Required or Optional</span></span> | <span data-ttu-id="f0fa7-160">Description</span><span class="sxs-lookup"><span data-stu-id="f0fa7-160">Description</span></span>                |
|--------------------------------------------------------|----------------------|----------------------------|
| [<span data-ttu-id="f0fa7-161">**\_ressource wpd \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="f0fa7-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="f0fa7-162">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-162">Required.</span></span>            | <span data-ttu-id="f0fa7-163">Contient le fichier programme.</span><span class="sxs-lookup"><span data-stu-id="f0fa7-163">Contains the program file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f0fa7-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f0fa7-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0fa7-165">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="f0fa7-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



