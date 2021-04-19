---
description: 'Les clusters peuvent être référencés à partir de deux perspectives différentes : dans le fichier et sur le volume.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Clusters et étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545824"
---
# <a name="clusters-and-extents"></a><span data-ttu-id="e68dd-103">Clusters et étendues</span><span class="sxs-lookup"><span data-stu-id="e68dd-103">Clusters and Extents</span></span>

<span data-ttu-id="e68dd-104">Les clusters peuvent être référencés à partir de deux perspectives différentes : dans le fichier et sur le volume.</span><span class="sxs-lookup"><span data-stu-id="e68dd-104">Clusters may be referred to from two different perspectives: within the file and on the volume.</span></span> <span data-ttu-id="e68dd-105">Tout cluster d’un fichier a un *numéro de cluster virtuel* (VCN), qui est son décalage relatif par rapport au début du fichier.</span><span class="sxs-lookup"><span data-stu-id="e68dd-105">Any cluster in a file has a *virtual cluster number* (VCN), which is its relative offset from the beginning of the file.</span></span> <span data-ttu-id="e68dd-106">Par exemple, une recherche sur deux fois la taille d’un cluster, suivie d’une lecture, renverra des données en commençant au troisième VCN.</span><span class="sxs-lookup"><span data-stu-id="e68dd-106">For example, a seek to twice the size of a cluster, followed by a read, will return data beginning at the third VCN.</span></span> <span data-ttu-id="e68dd-107">Un *numéro de cluster logique* (LCN) décrit le décalage d’un cluster à partir d’un point arbitraire au sein du volume.</span><span class="sxs-lookup"><span data-stu-id="e68dd-107">A *logical cluster number* (LCN) describes the offset of a cluster from some arbitrary point within the volume.</span></span> <span data-ttu-id="e68dd-108">LCNs doit être traité uniquement comme des nombres ordinaux ou relatifs.</span><span class="sxs-lookup"><span data-stu-id="e68dd-108">LCNs should be treated only as ordinal, or relative, numbers.</span></span> <span data-ttu-id="e68dd-109">Il n’existe aucun mappage garanti de clusters logiques vers des secteurs de lecteur de disque dur physique.</span><span class="sxs-lookup"><span data-stu-id="e68dd-109">There is no guaranteed mapping of logical clusters to physical hard disk drive sectors.</span></span>

<span data-ttu-id="e68dd-110">Une *extension* est une exécution de clusters contigus.</span><span class="sxs-lookup"><span data-stu-id="e68dd-110">An *extent* is a run of contiguous clusters.</span></span> <span data-ttu-id="e68dd-111">Supposons, par exemple, qu’un fichier composé de 30 clusters soit enregistré dans deux extensions.</span><span class="sxs-lookup"><span data-stu-id="e68dd-111">For example, suppose a file consisting of 30 clusters is recorded in two extents.</span></span> <span data-ttu-id="e68dd-112">La première extension peut être constituée de cinq clusters contigus, l’autre des 25 clusters restants.</span><span class="sxs-lookup"><span data-stu-id="e68dd-112">The first extent might consist of five contiguous clusters, the other of the remaining 25 clusters.</span></span>

<span data-ttu-id="e68dd-113">Il n’existe aucune garantie de relation sur le disque, quelle que soit l’étendue de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="e68dd-113">There is no guarantee of any relationship on the disk of any extent to any other extent.</span></span> <span data-ttu-id="e68dd-114">Par exemple, la première extension peut être à un LCN plus élevé qu’une autre étendue.</span><span class="sxs-lookup"><span data-stu-id="e68dd-114">For example, the first extent may be at a higher LCN than a subsequent extent.</span></span>

 

 



