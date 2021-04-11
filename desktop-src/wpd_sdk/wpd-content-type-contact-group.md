---
description: '\_groupe de \_ contacts du type de contenu wpd \_ \_'
ms.assetid: ddebb789-7e60-4728-a0a4-94c06d8a98f9
title: WPD_CONTENT_TYPE_CONTACT_GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b9db8d82807f854ee6cf04e4654228631eb1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209744"
---
# <a name="wpd_content_type_contact_group"></a><span data-ttu-id="4d560-103">\_groupe de \_ contacts du type de contenu wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="4d560-103">WPD\_CONTENT\_TYPE\_CONTACT\_GROUP</span></span>

<span data-ttu-id="4d560-104">Objet qui décrit son type, le \_ \_ \_ groupe de contacts de type de contenu wpd \_ représente un groupe de contacts.</span><span class="sxs-lookup"><span data-stu-id="4d560-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CONTACT\_GROUP represents a group of contacts.</span></span> <span data-ttu-id="4d560-105">Les références de l’objet WPD de cet objet \_ \_ contiennent une liste d’ID d’objet pour différents \_ objets de contact de type de contenu wpd \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4d560-105">This object's WPD\_OBJECT\_REFERENCES contains a list of object IDs for various WPD\_CONTENT\_TYPE\_CONTACT objects.</span></span>

<span data-ttu-id="4d560-106">Ce type d’objet prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d560-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="4d560-107">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="4d560-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="4d560-108">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="4d560-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="4d560-109">\_ID d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="4d560-110">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4d560-110">Required.</span></span>                                                             |
| [<span data-ttu-id="4d560-111">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="4d560-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4d560-112">Required.</span></span>                                                             |
| [<span data-ttu-id="4d560-113">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="4d560-114">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="4d560-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="4d560-115">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="4d560-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4d560-116">Required.</span></span>                                                             |
| [<span data-ttu-id="4d560-117">\_format d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="4d560-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4d560-118">Required.</span></span>                                                             |
| [<span data-ttu-id="4d560-119">TYPE de contenu de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="4d560-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="4d560-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="4d560-120">Required.</span></span>                                                             |
| [<span data-ttu-id="4d560-121">WPD, \_ objet \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="4d560-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="4d560-122">Obligatoire si l’objet est masqué.</span><span class="sxs-lookup"><span data-stu-id="4d560-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="4d560-123">WPD, \_ objet \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="4d560-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="4d560-124">Obligatoire si l’objet est un objet système (représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="4d560-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="4d560-125">taille de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="4d560-126">Obligatoire si l’objet a au moins une ressource.</span><span class="sxs-lookup"><span data-stu-id="4d560-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="4d560-127">\_nom du \_ fichier d’origine de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="4d560-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="4d560-128">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="4d560-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="4d560-129">\_objet wpd \_ non \_ utilisable</span><span class="sxs-lookup"><span data-stu-id="4d560-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="4d560-130">Recommandé si l’objet n’est pas destiné à être consommé par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4d560-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="4d560-131">\_références d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="4d560-132">Obligatoire si l’objet a des références à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="4d560-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="4d560-133">\_Mots clés d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="4d560-134">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4d560-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="4d560-135">ID de synchronisation de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="4d560-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="4d560-136">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4d560-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="4d560-137">l' \_ objet \_ wpd \_ est \_ protégé par DRM</span><span class="sxs-lookup"><span data-stu-id="4d560-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="4d560-138">Obligatoire si l’objet est protégé par la technologie DRM.</span><span class="sxs-lookup"><span data-stu-id="4d560-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="4d560-139">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="4d560-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="4d560-140">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4d560-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="4d560-141">Date de modification de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="4d560-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="4d560-142">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="4d560-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="4d560-143">Date de création de l' \_ objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="4d560-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="4d560-144">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4d560-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="4d560-145">\_ \_ références arrière des objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="4d560-146">Recommandé si l’objet est référencé par un autre objet.</span><span class="sxs-lookup"><span data-stu-id="4d560-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="4d560-147">\_ID d' \_ \_ objet fonctionnel \_ du conteneur d’objets wpd \_</span><span class="sxs-lookup"><span data-stu-id="4d560-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="4d560-148">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4d560-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="4d560-149">\_objet wpd \_ générer une \_ miniature \_ à partir de la \_ ressource</span><span class="sxs-lookup"><span data-stu-id="4d560-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="4d560-150">Facultatif</span><span class="sxs-lookup"><span data-stu-id="4d560-150">Optional</span></span>                                                              |
| [<span data-ttu-id="4d560-151">l' \_ objet wpd \_ peut \_ Supprimer</span><span class="sxs-lookup"><span data-stu-id="4d560-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="4d560-152">Obligatoire si l’objet peut être supprimé.</span><span class="sxs-lookup"><span data-stu-id="4d560-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="4d560-153">\_paramètres régionaux de la langue de l’objet wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="4d560-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="4d560-154">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="4d560-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="4d560-155">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="4d560-155">Typical Resources</span></span>

<span data-ttu-id="4d560-156">Aucun</span><span class="sxs-lookup"><span data-stu-id="4d560-156">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d560-157">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d560-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d560-158">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="4d560-158">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



