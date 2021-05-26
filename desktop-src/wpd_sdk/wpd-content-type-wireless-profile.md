---
description: '\_profil de type de contenu wpd \_ \_ sans fil \_'
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 999c8aec77c6ff046690e4c3450c0643d685e1db
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423699"
---
# <a name="wpd_content_type_wireless_profile"></a><span data-ttu-id="d73ad-103">\_profil de type de contenu wpd \_ \_ sans fil \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-103">WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE</span></span>

<span data-ttu-id="d73ad-104">Objet qui décrit son type de contenu WPD \_ le \_ \_ profil sans fil \_ représente les informations utilisées pour accéder à un réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="d73ad-104">An object that describes its type as WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE represents information used to access a wireless network.</span></span>

<span data-ttu-id="d73ad-105">Ce type d’objet prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d73ad-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="d73ad-106">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="d73ad-106">Property Name</span></span>             | <span data-ttu-id="d73ad-107">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="d73ad-107">Required or Optional</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="d73ad-108">\_ID d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="d73ad-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d73ad-109">Required.</span></span>                                                             |
| [<span data-ttu-id="d73ad-110">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="d73ad-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d73ad-111">Required.</span></span>                                                             |
| [<span data-ttu-id="d73ad-112">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="d73ad-113">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="d73ad-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="d73ad-114">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="d73ad-115">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d73ad-115">Required.</span></span>                                                             |
| [<span data-ttu-id="d73ad-116">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="d73ad-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d73ad-117">Required.</span></span>                                                             |
| [<span data-ttu-id="d73ad-118">TYPE de contenu de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="d73ad-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d73ad-119">Required.</span></span>                                                             |
| [<span data-ttu-id="d73ad-120">WPD, \_ objet \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="d73ad-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="d73ad-121">Obligatoire si l’objet est masqué.</span><span class="sxs-lookup"><span data-stu-id="d73ad-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="d73ad-122">WPD, \_ objet \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="d73ad-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="d73ad-123">Obligatoire si l’objet est un objet système (représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="d73ad-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="d73ad-124">taille de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="d73ad-125">Obligatoire si l’objet a au moins une ressource.</span><span class="sxs-lookup"><span data-stu-id="d73ad-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="d73ad-126">\_nom du \_ fichier d’origine de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="d73ad-127">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="d73ad-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="d73ad-128">\_objet wpd \_ non \_ utilisable</span><span class="sxs-lookup"><span data-stu-id="d73ad-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="d73ad-129">Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d73ad-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="d73ad-130">\_références d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="d73ad-131">Obligatoire si l’objet a des références à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="d73ad-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="d73ad-132">\_Mots clés d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="d73ad-133">facultatif.</span><span class="sxs-lookup"><span data-stu-id="d73ad-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="d73ad-134">ID de synchronisation de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="d73ad-135">facultatif.</span><span class="sxs-lookup"><span data-stu-id="d73ad-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="d73ad-136">l' \_ objet \_ wpd \_ est \_ protégé par DRM</span><span class="sxs-lookup"><span data-stu-id="d73ad-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="d73ad-137">Obligatoire si l’objet est protégé par la technologie DRM.</span><span class="sxs-lookup"><span data-stu-id="d73ad-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="d73ad-138">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="d73ad-139">facultatif.</span><span class="sxs-lookup"><span data-stu-id="d73ad-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="d73ad-140">Date de modification de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="d73ad-141">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="d73ad-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="d73ad-142">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="d73ad-143">facultatif.</span><span class="sxs-lookup"><span data-stu-id="d73ad-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="d73ad-144">\_ \_ références arrière des objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="d73ad-145">Recommandé si l’objet est référencé par un autre objet.</span><span class="sxs-lookup"><span data-stu-id="d73ad-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="d73ad-146">\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="d73ad-147">facultatif.</span><span class="sxs-lookup"><span data-stu-id="d73ad-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="d73ad-148">\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource</span><span class="sxs-lookup"><span data-stu-id="d73ad-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="d73ad-149">facultatif.</span><span class="sxs-lookup"><span data-stu-id="d73ad-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="d73ad-150">l' \_ objet wpd \_ peut \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="d73ad-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="d73ad-151">Obligatoire si l’objet ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="d73ad-151">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="d73ad-152">\_paramètres régionaux de la langue de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="d73ad-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="d73ad-153">facultatif.</span><span class="sxs-lookup"><span data-stu-id="d73ad-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="d73ad-154">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="d73ad-154">Typical Resources</span></span>

<span data-ttu-id="d73ad-155">Ces objets incluent généralement les ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="d73ad-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="d73ad-156">Nom de la ressource</span><span class="sxs-lookup"><span data-stu-id="d73ad-156">Resource Name</span></span>                                          | <span data-ttu-id="d73ad-157">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="d73ad-157">Required or Optional</span></span>                                  | <span data-ttu-id="d73ad-158">Description</span><span class="sxs-lookup"><span data-stu-id="d73ad-158">Description</span></span>               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [<span data-ttu-id="d73ad-159">**\_ressource wpd \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="d73ad-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="d73ad-160">Obligatoire si l’objet est représenté par des données binaires.</span><span class="sxs-lookup"><span data-stu-id="d73ad-160">Required if the object is represented by binary data.</span></span> | <span data-ttu-id="d73ad-161">Contient les données binaires.</span><span class="sxs-lookup"><span data-stu-id="d73ad-161">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d73ad-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d73ad-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d73ad-163">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="d73ad-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



