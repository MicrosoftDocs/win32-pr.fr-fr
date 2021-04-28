---
description: Mémoire dynamique
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: Mémoire dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcc54a1b85f4fc39bf6383e05a2e6e535edd1d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088467"
---
# <a name="dynamic-memory"></a>Mémoire dynamique

## <a name="affected-platforms"></a>Plateformes affectées

**Clients (s’exécutant en tant qu’ordinateurs virtuels)** -Windows Vista \| Windows 7  
**Serveurs** -Windows Server 2008 R2 Hyper-V SP1  


## <a name="feature-impact"></a>Impact sur les fonctionnalités

 **Gravité** -faible  
**Fréquence** -élevée  






## <a name="description"></a>Description

À un niveau élevé, Hyper-V Mémoire dynamique est une amélioration de la gestion de la mémoire pour le rôle Hyper-V inclus dans Windows Server 2008 R2 SP1. Il est conçu pour une utilisation en production et permet aux clients d’obtenir des ratios plus élevés de densité de machines virtuelles et de consolidation tout en optimisant l’utilisation de la mémoire sur l’ordinateur physique. L’allocation de mémoire statique est réduite et la mémoire supplémentaire est allouée en fonction des besoins. Mémoire dynamique a un impact sur les développeurs de logiciels qui souhaitent s’assurer que leurs logiciels fonctionnent correctement dans un environnement de machine virtuelle.

## <a name="usage-scenario"></a>Scénario d'utilisation

Il existe deux scénarios d’utilisation de la clé où Mémoire dynamique entre en lecture, les applications côté hôte et les applications côté invité.

**Applications côté hôte (outils de gestion)**

Les anciens outils qui gèrent un nouveau serveur Windows Server 2008 R2 SP1 ne seront pas en mesure d’accéder aux nouveaux paramètres de Mémoire dynamique. De nouvelles API WMI et des compteurs de performances ont été développés pour gérer les nouveaux paramètres de Mémoire dynamique pour les machines virtuelles Hyper-V. Les développeurs de logiciels qui travaillent sur des outils de gestion doivent tirer parti de ces API et compteurs pour une utilisation avec Windows Server 2008 R2 SP1 avec le rôle Hyper-V installé. Des détails sur ces nouvelles API seront disponibles via [la documentation du fournisseur WMI Hyper-V sur MSDN](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider).

**Applications côté invité**

Les développeurs qui écrivent des logiciels pour une utilisation au sein d’une machine virtuelle configurée pour utiliser Mémoire dynamique doivent garder à l’esprit que la mémoire système de la machine virtuelle n’est plus constante. Par conséquent, leur application doit libérer de la mémoire lorsqu’il n’est plus nécessaire d’autoriser d’autres applications à tirer parti de la ressource.

Les allocations et les désallocations de mémoire continuent de fonctionner normalement pour les applications utilisateur. Mémoire dynamique est complètement transparent pour la plupart des applications des utilisateurs finaux. Toutefois, si le logiciel en cours de développement utilise des compteurs de performances de la mémoire dans l’ordinateur virtuel, un test minutieux doit être effectué dans un environnement Mémoire dynamique activé pour s’assurer que le logiciel prend en compte les modifications apportées à l’allocation de mémoire du système d’exploitation invité. La mémoire disponible n’est plus « statique » du point de vue de la machine virtuelle.

## <a name="solutions"></a>Solutions

Les machines virtuelles doivent disposer d’une version mise à jour d’Integration Services (SP1) pour pouvoir tirer parti de Mémoire dynamique. Assurez-vous que tous les ordinateurs utilisés dans la gestion des ordinateurs virtuels Hyper-V utilisent la dernière version de Windows Server 2008 R2 SP1.

## <a name="links-to-other-resources"></a>Liens vers d’autres ressources

-   [Mémoire dynamique en provenance du blog Hyper-V](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [Utilisation du fournisseur WMI Hyper-V](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>Clause d'exclusion de responsabilité

Les informations contenues dans ce document concernent le produit logiciel en version préliminaire qui peut être considérablement modifié avant sa première version commerciale. En conséquence, les informations peuvent ne pas décrire ou refléter le produit logiciel lors de la première publication commercialisée. Ce document est fourni à titre d’information uniquement. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
