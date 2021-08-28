---
description: Encapsulez le disque dur dans un fichier unique pour qu’il soit utilisé par le système d’exploitation en tant que disque virtuel. Les disques virtuels peuvent fonctionner comme des disques de démarrage et peuvent héberger des systèmes de fichiers natifs (NTFS, FAT, exFAT et UDF) tout en prenant en charge les opérations de disque et de fichier standard.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Disque virtuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfa2d39ea786029e8be319d7affaa2214682ce05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480985"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Disque virtuel

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Objectif

Le format de disque dur virtuel (VHD) est une spécification de format d’image disponible publiquement qui spécifie un disque dur virtuel encapsulé dans un fichier unique, capable d’héberger des systèmes de fichiers natifs tout en prenant en charge les opérations de disque et de fichier standard. l’utilisation des fichiers VHD est un exemple de la fonctionnalité [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) dans Windows server 2008, virtual Server et Windows virtual PC. ces produits utilisent des disques durs virtuels pour contenir l’image du système d’exploitation Windows utilisée par une machine virtuelle comme disque de démarrage système.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Développeurs concernés

le kit de développement logiciel (SDK) Microsoft Windows intègre la prise en charge du disque dur virtuel natif pour l’utilisation des disques durs virtuels, ce qui permet aux développeurs et aux administrateurs de créer, gérer et déployer plus facilement des images Windows dans des disques durs virtuels à l’aide des outils de gestion ou de prise en charge des API de plateforme. Il n’est pas nécessaire d’installer des applications distinctes ou d’implémenter un analyseur de format VHD pour activer ces opérations. Ces API permettent l’utilisation générique de disques durs virtuels indépendants de toute autre technologie de virtualisation.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Spécifications d’exécution

le disque dur virtuel est pris en charge sur Windows 7 et Windows Server 2008 R2.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>Dans cette section


| Rubrique | Description | 
|-------|-------------|
| <p><a href="about-vhd.md">À propos du disque dur virtuel</a></p> | <p>Décrit le format VHD avec des conseils et des suggestions d’utilisation de l’API.</p> | 
| <p><a href="vhd-reference.md">Référence VHD</a></p> | <p>Décrit les fonctions, structures et énumérations des API VHD.</p> | 


 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Rubriques connexes

[Service Disque virtuel](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
