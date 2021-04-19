---
title: Services de déploiement Windows
description: Déployez des systèmes d’exploitation Windows. Configurez de nouveaux clients avec une installation réseau sans obliger les administrateurs à visiter chaque ordinateur ou à installer directement à partir d’un CD ou d’un DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Services de déploiement Windows (services de déploiement Windows)
- Services de déploiement Windows Services de déploiement Windows, page d’hébergement
- services de déploiement Windows Deployment Services
- Services de déploiement Windows WDS voir services de déploiement Windows
- Services d’installation à distance services de déploiement Windows Voir services de déploiement Windows
- Services de déploiement Windows RIS voir services de déploiement Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512525"
---
# <a name="windows-deployment-services"></a>Services de déploiement Windows

## <a name="purpose"></a>Objectif

Les services de déploiement Windows (WDS) sont la version révisée des services d’installation à distance (RIS). WDS permet le déploiement de systèmes d’exploitation Windows. Vous pouvez utiliser WDS pour configurer de nouveaux clients avec une installation réseau sans obliger les administrateurs à visiter chaque ordinateur ou à installer directement à partir d’un CD ou d’un DVD.

## <a name="developer-audience"></a>Développeurs concernés

L’audience principale du développeur de l’API WDS concerne les groupes qui développent des outils et des processus personnalisés pour l’informatique et d’autres groupes d’administration de l’ordinateur. Dans les environnements où la solution standard des services de déploiement Windows (WDS) ne peut pas être utilisée, l’API WDS autorise l’accès par programmation à certains composants de WDS.

Les fabricants OEM (Original Equipment Manufacturers), les intégrateurs de systèmes et les professionnels de l’informatique d’entreprise qui recherchent des informations sur le déploiement de Windows sur de nouveaux ordinateurs doivent voir les informations relatives à la solution Windows Deployment Services (WDS) standard dans le [Guide pas à pas de la mise à jour des services de déploiement Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) et le [Kit d’installation automatisée (Windows AIK) (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="run-time-requirements"></a>Conditions d’exécution

WDS est disponible en tant que module complémentaire pour Windows Server 2003 avec Service Pack 1 (SP1) et est inclus dans le système d’exploitation à partir de Windows Server 2003 avec Service Pack 2 (SP2) et Windows Server 2008. L’API du serveur PXE WDS requiert que le rôle serveur WDS sur le serveur implémente des fournisseurs PXE personnalisés. L’API cliente WDS requiert la phase de traitement de l’installation de Microsoft environnement de préinstallation Windows (WinPE) (Windows PE 2,0). Une image de démarrage RAMDISK de Windows PE 2,0 dans le. Le format WIM doit être téléchargé dans le cadre du processus de démarrage réseau pour implémenter des clients WDS personnalisés.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                 | Description                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [À propos de l’API des services de déploiement Windows](about-the-windows-deployment-services-api.md)<br/> | Informations générales sur l’API du serveur WDS et l’API client WDS.<br/>    |
| [Informations de référence sur les services de déploiement Windows](windows-deployment-services-reference.md)<br/>         | Décrit les fonctions et les structures des services de déploiement Windows.<br/> |



 

 

