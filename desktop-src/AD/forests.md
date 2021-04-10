---
title: Forêts
description: Une forêt est un ensemble d’une ou plusieurs arborescences de domaines qui ne forment pas un espace de noms contigu.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- forêts Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940820"
---
# <a name="forests"></a>Forêts

Une [*forêt*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) est un ensemble d’une ou plusieurs arborescences de domaines qui ne forment pas un espace de noms contigu. Toutes les arborescences d’une forêt partagent un schéma, une configuration et un catalogue global communs. Toutes les arborescences d’une forêt donnée font confiance à Exchange en fonction des relations d’approbation Kerberos transitives hiérarchiques. Contrairement aux arborescences, une forêt ne nécessite pas de nom distinct. Une forêt existe sous la forme d’un ensemble d’objets de référence croisée et de relations d’approbation Kerberos reconnues par les arborescences membres. Les arborescences d’une forêt forment une hiérarchie à des fins d’approbation Kerberos ; le nom de l’arborescence à la racine de l’arborescence d’approbation fait référence à une forêt donnée.

L’illustration suivante montre une forêt d’espaces de noms non contigus.

![forêt d’espaces de noms non contigus](images/forests.png)

 

 