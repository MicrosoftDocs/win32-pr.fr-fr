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
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Disque virtuel

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Objectif

Le format de disque dur virtuel (VHD) est une spécification de format d’image disponible publiquement qui spécifie un disque dur virtuel encapsulé dans un fichier unique, capable d’héberger des systèmes de fichiers natifs tout en prenant en charge les opérations de disque et de fichier standard. L’utilisation des fichiers VHD est un exemple de la fonctionnalité [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) dans windows Server 2008, Virtual Server et Windows Virtual PC. Ces produits utilisent des disques durs virtuels pour contenir l’image du système d’exploitation Windows utilisée par une machine virtuelle comme disque de démarrage système.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Développeurs concernés

Le kit de développement logiciel (SDK) Microsoft Windows intègre la prise en charge du disque dur virtuel natif pour l’utilisation des disques durs virtuels, ce qui permet aux développeurs et aux administrateurs de créer, gérer et déployer plus facilement des images Windows dans des disques durs virtuels à l’aide des outils de gestion ou de prise en charge des API de plateforme. Il n’est pas nécessaire d’installer des applications distinctes ou d’implémenter un analyseur de format VHD pour activer ces opérations. Ces API permettent l’utilisation générique de disques durs virtuels indépendants de toute autre technologie de virtualisation.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Spécifications d’exécution

Le disque dur virtuel est pris en charge sur Windows 7 et Windows Server 2008 R2.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Dans cette section

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="about-vhd.md">À propos du disque dur virtuel</a></p></td>
<td><p>Décrit le format VHD avec des conseils et des suggestions d’utilisation de l’API.</p></td>
</tr>
<tr class="even">
<td><p><a href="vhd-reference.md">Référence VHD</a></p></td>
<td><p>Décrit les fonctions, structures et énumérations des API VHD.</p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Rubriques connexes

[Service Disque virtuel](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
