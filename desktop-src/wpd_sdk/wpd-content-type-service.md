---
description: '\_service de \_ type de contenu wpd \_'
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952651"
---
# <a name="wpd_content_type_service"></a><span data-ttu-id="b5dba-103">\_service de \_ type de contenu wpd \_</span><span class="sxs-lookup"><span data-stu-id="b5dba-103">WPD\_CONTENT\_TYPE\_SERVICE</span></span>

<span data-ttu-id="b5dba-104">Objet qui décrit son type en tant que \_ \_ service de type de contenu wpd \_ représente un service d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b5dba-104">An object that describes its type as WPD\_CONTENT\_TYPE\_SERVICE represents a device service.</span></span>

<span data-ttu-id="b5dba-105">Ce type d’objet prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b5dba-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="b5dba-106">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="b5dba-106">Property Name</span></span>                                                                                        | <span data-ttu-id="b5dba-107">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="b5dba-107">Required or Optional</span></span>                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="b5dba-108">\_ID d’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b5dba-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                               | <span data-ttu-id="b5dba-109">Obligatoire, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b5dba-109">Required, read-only.</span></span> <span data-ttu-id="b5dba-110">Un client ne peut pas définir cette propriété, même au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="b5dba-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="b5dba-111">\_ \_ ID parent de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b5dba-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                | <span data-ttu-id="b5dba-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b5dba-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="b5dba-113">nom de l' \_ objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b5dba-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                           | <span data-ttu-id="b5dba-114">Obligatoire si l’objet représente un fichier.</span><span class="sxs-lookup"><span data-stu-id="b5dba-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="b5dba-115">\_ \_ \_ ID unique persistant de l’objet wpd \_</span><span class="sxs-lookup"><span data-stu-id="b5dba-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)         | <span data-ttu-id="b5dba-116">Obligatoire, en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b5dba-116">Required, read-only.</span></span> <span data-ttu-id="b5dba-117">Un client ne peut pas définir cette propriété, même au moment de la création.</span><span class="sxs-lookup"><span data-stu-id="b5dba-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="b5dba-118">WPD, \_ objet \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="b5dba-118">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                   | <span data-ttu-id="b5dba-119">Obligatoire si le service ne doit pas être présenté à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b5dba-119">Required if the service should not be shown to the user.</span></span>                       |
| [<span data-ttu-id="b5dba-120">WPD, \_ objet \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="b5dba-120">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                   | <span data-ttu-id="b5dba-121">Obligatoire si l’objet est un objet système (représente un fichier système).</span><span class="sxs-lookup"><span data-stu-id="b5dba-121">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="b5dba-122">\_catégorie d' \_ objet \_ fonctionnel wpd</span><span class="sxs-lookup"><span data-stu-id="b5dba-122">WPD\_FUNCTIONAL\_OBJECT\_CATEGORY</span></span>](object-properties.md) | <span data-ttu-id="b5dba-123">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b5dba-123">Required.</span></span> <span data-ttu-id="b5dba-124">Cela représente le type de service de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b5dba-124">This represents the device service type.</span></span>                             |
| [<span data-ttu-id="b5dba-125">\_version du service wpd \_</span><span class="sxs-lookup"><span data-stu-id="b5dba-125">WPD\_SERVICE\_VERSION</span></span>](object-properties.md)           | <span data-ttu-id="b5dba-126">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="b5dba-126">Required.</span></span>                                                                      |
| [<span data-ttu-id="b5dba-127">\_type de stockage wpd \_</span><span class="sxs-lookup"><span data-stu-id="b5dba-127">WPD\_STORAGE\_TYPE</span></span>](object-properties.md)                                                          | <span data-ttu-id="b5dba-128">Obligatoire si le service est utilisé pour stocker des objets.</span><span class="sxs-lookup"><span data-stu-id="b5dba-128">Required if the service is used to store objects.</span></span>                              |
| [<span data-ttu-id="b5dba-129">\_capacité de stockage wpd \_</span><span class="sxs-lookup"><span data-stu-id="b5dba-129">WPD\_STORAGE\_CAPACITY</span></span>](object-properties.md)                                                      | <span data-ttu-id="b5dba-130">Obligatoire si le service est utilisé pour stocker des objets.</span><span class="sxs-lookup"><span data-stu-id="b5dba-130">Required if the service is used to store objects.</span></span>                              |



 

## <a name="typical-resources"></a><span data-ttu-id="b5dba-131">Ressources standard</span><span class="sxs-lookup"><span data-stu-id="b5dba-131">Typical Resources</span></span>

<span data-ttu-id="b5dba-132">Ces objets n’hébergent pas de ressources.</span><span class="sxs-lookup"><span data-stu-id="b5dba-132">These objects do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5dba-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5dba-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5dba-134">**Conditions requises pour les objets**</span><span class="sxs-lookup"><span data-stu-id="b5dba-134">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



