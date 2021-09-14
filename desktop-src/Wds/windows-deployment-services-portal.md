---
title: Services de déploiement Windows
description: déployer des systèmes d’exploitation Windows. Configurez de nouveaux clients avec une installation réseau sans obliger les administrateurs à visiter chaque ordinateur ou à installer directement à partir d’un CD ou d’un DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows services de déploiement Windows les services de déploiement
- Windows services de déploiement Windows les services de déploiement, page d’hébergement
- services de déploiement Windows les services de déploiement
- WDS Windows les services de déploiement voir services de déploiement Windows
- services d’Installation à distance Windows les services de déploiement voir services de déploiement Windows
- services de déploiement Windows RIS voir services de déploiement Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292242"
---
# <a name="windows-deployment-services"></a>Services de déploiement Windows

## <a name="purpose"></a>Objectif

Windows Les services de déploiement (WDS) sont la version révisée des services d’installation à distance (RIS). WDS permet le déploiement de systèmes d’exploitation Windows. Vous pouvez utiliser WDS pour configurer de nouveaux clients avec une installation réseau sans obliger les administrateurs à visiter chaque ordinateur ou à installer directement à partir d’un CD ou d’un DVD.

## <a name="developer-audience"></a>Développeurs concernés

L’audience principale du développeur de l’API WDS concerne les groupes qui développent des outils et des processus personnalisés pour l’informatique et d’autres groupes d’administration de l’ordinateur. dans les environnements où la solution standard Windows Deployment Services (WDS) ne peut pas être utilisée, l’API wds autorise l’accès par programmation à certains composants de wds.

les fabricants oem (Original equipment manufacturers), les intégrateurs de systèmes et les professionnels de l’informatique d’entreprise qui recherchent des informations sur la façon de déployer des Windows sur de nouveaux ordinateurs doivent voir les informations relatives à la solution standard Windows deployment services (WDS) dans le [Guide pas à pas de la mise à jour des services de déploiement Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) et le [Kit d’installation automatisée (Windows AIK) (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="run-time-requirements"></a>Conditions d’exécution

WDS est disponible en tant que module complémentaire pour Windows server 2003 avec service pack 1 (SP1) et est inclus dans le système d’exploitation à partir de Windows server 2003 avec service pack 2 (SP2) et Windows server 2008. L’API du serveur PXE WDS requiert que le rôle serveur WDS sur le serveur implémente des fournisseurs PXE personnalisés. l’API cliente WDS requiert la phase de traitement de l’installation de Microsoft environnement de préinstallation Windows (WinPE) (Windows PE 2,0). une image de démarrage RAMDISK de Windows PE 2,0 dans le. Le format WIM doit être téléchargé dans le cadre du processus de démarrage réseau pour implémenter des clients WDS personnalisés.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                 | Description                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [à propos de l’API Windows Deployment Services](about-the-windows-deployment-services-api.md)<br/> | Informations générales sur l’API du serveur WDS et l’API client WDS.<br/>    |
| [Windows Référence des services de déploiement](windows-deployment-services-reference.md)<br/>         | décrit les structures et les fonctions des Services de déploiement Windows.<br/> |



 

 

