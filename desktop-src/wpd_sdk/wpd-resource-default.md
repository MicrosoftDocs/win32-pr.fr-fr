---
description: Spécifie l’ensemble du fichier situé derrière l’objet. Il permet également de faire référence à n’importe quel type de ressource, y compris ceux non couverts par d’autres types de ressources de périphériques mobiles Windows, tels qu’un type d’objet personnalisé.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529890"
---
# <a name="wpd_resource_default"></a><span data-ttu-id="2eb57-104">\_ressource wpd \_ par défaut</span><span class="sxs-lookup"><span data-stu-id="2eb57-104">WPD\_RESOURCE\_DEFAULT</span></span>

<span data-ttu-id="2eb57-105">Spécifie l’ensemble du fichier situé derrière l’objet.</span><span class="sxs-lookup"><span data-stu-id="2eb57-105">Specifies the whole file behind the object.</span></span> <span data-ttu-id="2eb57-106">Il permet également de faire référence à n’importe quel type de ressource, y compris ceux non couverts par d’autres types de ressources de périphériques mobiles Windows, tels qu’un type d’objet personnalisé.</span><span class="sxs-lookup"><span data-stu-id="2eb57-106">It is also a way of referring to any resource type, including those not covered by other Windows Portable Devices resource types, such as a custom object type.</span></span>

<span data-ttu-id="2eb57-107">Toutes les ressources incorporées dans la ressource spécifiée seront incluses.</span><span class="sxs-lookup"><span data-stu-id="2eb57-107">Any resources embedded within the specified resource will be included.</span></span> <span data-ttu-id="2eb57-108">Par exemple, la ressource par défaut d’un dossier racine des contacts peut inclure tous les contacts imbriqués.</span><span class="sxs-lookup"><span data-stu-id="2eb57-108">For example, the default resource of a root folder of contacts may include all the nested contacts.</span></span> <span data-ttu-id="2eb57-109">Toutefois, les ressources enfants qui sont simplement *liées* par des métadonnées ou des références ne sont pas incluses.</span><span class="sxs-lookup"><span data-stu-id="2eb57-109">However, any child resources that are merely *linked* by metadata or references are not included.</span></span> <span data-ttu-id="2eb57-110">Il peut s’agir, par exemple, d’une sélection, qui peut uniquement être liée à des fichiers audio par le biais de références de métadonnées ou de chemins textuels dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="2eb57-110">An example of this would be a playlist, which might only link to audio files through metadata references or textual path references in the file.</span></span>

<span data-ttu-id="2eb57-111">La seule valeur *PID* autorisée pour cette **PROPERTYKEY** est zéro.</span><span class="sxs-lookup"><span data-stu-id="2eb57-111">The only allowed *pid* value for this **PROPERTYKEY** is zero.</span></span>

<span data-ttu-id="2eb57-112">Ce type de ressource doit prendre en charge les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="2eb57-112">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="2eb57-113">Nom de l'attribut</span><span class="sxs-lookup"><span data-stu-id="2eb57-113">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="2eb57-114">Obligatoire ou facultatif</span><span class="sxs-lookup"><span data-stu-id="2eb57-114">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="2eb57-115">\_ \_ \_ taille totale de l’attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="2eb57-115">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="2eb57-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2eb57-116">Required.</span></span>                                              |
| [<span data-ttu-id="2eb57-117">l' \_ attribut de ressource wpd \_ \_ peut \_ lire</span><span class="sxs-lookup"><span data-stu-id="2eb57-117">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="2eb57-118">Obligatoire si les clients peuvent lire cette ressource.</span><span class="sxs-lookup"><span data-stu-id="2eb57-118">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="2eb57-119">l' \_ attribut de ressource wpd \_ \_ peut \_ écrire</span><span class="sxs-lookup"><span data-stu-id="2eb57-119">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="2eb57-120">Obligatoire si les clients peuvent écrire dans cette ressource.</span><span class="sxs-lookup"><span data-stu-id="2eb57-120">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="2eb57-121">l' \_ attribut de ressource wpd \_ \_ peut être \_ supprimé</span><span class="sxs-lookup"><span data-stu-id="2eb57-121">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="2eb57-122">Obligatoire si les clients peuvent supprimer cette ressource.</span><span class="sxs-lookup"><span data-stu-id="2eb57-122">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="2eb57-123">\_taille de \_ la \_ \_ \_ mémoire tampon de lecture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="2eb57-123">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="2eb57-124">Obligatoire si les clients ont un accès en lecture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="2eb57-124">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="2eb57-125">\_taille de \_ la \_ \_ \_ mémoire tampon d’écriture optimale \_ des attributs de ressource wpd</span><span class="sxs-lookup"><span data-stu-id="2eb57-125">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="2eb57-126">Obligatoire si les clients ont un accès en écriture à la ressource.</span><span class="sxs-lookup"><span data-stu-id="2eb57-126">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="2eb57-127">\_format d' \_ attribut de ressource wpd \_</span><span class="sxs-lookup"><span data-stu-id="2eb57-127">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="2eb57-128">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2eb57-128">Required.</span></span>                                              |
| [<span data-ttu-id="2eb57-129">\_clé de \_ ressource d’attribut de ressource wpd \_ \_</span><span class="sxs-lookup"><span data-stu-id="2eb57-129">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="2eb57-130">Recommandé.</span><span class="sxs-lookup"><span data-stu-id="2eb57-130">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="2eb57-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2eb57-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb57-132">**Conditions requises pour les ressources**</span><span class="sxs-lookup"><span data-stu-id="2eb57-132">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



