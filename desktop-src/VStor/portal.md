---
description: Encapsulez le disque dur dans un fichier unique pour qu’il soit utilisé par le système d’exploitation en tant que disque virtuel. Les disques virtuels peuvent fonctionner comme des disques de démarrage et peuvent héberger des systèmes de fichiers natifs (NTFS, FAT, exFAT et UDF) tout en prenant en charge les opérations de disque et de fichier standard.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disque virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044145f5d631b878b533bbd409fad5eda5b4863f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201450"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span data-ttu-id="a87ed-104"><span id="vhd.portal"></span>Disque virtuel</span><span class="sxs-lookup"><span data-stu-id="a87ed-104"><span id="vhd.portal"></span>Virtual Disk</span></span>

## <a name="span-idpurposespanpurpose"></a><span data-ttu-id="a87ed-105"><span id="purpose"></span>Objectif</span><span class="sxs-lookup"><span data-stu-id="a87ed-105"><span id="purpose"></span>Purpose</span></span>

<span data-ttu-id="a87ed-106">Le format de disque dur virtuel (VHD) est une spécification de format d’image disponible publiquement qui spécifie un disque dur virtuel encapsulé dans un fichier unique, capable d’héberger des systèmes de fichiers natifs tout en prenant en charge les opérations de disque et de fichier standard.</span><span class="sxs-lookup"><span data-stu-id="a87ed-106">The Virtual Hard Disk (VHD) format is a publicly-available image format specification that specifies a virtual hard disk encapsulated in a single file, capable of hosting native file systems while supporting standard disk and file operations.</span></span> <span data-ttu-id="a87ed-107">L’utilisation des fichiers VHD est un exemple de la fonctionnalité [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) dans windows Server 2008, Virtual Server et Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a87ed-107">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="a87ed-108">Ces produits utilisent des disques durs virtuels pour contenir l’image du système d’exploitation Windows utilisée par une machine virtuelle comme disque de démarrage système.</span><span class="sxs-lookup"><span data-stu-id="a87ed-108">These products use VHDs to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span data-ttu-id="a87ed-109"><span id="developer_audience_heading"></span>Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="a87ed-109"><span id="developer_audience_heading"></span>Developer audience</span></span>

<span data-ttu-id="a87ed-110">Le kit de développement logiciel (SDK) Microsoft Windows intègre la prise en charge du disque dur virtuel natif pour l’utilisation des disques durs virtuels, ce qui permet aux développeurs et aux administrateurs de créer, gérer et déployer plus facilement des images Windows dans des disques durs virtuels à l’aide des outils de gestion ou de prise en charge des API de plateforme.</span><span class="sxs-lookup"><span data-stu-id="a87ed-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with VHDs, making it easier for developers and administrators to create, manage, and deploy Windows images in VHDs using the platform API support or management tools.</span></span> <span data-ttu-id="a87ed-111">Il n’est pas nécessaire d’installer des applications distinctes ou d’implémenter un analyseur de format VHD pour activer ces opérations.</span><span class="sxs-lookup"><span data-stu-id="a87ed-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="a87ed-112">Ces API permettent l’utilisation générique de disques durs virtuels indépendants de toute autre technologie de virtualisation.</span><span class="sxs-lookup"><span data-stu-id="a87ed-112">These APIs allow for generic use of VHDs independent of any other virtualization technologies.</span></span>

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span data-ttu-id="a87ed-113"><span id="run_time_requirements_heading"></span>Spécifications d’exécution</span><span class="sxs-lookup"><span data-stu-id="a87ed-113"><span id="run_time_requirements_heading"></span>Run-time requirements</span></span>

<span data-ttu-id="a87ed-114">Le disque dur virtuel est pris en charge sur Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a87ed-114">VHD is supported on Windows 7 and Windows Server 2008 R2.</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="a87ed-115"><span id="in_this_section"></span>Dans cette section</span><span class="sxs-lookup"><span data-stu-id="a87ed-115"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a87ed-116">Rubrique</span><span class="sxs-lookup"><span data-stu-id="a87ed-116">Topic</span></span></th>
<th><span data-ttu-id="a87ed-117">Description</span><span class="sxs-lookup"><span data-stu-id="a87ed-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a87ed-118"><a href="about-vhd.md">À propos du disque dur virtuel</a></span><span class="sxs-lookup"><span data-stu-id="a87ed-118"><a href="about-vhd.md">About VHD</a></span></span></p></td>
<td><p><span data-ttu-id="a87ed-119">Décrit le format VHD avec des conseils et des suggestions d’utilisation de l’API.</span><span class="sxs-lookup"><span data-stu-id="a87ed-119">Describes the VHD format with API usage tips and suggestions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a87ed-120"><a href="vhd-reference.md">Référence VHD</a></span><span class="sxs-lookup"><span data-stu-id="a87ed-120"><a href="vhd-reference.md">VHD Reference</a></span></span></p></td>
<td><p><span data-ttu-id="a87ed-121">Décrit les fonctions, structures et énumérations des API VHD.</span><span class="sxs-lookup"><span data-stu-id="a87ed-121">Describes the VHD API functions, structures, and enumerations.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="a87ed-122"><span id="related_topics"></span>Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a87ed-122"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="a87ed-123">Service Disque virtuel</span><span class="sxs-lookup"><span data-stu-id="a87ed-123">Virtual Disk Service</span></span>](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
