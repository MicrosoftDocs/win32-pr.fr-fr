---
description: Un filtre de capture est un élément d’une application NPP qui indique au pilote de Moniteur réseau (Nmnt.sys) les trames de données réseau à conserver et les trames à ignorer.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: À propos des filtres de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536365"
---
# <a name="about-capture-filters"></a>À propos des filtres de capture

Un filtre de capture est un élément d’une application NPP qui indique au pilote de Moniteur réseau (Nmnt.sys) les trames de données réseau à conserver et les trames à ignorer. L’avantage de définir un filtre de capture est plus efficace. Vous n’avez pas besoin d’examiner les frames capturés. le pilote Moniteur réseau les examine. Cette approche élimine la copie de frame, qui offre un avantage de l’utilisation de la mémoire.

## <a name="capture-filter-structure"></a>Structure de filtre de capture

Les filtres de capture se composent de trois éléments :

-   Paramètres ETYPE/SAP
-   Adresse
-   Correspondance de modèle

Ensemble, ces éléments évaluent logiquement les frames à inclure ou à exclure au cours de l’opération d’une application NPP. Le filtre de capture fournit des correspondances et des exclusions complexes d’éléments de frame à l’application NPP.

Moniteur réseau implémente le filtre de capture via une structure de données, [**capturefilter**](the-capturefilter-structure.md), passée au NPP, puis transmis au pilote Moniteur réseau au démarrage de la capture.

Pour plus d’informations sur les opérations NPP et les fonctionnalités d’objet BLOB, consultez [fournisseurs de paquets réseau](network-packet-providers.md) et [objets BLOB de moniteur réseau](network-monitor-blobs.md).

 

 



