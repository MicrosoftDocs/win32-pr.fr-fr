---
description: '\_certificat de \_ type de contenu wpd \_'
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde0ff631cd8eed28226d1e374d84e65d9756b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536807"
---
# <a name="wpd_content_type_certificate"></a><span data-ttu-id="d6329-103">\_certificat de \_ type de contenu wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-103">WPD\_CONTENT\_TYPE\_CERTIFICATE</span></span>

<span data-ttu-id="d6329-104">Objet qui décrit son type en tant que \_ certificat de type de contenu wpd \_ \_ représente un certificat utilisé pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="d6329-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CERTIFICATE represents a certificate used for authentication.</span></span>

<span data-ttu-id="d6329-105">Ce type d’objet prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d6329-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="d6329-106">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="d6329-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="d6329-107">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="d6329-107">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="d6329-108">\_ID d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="d6329-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d6329-109">Required.</span></span>                                                             |
| [<span data-ttu-id="d6329-110">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="d6329-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d6329-111">Required.</span></span>                                                             |
| [<span data-ttu-id="d6329-112">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="d6329-113">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="d6329-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="d6329-114">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="d6329-115">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d6329-115">Required.</span></span>                                                             |
| [<span data-ttu-id="d6329-116">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="d6329-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d6329-117">Required.</span></span>                                                             |
| [<span data-ttu-id="d6329-118">TYPE de contenu de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6329-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="d6329-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d6329-119">Required.</span></span>                                                             |
| [<span data-ttu-id="d6329-120">WPD, \_ objet \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="d6329-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="d6329-121">Obligatoire si l’objet est masqué.</span><span class="sxs-lookup"><span data-stu-id="d6329-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="d6329-122">WPD, \_ objet \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="d6329-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="d6329-123">Obligatoire si l’objet est un objet système (représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="d6329-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="d6329-124">taille de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="d6329-125">Obligatoire si l’objet a au moins une ressource.</span><span class="sxs-lookup"><span data-stu-id="d6329-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="d6329-126">\_nom du \_ fichier d’origine de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6329-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="d6329-127">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="d6329-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="d6329-128">\_objet wpd \_ non \_ utilisable</span><span class="sxs-lookup"><span data-stu-id="d6329-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="d6329-129">Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d6329-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="d6329-130">\_références d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="d6329-131">Obligatoire si l’objet a des références à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="d6329-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="d6329-132">\_Mots clés d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="d6329-133">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d6329-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="d6329-134">ID de synchronisation de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6329-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="d6329-135">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d6329-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="d6329-136">l' \_ objet \_ wpd \_ est \_ protégé par DRM</span><span class="sxs-lookup"><span data-stu-id="d6329-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="d6329-137">Obligatoire si l’objet est protégé par la technologie DRM.</span><span class="sxs-lookup"><span data-stu-id="d6329-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="d6329-138">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6329-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="d6329-139">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d6329-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="d6329-140">Date de modification de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6329-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="d6329-141">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="d6329-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="d6329-142">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6329-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="d6329-143">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d6329-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="d6329-144">\_ \_ références arrière des objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="d6329-145">Recommandé si l’objet est référencé par un autre objet.</span><span class="sxs-lookup"><span data-stu-id="d6329-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="d6329-146">\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="d6329-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="d6329-147">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d6329-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="d6329-148">\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource</span><span class="sxs-lookup"><span data-stu-id="d6329-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="d6329-149">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d6329-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="d6329-150">l' \_ objet wpd \_ peut \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="d6329-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="d6329-151">Obligatoire si l’objet peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="d6329-151">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="d6329-152">\_paramètres régionaux de la langue de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d6329-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="d6329-153">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d6329-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="d6329-154">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="d6329-154">Typical Resources</span></span>

<span data-ttu-id="d6329-155">Ces objets incluent généralement les ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="d6329-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="d6329-156">Nom de la ressource</span><span class="sxs-lookup"><span data-stu-id="d6329-156">Resource Name</span></span>                                          | <span data-ttu-id="d6329-157">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="d6329-157">Required or Optional</span></span> | <span data-ttu-id="d6329-158">Description</span><span class="sxs-lookup"><span data-stu-id="d6329-158">Description</span></span>        |
|--------------------------------------------------------|----------------------|--------------------|
| [<span data-ttu-id="d6329-159">**\_ressource wpd \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="d6329-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="d6329-160">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d6329-160">Required.</span></span>            | <span data-ttu-id="d6329-161">Contient les données.</span><span class="sxs-lookup"><span data-stu-id="d6329-161">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d6329-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6329-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6329-163">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="d6329-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



