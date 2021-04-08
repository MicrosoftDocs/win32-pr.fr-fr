---
title: À propos du gestionnaire de redémarrage
description: La raison principale pour laquelle l’installation et les mises à jour du logiciel nécessitent un redémarrage du système est que certains des fichiers en cours de mise à jour sont actuellement utilisés par une application ou un service en cours d’exécution.
ms.assetid: 9a1166d7-a0e1-4948-9077-278c84afccac
keywords:
- Restart Manager restart Mgr, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1cfd300d554e311ab43cc0a9413514b6b60081
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729573"
---
# <a name="about-restart-manager"></a>À propos du gestionnaire de redémarrage

La raison principale pour laquelle l’installation et les mises à jour du logiciel nécessitent un redémarrage du système est que certains des fichiers en cours de mise à jour sont actuellement utilisés par une application ou un service en cours d’exécution. Le gestionnaire de redémarrage permet l’arrêt et le redémarrage de tous les services et applications critiques. Cela libère les fichiers en cours d’utilisation et permet d’effectuer les opérations d’installation. Il peut également éliminer ou réduire le nombre de redémarrages système nécessaires à l’exécution d’une installation ou d’une mise à jour.

Le gestionnaire de redémarrage arrête les applications dans l’ordre suivant, et une fois que les applications ont été mises à jour, redémarre les applications qui ont été inscrites pour le redémarrage dans l’ordre inverse.

1.  Applications GUI
2.  Applications console
3.  Services Windows
4.  Explorateur Windows

Le gestionnaire de démarrage arrête l’application ou les services uniquement si l’appelant est autorisé à le faire. Notez que l’arrêt entre sessions n’est pas pris en charge.

Les applications qui utilisent la version 4,0 de [Windows Installer](/windows/desktop/Msi/windows-installer-portal) pour l’installation et la maintenance utilisent automatiquement le gestionnaire de redémarrage pour réduire les redémarrages du système. Les programmes d’installation personnalisés peuvent également être conçus pour appeler l’API du gestionnaire de redémarrage pour arrêter et redémarrer les applications et les services. Dans les cas où un redémarrage du système est inévitable, les programmes d’installation peuvent utiliser l’API du gestionnaire de redémarrage pour planifier les redémarrages de manière à réduire au minimum l’interruption du processus de travail de l’utilisateur.

Pour plus d’informations sur l’utilisation de l’API du gestionnaire de redémarrage pendant l’installation et les mises à jour, consultez [utilisation du gestionnaire de redémarrage](using-restart-manager.md).

Les services système critiques ne peuvent pas être arrêtés et redémarrés par le gestionnaire de redémarrage sans redémarrage du système. Pour plus d’informations sur l’identification des services système critiques, consultez [services système critiques](critical-system-services.md).

Vos applications et services doivent être prêts à être arrêtés par le gestionnaire de redémarrage et enregistrer les données utilisateur et les informations d’État nécessaires pour un redémarrage propre. Pour plus d’informations sur la façon de préparer vos applications et services pour qu’ils fonctionnent avec le gestionnaire de redémarrage, consultez [instructions pour les applications et les services](guidelines-for-applications-and-services.md).

Pour obtenir des informations de référence sur les énumérations, les structures et les fonctions de l’API du gestionnaire de redémarrage, consultez la section [Référence du gestionnaire de redémarrage](restart-manager-reference.md) .

 

 