---
description: Décrit deux types de limites de quota de disque et la mesure des limites de quota de disque.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Limites de quota de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517918"
---
# <a name="disk-quota-limits"></a><span data-ttu-id="9dfcf-103">Limites de quota de disque</span><span class="sxs-lookup"><span data-stu-id="9dfcf-103">Disk Quota Limits</span></span>

<span data-ttu-id="9dfcf-104">L’espace disque utilisé par chaque fichier est facturé directement à l’utilisateur propriétaire du fichier.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-104">The disk space that each file uses is charged directly to the user who owns the file.</span></span> <span data-ttu-id="9dfcf-105">Le propriétaire d’un fichier est identifié par l’identificateur de sécurité (SID) dans les informations de sécurité du fichier.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-105">The owner of a file is identified by the security identifier (SID) in the security information for the file.</span></span> <span data-ttu-id="9dfcf-106">L’espace disque total facturé pour un utilisateur est la somme de la longueur de tous les flux de données.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-106">The total disk space charged to a user is the sum of the length of all data streams.</span></span> <span data-ttu-id="9dfcf-107">En d’autres termes, les flux de jeu de propriétés et les flux de données utilisateur résidents affectent le quota de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-107">In other words, property set streams and resident user data streams affect the user's quota.</span></span>

<span data-ttu-id="9dfcf-108">Le quota n’est pas facturé pour les points de réanalyse, les descripteurs de sécurité ou d’autres métadonnées associées aux fichiers.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-108">Quota is not charged for re-parse points, security descriptors, or other metadata that is associated with the files.</span></span> <span data-ttu-id="9dfcf-109">La compression ou la décompression des fichiers n’affecte pas l’espace disque indiqué pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-109">Compressing or decompressing files does not affect the disk space reported for the files.</span></span> <span data-ttu-id="9dfcf-110">Par conséquent, les paramètres de quota sur un volume peuvent être comparés aux paramètres d’un autre volume.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-110">Therefore, quota settings on one volume can be compared to settings on another volume.</span></span>

<span data-ttu-id="9dfcf-111">Il existe deux types de limites de quota de disque, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-111">There are two types of disk quota limits, as shown in the following table.</span></span>



| <span data-ttu-id="9dfcf-112">Limite</span><span class="sxs-lookup"><span data-stu-id="9dfcf-112">Limit</span></span>                        | <span data-ttu-id="9dfcf-113">Description</span><span class="sxs-lookup"><span data-stu-id="9dfcf-113">Description</span></span>                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dfcf-114">Seuil d'avertissement</span><span class="sxs-lookup"><span data-stu-id="9dfcf-114">Warning threshold</span></span><br/> | <span data-ttu-id="9dfcf-115">Vous pouvez configurer le système pour générer une entrée de fichier journal système lorsque l’espace disque facturé à l’utilisateur dépasse cette valeur.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-115">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span><br/>                                                                                                                                         |
| <span data-ttu-id="9dfcf-116">Quota de disque dur</span><span class="sxs-lookup"><span data-stu-id="9dfcf-116">Hard quota</span></span><br/>        | <span data-ttu-id="9dfcf-117">Vous pouvez configurer le système pour générer une entrée de fichier journal système lorsque l’espace disque facturé à l’utilisateur dépasse cette valeur.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-117">You can configure the system to generate a system logfile entry when the disk space charged to the user exceeds this value.</span></span> <span data-ttu-id="9dfcf-118">Vous pouvez également configurer le système pour refuser de l’espace disque supplémentaire à l’utilisateur lorsque l’espace disque facturé à l’utilisateur dépasse cette valeur.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-118">You can also configure the system to deny additional disk space to the user when the disk space charged to the user exceeds this value.</span></span><br/> |



 

<span data-ttu-id="9dfcf-119">Le système de fichiers NTFS crée automatiquement une entrée de quota utilisateur lorsqu’un utilisateur écrit pour la première fois sur le volume.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-119">The NTFS file system automatically creates a user quota entry when a user first writes to the volume.</span></span> <span data-ttu-id="9dfcf-120">Les entrées créées automatiquement se voient attribuer le seuil d’avertissement par défaut et les valeurs de limite de quota matériel pour le volume.</span><span class="sxs-lookup"><span data-stu-id="9dfcf-120">Entries that are created automatically are assigned the default warning threshold and hard quota limit values for the volume.</span></span>

 

 




