---
description: Les objets sécurisables utilisent un format de masque d’accès dans lequel les quatre bits de poids fort spécifient des droits d’accès génériques.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Droits d’accès génériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758248"
---
# <a name="generic-access-rights"></a><span data-ttu-id="da550-103">Droits d’accès génériques</span><span class="sxs-lookup"><span data-stu-id="da550-103">Generic Access Rights</span></span>

<span data-ttu-id="da550-104">Les objets sécurisables utilisent un [format de masque d’accès](access-mask-format.md) dans lequel les quatre bits de poids fort spécifient des droits d’accès génériques.</span><span class="sxs-lookup"><span data-stu-id="da550-104">Securable objects use an [access mask format](access-mask-format.md) in which the four high-order bits specify generic access rights.</span></span> <span data-ttu-id="da550-105">Chaque type d’objet sécurisable mappe ces bits à un ensemble de ses droits d’accès standard et spécifiques aux objets.</span><span class="sxs-lookup"><span data-stu-id="da550-105">Each type of securable object maps these bits to a set of its standard and object-specific access rights.</span></span> <span data-ttu-id="da550-106">Par exemple, un objet fichier Windows mappe le \_ bit de lecture générique au contrôle de lecture \_ et synchronise les droits d’accès standard et les droits d’accès de lecture de fichier \_ , de lecture de \_ fichier \_ \_ EA et de lecture de fichier \_ \_ spécifiques.</span><span class="sxs-lookup"><span data-stu-id="da550-106">For example, a Windows file object maps the GENERIC\_READ bit to the READ\_CONTROL and SYNCHRONIZE standard access rights and to the FILE\_READ\_DATA, FILE\_READ\_EA, and FILE\_READ\_ATTRIBUTES object-specific access rights.</span></span> <span data-ttu-id="da550-107">D’autres types d’objets mappent le \_ bit de lecture générique à n’importe quel jeu de droits d’accès adapté à ce type d’objet.</span><span class="sxs-lookup"><span data-stu-id="da550-107">Other types of objects map the GENERIC\_READ bit to whatever set of access rights is appropriate for that type of object.</span></span>

<span data-ttu-id="da550-108">Vous pouvez utiliser des droits d’accès génériques pour spécifier le type d’accès dont vous avez besoin lorsque vous ouvrez un handle vers un objet.</span><span class="sxs-lookup"><span data-stu-id="da550-108">You can use generic access rights to specify the type of access you need when you are opening a handle to an object.</span></span> <span data-ttu-id="da550-109">C’est généralement plus simple que de spécifier tous les droits standard et spécifiques correspondants.</span><span class="sxs-lookup"><span data-stu-id="da550-109">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span>

<span data-ttu-id="da550-110">Le tableau suivant montre les constantes définies pour les droits d’accès génériques.</span><span class="sxs-lookup"><span data-stu-id="da550-110">The following table shows the constants defined for the generic access rights.</span></span>



| <span data-ttu-id="da550-111">Constante</span><span class="sxs-lookup"><span data-stu-id="da550-111">Constant</span></span>         | <span data-ttu-id="da550-112">Signification générique</span><span class="sxs-lookup"><span data-stu-id="da550-112">Generic meaning</span></span>            |
|------------------|----------------------------|
| <span data-ttu-id="da550-113">GÉNÉRIQUE \_ tout</span><span class="sxs-lookup"><span data-stu-id="da550-113">GENERIC\_ALL</span></span>     | <span data-ttu-id="da550-114">Tous les droits d’accès possibles</span><span class="sxs-lookup"><span data-stu-id="da550-114">All possible access rights</span></span> |
| <span data-ttu-id="da550-115">\_Exécution générique</span><span class="sxs-lookup"><span data-stu-id="da550-115">GENERIC\_EXECUTE</span></span> | <span data-ttu-id="da550-116">Exécuter l’accès</span><span class="sxs-lookup"><span data-stu-id="da550-116">Execute access</span></span>             |
| <span data-ttu-id="da550-117">\_lecture générique</span><span class="sxs-lookup"><span data-stu-id="da550-117">GENERIC\_READ</span></span>    | <span data-ttu-id="da550-118">Accès en lecture</span><span class="sxs-lookup"><span data-stu-id="da550-118">Read access</span></span>                |
| <span data-ttu-id="da550-119">\_écriture générique</span><span class="sxs-lookup"><span data-stu-id="da550-119">GENERIC\_WRITE</span></span>   | <span data-ttu-id="da550-120">Accès en écriture</span><span class="sxs-lookup"><span data-stu-id="da550-120">Write access</span></span>               |



 

<span data-ttu-id="da550-121">Les applications qui définissent des objets sécurisables privés peuvent également utiliser les droits d’accès génériques.</span><span class="sxs-lookup"><span data-stu-id="da550-121">Applications that define private securable objects can also use the generic access rights.</span></span>

 

 



