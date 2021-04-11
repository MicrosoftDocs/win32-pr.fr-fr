---
title: Gestionnaire de redémarrage
description: Écrire des programmes d’installation personnalisés pour éliminer les redémarrages du système requis pour terminer la mise à jour d’un fichier en cours d’utilisation. Arrêtez et redémarrez tous les services système sauf critiques à partir des programmes.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Gestionnaire de redémarrage du gestionnaire de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031577"
---
# <a name="restart-manager"></a>Gestionnaire de redémarrage

## <a name="purpose"></a>Objectif

L’API gestionnaire de redémarrage permet d’éliminer ou de réduire le nombre de redémarrages système nécessaires à l’exécution d’une installation ou d’une mise à jour. La raison principale pour laquelle les mises à jour logicielles nécessitent un redémarrage du système lors d’une installation ou d’une mise à jour est que certains des fichiers en cours de mise à jour sont actuellement utilisés par une application ou un service en cours d’exécution. Le gestionnaire de redémarrage permet l’arrêt et le redémarrage de tous les [services système sauf les services critiques](critical-system-services.md) . Cela permet de libérer les fichiers en cours d’utilisation et de permettre l’exécution des opérations d’installation.

## <a name="where-applicable"></a>Le cas échéant

La DLL du gestionnaire de redémarrage exporte une interface C publique qui peut être chargée par des programmes d’installation standard ou personnalisés. Le programme d’installation peut utiliser le gestionnaire de redémarrage pour inscrire les fichiers qui doivent être remplacés lors de l’installation d’une application ou d’une mise à jour. Ensuite, lors d’une mise à jour ou d’une installation ultérieure, le programme d’installation peut utiliser le gestionnaire de redémarrage pour déterminer les fichiers qui ne peuvent pas être mis à jour, car ils sont en cours d’utilisation. Le gestionnaire de redémarrage peut arrêter et redémarrer les services non critiques ou les applications qui utilisent actuellement ces fichiers. Les programmes d’installation peuvent demander au gestionnaire de redémarrage d’arrêter et de redémarrer les applications ou les services en fonction du fichier utilisé, de l’ID de processus (PID) ou du nom abrégé d’un service Windows.

Le gestionnaire de redémarrage est destiné au développement d’applications de style bureau.

## <a name="developer-audience"></a>Développeurs concernés

Cette documentation est destinée aux développeurs d’applications d’installation qui souhaitent tirer parti des fonctionnalités du programme d’installation de Windows Vista ou Windows Server 2008. Les applications qui utilisent la version 4,0 de [Windows Installer](/windows/desktop/Msi/windows-installer-portal) pour l’installation et la maintenance utilisent automatiquement le gestionnaire de redémarrage pour réduire les redémarrages du système. Les programmes d’installation personnalisés peuvent également être conçus pour appeler l’API du gestionnaire de redémarrage pour arrêter et redémarrer les applications et les services. Dans les cas où un redémarrage du système est inévitable, les programmes d’installation peuvent utiliser l’API du gestionnaire de redémarrage pour planifier les redémarrages de manière à réduire au minimum l’interruption du processus de travail de l’utilisateur.

## <a name="run-time-requirements"></a>Conditions d’exécution

L’API du gestionnaire de redémarrage est disponible à partir de Windows Vista et de Windows Server 2008. Le gestionnaire de redémarrage se compose d’une seule DLL que les applications peuvent charger pour accéder à l’API du gestionnaire de redémarrage.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                 | Description                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [À propos du gestionnaire de redémarrage](about-restart-manager.md)<br/>         | Rubriques de vue d’ensemble qui décrivent le gestionnaire de redémarrage.<br/>   |
| [Utilisation du gestionnaire de redémarrage](using-restart-manager.md)<br/>         | Rubriques de présentation sur l’utilisation de l’API du gestionnaire de redémarrage.<br/> |
| [Référence du gestionnaire de redémarrage](restart-manager-reference.md)<br/> | Rubriques de référence pour l’API du gestionnaire de redémarrage.<br/>        |



 

 

