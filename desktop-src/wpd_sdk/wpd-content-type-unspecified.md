---
description: '\_type de contenu wpd \_ \_ non spécifié'
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b767ba2d76dc569def42b80eb646ae0e6a6aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867513"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="3e84b-103">\_type de contenu wpd \_ \_ non spécifié</span><span class="sxs-lookup"><span data-stu-id="3e84b-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="3e84b-104">Un objet qui décrit son type de \_ contenu wpd \_ \_ non spécifié représente un objet générique qui peut ou non avoir un fichier physique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="3e84b-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="3e84b-105">La différence entre ce type et le \_ fichier générique de type de contenu wpd \_ \_ \_ est que les \_ objets de fichier générique du type de contenu wpd \_ \_ \_ doivent avoir un fichier physique sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="3e84b-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="3e84b-106">Ce type d’objet prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="3e84b-106">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="3e84b-107">**Nom de la propriété**</span><span class="sxs-lookup"><span data-stu-id="3e84b-107">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="3e84b-108">**Obligatoire ou facultatif**</span><span class="sxs-lookup"><span data-stu-id="3e84b-108">**Required or Optional**</span></span>                                                      |
| [<span data-ttu-id="3e84b-109">\_ID d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="3e84b-110">Obligatoire, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3e84b-110">Required, read-only.</span></span> <span data-ttu-id="3e84b-111">Un client ne peut pas définir cette propriété même au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="3e84b-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="3e84b-112">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="3e84b-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3e84b-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="3e84b-114">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="3e84b-115">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="3e84b-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="3e84b-116">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="3e84b-117">Obligatoire, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3e84b-117">Required, read-only.</span></span> <span data-ttu-id="3e84b-118">Un client ne peut pas définir cette propriété même au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="3e84b-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="3e84b-119">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="3e84b-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3e84b-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="3e84b-121">TYPE de contenu de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="3e84b-122">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3e84b-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="3e84b-123">WPD, \_ objet \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="3e84b-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="3e84b-124">Obligatoire si l’objet est masqué.</span><span class="sxs-lookup"><span data-stu-id="3e84b-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="3e84b-125">WPD, \_ objet \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="3e84b-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="3e84b-126">Obligatoire si l’objet est un objet système (représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="3e84b-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="3e84b-127">taille de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="3e84b-128">Obligatoire si l’objet a au moins une ressource.</span><span class="sxs-lookup"><span data-stu-id="3e84b-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="3e84b-129">\_nom du \_ fichier d’origine de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="3e84b-130">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="3e84b-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="3e84b-131">\_objet wpd \_ non \_ utilisable</span><span class="sxs-lookup"><span data-stu-id="3e84b-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="3e84b-132">Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3e84b-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="3e84b-133">\_références d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="3e84b-134">Obligatoire si l’objet a des références à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="3e84b-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="3e84b-135">\_Mots clés d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="3e84b-136">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3e84b-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="3e84b-137">ID de synchronisation de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="3e84b-138">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3e84b-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="3e84b-139">l' \_ objet \_ wpd \_ est \_ protégé par DRM</span><span class="sxs-lookup"><span data-stu-id="3e84b-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="3e84b-140">Obligatoire si l’objet est protégé par la technologie DRM.</span><span class="sxs-lookup"><span data-stu-id="3e84b-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="3e84b-141">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="3e84b-142">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3e84b-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="3e84b-143">Date de modification de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="3e84b-144">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="3e84b-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="3e84b-145">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="3e84b-146">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3e84b-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="3e84b-147">\_ \_ références arrière des objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="3e84b-148">Recommandé si l’objet est référencé par un autre objet.</span><span class="sxs-lookup"><span data-stu-id="3e84b-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="3e84b-149">\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="3e84b-150">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3e84b-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="3e84b-151">\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource</span><span class="sxs-lookup"><span data-stu-id="3e84b-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="3e84b-152">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3e84b-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="3e84b-153">l' \_ objet wpd \_ peut \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="3e84b-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="3e84b-154">Obligatoire si l’objet ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="3e84b-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="3e84b-155">\_paramètres régionaux de la langue de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e84b-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="3e84b-156">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3e84b-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="3e84b-157">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="3e84b-157">Typical Resources</span></span>

<span data-ttu-id="3e84b-158">Ces objets incluent généralement les ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="3e84b-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="3e84b-159">Nom de la ressource</span><span class="sxs-lookup"><span data-stu-id="3e84b-159">Resource Name</span></span>                                          | <span data-ttu-id="3e84b-160">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="3e84b-160">Required or Optional</span></span>                             | <span data-ttu-id="3e84b-161">Description</span><span class="sxs-lookup"><span data-stu-id="3e84b-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="3e84b-162">**\_ressource wpd \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="3e84b-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="3e84b-163">Obligatoire si l’objet est associé à des données binaires.</span><span class="sxs-lookup"><span data-stu-id="3e84b-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="3e84b-164">Contient les données binaires.</span><span class="sxs-lookup"><span data-stu-id="3e84b-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3e84b-165">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e84b-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e84b-166">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="3e84b-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



