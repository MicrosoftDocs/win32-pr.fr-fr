---
description: TAPI 2,0 fournit un petit nombre d’améliorations apportées à la fonctionnalité de base de l’interface TAPI 1,4.
ms.assetid: f3a319b4-5e82-4bf9-bd89-a027d58ad126
title: TAPI 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 926def5cf2348396b9197a83e17b35d9a91d4dee617e00abe4c02d0428f2884e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861245"
---
# <a name="tapi-20"></a>TAPI 2,0

TAPI 2,0 fournit un petit nombre d’améliorations apportées à la fonctionnalité de base de l’interface TAPI 1,4. Toutefois, il y avait des modifications architecturales majeures qui ont beaucoup amélioré sa stabilité. La plupart des modifications étaient des modifications fondamentales nécessaires pour que l’interface TAPI soit Windows NT 4,0 et tirer parti de ses fonctionnalités (prise en charge complète de 32 bits, services et Unicode). Toutefois, ces modifications étaient internes à l’interface TAPI et avaient peu d’effet sur les applications TAPI.

les applications qui prennent en charge l’interface TAPI 1,3 et 1,4 (applications 16 bits par le biais d’une couche de conversion) fonctionnent bien sur les systèmes d’exploitation Windows Server 2003, Windows XP, Windows 2000 et Windows NT. Toutefois, l’effet sur les développeurs de fournisseurs de services était important. Les fournisseurs de services pour ces systèmes d’exploitation doivent être des dll Unicode entièrement 32 bits qui peuvent s’exécuter dans le contexte de TAPISRV, et non dans le contexte de l’application TAPI (comme pour tous les TSPs basés sur Win16 précédents). TSPs conçu pour TAPI 1,4 ne fonctionne pas sur les systèmes d’exploitation Windows Server 2003, Windows XP, Windows 2000 ou Windows NT.

TAPI 2,0 ajoute également les fonctionnalités importantes de la prise en charge du centre d’appels et de la qualité de service (QOS).

les binaires système tapi fournis avec Windows prennent en charge tapi versions 1,3 et 1,4 pour toutes les applications. Toutefois, les applications 16 bits ne peuvent pas utiliser TAPI 2,0 et vous ne pouvez pas utiliser un TSP TAPI 2. x de 16 bits.

 

 



