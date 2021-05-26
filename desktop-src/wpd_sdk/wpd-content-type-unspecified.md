---
description: '\_type de contenu wpd \_ \_ non spécifié'
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd955ee5ebf31b2348efd3f70c85ae9c004edb83
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423679"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="b57ff-103">\_type de contenu wpd \_ \_ non spécifié</span><span class="sxs-lookup"><span data-stu-id="b57ff-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="b57ff-104">Un objet qui décrit son type de \_ contenu wpd \_ \_ non spécifié représente un objet générique qui peut ou non avoir un fichier physique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b57ff-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="b57ff-105">La différence entre ce type et le \_ fichier générique de type de contenu wpd \_ \_ \_ est que les \_ objets de fichier générique du type de contenu wpd \_ \_ \_ doivent avoir un fichier physique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="b57ff-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="b57ff-106">Ce type d’objet prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b57ff-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="b57ff-107">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="b57ff-107">Property Name</span></span>       | <span data-ttu-id="b57ff-108">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="b57ff-108">Required or Optional</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="b57ff-109">\_ID d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="b57ff-110">Obligatoire, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b57ff-110">Required, read-only.</span></span> <span data-ttu-id="b57ff-111">Un client ne peut pas définir cette propriété même au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="b57ff-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="b57ff-112">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="b57ff-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b57ff-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="b57ff-114">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="b57ff-115">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="b57ff-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="b57ff-116">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="b57ff-117">Obligatoire, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b57ff-117">Required, read-only.</span></span> <span data-ttu-id="b57ff-118">Un client ne peut pas définir cette propriété même au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="b57ff-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="b57ff-119">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="b57ff-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b57ff-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="b57ff-121">TYPE de contenu de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="b57ff-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b57ff-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="b57ff-123">WPD, \_ objet \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="b57ff-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="b57ff-124">Obligatoire si l’objet est masqué.</span><span class="sxs-lookup"><span data-stu-id="b57ff-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="b57ff-125">WPD, \_ objet \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="b57ff-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="b57ff-126">Obligatoire si l’objet est un objet système (représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="b57ff-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="b57ff-127">taille de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="b57ff-128">Obligatoire si l’objet a au moins une ressource.</span><span class="sxs-lookup"><span data-stu-id="b57ff-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="b57ff-129">\_nom du \_ fichier d’origine de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="b57ff-130">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="b57ff-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="b57ff-131">\_objet wpd \_ non \_ utilisable</span><span class="sxs-lookup"><span data-stu-id="b57ff-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="b57ff-132">Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b57ff-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="b57ff-133">\_références d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="b57ff-134">Obligatoire si l’objet a des références à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="b57ff-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="b57ff-135">\_Mots clés d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="b57ff-136">facultatif.</span><span class="sxs-lookup"><span data-stu-id="b57ff-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="b57ff-137">ID de synchronisation de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="b57ff-138">facultatif.</span><span class="sxs-lookup"><span data-stu-id="b57ff-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="b57ff-139">l' \_ objet \_ wpd \_ est \_ protégé par DRM</span><span class="sxs-lookup"><span data-stu-id="b57ff-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="b57ff-140">Obligatoire si l’objet est protégé par la technologie DRM.</span><span class="sxs-lookup"><span data-stu-id="b57ff-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="b57ff-141">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="b57ff-142">facultatif.</span><span class="sxs-lookup"><span data-stu-id="b57ff-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="b57ff-143">Date de modification de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="b57ff-144">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="b57ff-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="b57ff-145">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="b57ff-146">facultatif.</span><span class="sxs-lookup"><span data-stu-id="b57ff-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="b57ff-147">\_ \_ références arrière des objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="b57ff-148">Recommandé si l’objet est référencé par un autre objet.</span><span class="sxs-lookup"><span data-stu-id="b57ff-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="b57ff-149">\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="b57ff-150">facultatif.</span><span class="sxs-lookup"><span data-stu-id="b57ff-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="b57ff-151">\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource</span><span class="sxs-lookup"><span data-stu-id="b57ff-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="b57ff-152">facultatif.</span><span class="sxs-lookup"><span data-stu-id="b57ff-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="b57ff-153">l' \_ objet wpd \_ peut \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="b57ff-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="b57ff-154">Obligatoire si l’objet ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="b57ff-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="b57ff-155">\_paramètres régionaux de la langue de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="b57ff-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="b57ff-156">facultatif.</span><span class="sxs-lookup"><span data-stu-id="b57ff-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="b57ff-157">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="b57ff-157">Typical Resources</span></span>

<span data-ttu-id="b57ff-158">Ces objets incluent généralement les ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="b57ff-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="b57ff-159">Nom de la ressource</span><span class="sxs-lookup"><span data-stu-id="b57ff-159">Resource Name</span></span>                                          | <span data-ttu-id="b57ff-160">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="b57ff-160">Required or Optional</span></span>                             | <span data-ttu-id="b57ff-161">Description</span><span class="sxs-lookup"><span data-stu-id="b57ff-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="b57ff-162">**\_ressource wpd \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="b57ff-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="b57ff-163">Obligatoire si l’objet est associé à des données binaires.</span><span class="sxs-lookup"><span data-stu-id="b57ff-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="b57ff-164">Contient les données binaires.</span><span class="sxs-lookup"><span data-stu-id="b57ff-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b57ff-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b57ff-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b57ff-166">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="b57ff-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



