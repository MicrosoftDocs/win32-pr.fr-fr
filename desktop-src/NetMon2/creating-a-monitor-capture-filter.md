---
description: La création d’un filtre de capture qui fonctionne avec Moniteur réseau est un processus en cinq étapes.
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: Création d’un filtre de capture d’analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527214"
---
# <a name="creating-a-monitor-capture-filter"></a>Création d’un filtre de capture d’analyse

La création d’un filtre de capture qui fonctionne avec Moniteur réseau est un processus en cinq étapes :

-   [Définition du filtre ETYPE ou SAP](writing-etypesap-filter-portion.md)
-   [Écriture du filtre ADDRESSTABLE](writing-addresstable-filter-portion.md)
-   [Écriture du filtre PATTERNMATCH](writing-the-patternmatch-filter.md)
-   [Découpage d’un frame](clipping-a-frame.md)
-   [Implémentation du code de filtre de capture](implementing-the-capture-filter-code.md)

Un [*filtre de capture*](c.md) est une série d’ajouts à l’objet BLOB NPP qui sélectionne les frames qui sont renvoyés à l’analyse. Si une analyse ne modifie pas l’objet BLOB NPP, le NPP passe en mode promiscuité et envoie tout le trafic réseau à l’analyse. Le NPP est plus efficace s’il peut réduire les données transmises à un pilote, de sorte qu’une analyse doit créer un filtre de capture. Une analyse définit son filtre de capture en écrivant dans l’objet BLOB NPP dans l’appel à la fonction [configure](imonitor-doconfigure.md) . Le MCSVC appelle ensuite le NPP avec l’objet BLOB NPP. Pour plus d’informations sur le filtre de capture, les [fournisseurs de paquets réseau](network-packet-providers.md) sur NPPs et les [objets BLOB Moniteur réseau](network-monitor-blobs.md) sur les fonctions BLOB, consultez filtres de [capture](capture-filters.md) .

 

 



