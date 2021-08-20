---
description: Microsoft Hyper-V server fournit un environnement de gestion d’ordinateurs virtuels évolutif, fiable et hautement disponible. Le logiciel de machine virtuelle Hyper-V consolide les serveurs, ainsi que les environnements de développement et de test.
ms.assetid: 3359A33F-528B-4955-8B37-30523B8AD33A
title: Fournisseur WMI Hyper-V (v2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b82156754f085196eaece86bb4996c1b4a0bb8348e1566894ee78d4921676f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014247"
---
# <a name="hyper-v-wmi-provider-v2"></a>Fournisseur WMI Hyper-V (v2)

## <a name="purpose"></a>Objectif

Hyper-V fournit un environnement informatique de serveur virtualisé évolutif, fiable et hautement disponible. Il permet à un ou plusieurs systèmes d’exploitation invités de s’exécuter simultanément sur un seul ordinateur physique. Les principales utilisations de la technologie des machines virtuelles sont les suivantes :

-   Consolidation de serveurs
-   Consolidation des environnements de développement et de test
-   Récupération d’urgence simplifiée

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                 | Description                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [À propos du fournisseur WMI Hyper-V](about-the-virtualization-wmi-provider.md)<br/>                | Le fournisseur WMI pour Hyper-V permet aux développeurs et aux scripteurs de créer rapidement des outils personnalisés, des utilitaires et des améliorations pour la plate-forme de virtualisation. Les interfaces WMI peuvent gérer tous les aspects des services Hyper-V.<br/> |
| [Utilisation du fournisseur WMI Hyper-V](using-the-virtualization-wmi-provider.md)<br/>                | Les rubriques suivantes décrivent comment utiliser le fournisseur WMI Hyper-V.<br/>                                                                                                                                                            |
| [Classes WMI Hyper-V](hyper-v-wmi-classes.md)<br/>                                             | Les classes WMI Hyper-V sont les suivantes.<br/>                                                                                                                                                                                    |
| [API de surveillance de l’intégrité des applications Hyper-V](hyper-v-application-health-monitoring-api.md)<br/> | L’API de surveillance de l’intégrité des applications Hyper-V est utilisée pour surveiller l’état d’intégrité des applications qui s’exécutent sur une machine virtuelle.<br/>                                                                                               |
| [API de réplication Hyper-V](hyper-v-replication-api.md)<br/>                                     | L’API de réplication Hyper-V est utilisée pour contrôler la réplication de l’ordinateur virtuel et la récupération du basculement.<br/>                                                                                                                             |
| [API métriques Hyper-V](hyper-v-metrics-api.md)<br/>                                             | L’API métriques Hyper-V permet de surveiller l’état d’intégrité des applications qui s’exécutent sur une machine virtuelle.<br/>                                                                                                                     |
| [API réseau Hyper-V](hyper-v-networking-api.md)<br/>                                       | L’API de mise en réseau Hyper-V est utilisée pour contrôler la mise en réseau dans Hyper-V.<br/>                                                                                                                                                          |
| [API de migration Hyper-V](hyper-v-storage-migration-api.md)<br/>                                 | L’API de migration Hyper-V est utilisée pour contrôler le stockage et la migration dynamique dans Hyper-V.<br/>                                                                                                                                           |
| [API Virtual Fibre Channel Hyper-V](hyper-v-virtual-fiber-channels-api.md)<br/>                | L’API de Fibre Channel virtuel Hyper-V est utilisée pour contrôler les adaptateurs de Fibre Channel virtuels dans Hyper-V.<br/>                                                                                                                           |
| [API de placement de machine virtuelle Hyper-V](hyper-v-vm-placement-api.md)<br/>                                   | L’API de placement de machine virtuelle Hyper-V contient les informations de compatibilité pour les machines virtuelles ou le système informatique d’hébergement.<br/>                                                                                                        |
| [Classes de seuil](threshold-classes.md)<br/>                                                 | Contient les classes introduites dans Windows 10.<br/>                                                                                                                                                                                |
| [Classes RS2](redstone-classes.md)<br/>                                                        | contient les nouvelles classes pour Windows 10, version 1703.<br/>                                                                                                                                                                        |
| [Classes RS3](rs3-classes.md)<br/>                                                             | contient les nouvelles classes pour Windows 10, version 1709.<br/>                                                                                                                                                                        |
| [Glossaire Hyper-V](virtualization-glossary.md)<br/>                                            | glossaire des termes utilisés dans la documentation du kit de développement logiciel (SDK) Windows virtualization.<br/>                                                                                                                                                       |



 

## <a name="run-time-requirements"></a>Conditions d’exécution

Les services Hyper-V requièrent un système x64 qui prend en charge la virtualisation d’assistance matérielle exécutant Hyper-V. Toutefois, les programmes qui interagissent avec les interfaces WMI Hyper-V peuvent s’exécuter à distance sur n’importe quel système qui prend en charge WMI.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hyper-V (bibliothèque technique de Windows Server 2008 R2)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc753637(v=ws.10))
</dt> <dt>

[Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page)
</dt> <dt>

[Windows Virtualisation de serveur](https://www.microsoft.com/windowsserver2008/virtualization/default.mspx)
</dt> </dl>

 

