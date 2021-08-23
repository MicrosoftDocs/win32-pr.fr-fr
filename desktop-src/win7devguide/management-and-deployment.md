---
title: Gestion et déploiement
description: les professionnels de l’informatique ou les développeurs qui se préparent à déployer Windows 7 auront une confiance accrue et présenteront un plus petit cycle d’évaluation en raison des améliorations apportées aux outils et fonctionnalités de création d’images.
ms.assetid: 217090c4-6385-4333-a380-f75f2c80e369
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4a68a2c20f3ff765fcb9855afe1bd0455904088e3558562ec5c1cd0402e5c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964601"
---
# <a name="management-and-deployment"></a>Gestion et déploiement

les professionnels de l’informatique ou les développeurs qui se préparent à déployer Windows 7 auront une confiance accrue et présenteront un plus petit cycle d’évaluation en raison des améliorations apportées aux outils et fonctionnalités de création d’images. Cela inclut la prise en charge de la gestion des applications, des pilotes et des systèmes d’exploitation dans les fichiers image hors connexion. En outre, la création et la gestion d’images seront plus faciles et seront disponibles pour un plus grand nombre d’organisations informatiques. le déploiement de Windows 7 sur les ordinateurs d’entreprise sera également plus facile et plus rapide grâce aux nouveaux outils de migration informatique et aux technologies de déploiement automatisé.

## <a name="windows-powershell-20"></a>Windows PowerShell 2.0

PowerShell est un langage de script géré Microsoft .NET complet qui possède un interpréteur de ligne de commande interactif et un environnement d’écriture de scripts intégré (ISE). Il prend en charge la création de branches, les boucles, les fonctions, le débogage, la gestion des exceptions et l’internationalisation. PowerShell 2,0 fait partie de Windows 7 et offre de nombreuses améliorations et un ensemble croissant d' *applets* de commande pour les diagnostics Windows, Microsoft Active Directory, Microsoft Internet Information Services (IIS) et bien plus encore.

La fonctionnalité de communication à distance PowerShell 2,0 permet désormais aux utilisateurs d’exécuter des commandes sur un ou plusieurs ordinateurs distants à partir d’un seul ordinateur exécutant PowerShell. Les développeurs peuvent également héberger PowerShell sur IIS pour accéder et gérer leurs serveurs.

PowerShell 2,0 prend en charge le partitionnement et l’organisation de scripts PowerShell à l’aide de modules qui peuvent être distribués et déployés en tant qu’unités autonomes réutilisables. Elle prend également en charge les transactions dans le moteur PowerShell et les API, ce qui signifie que les développeurs peuvent démarrer, valider et restaurer les transactions à l’aide des *applets* de commande de transaction intégrées. En outre, le moteur PowerShell offre une prise en charge des événements pour l’écoute, le transfert et l’action des événements système et de gestion. Les applications PowerShell peuvent être écrites pour s’abonner à certains événements en vue d’un traitement synchrone ou asynchrone. (Voir [Windows PowerShell](https://msdn.microsoft.com/library/bb905330.aspx).)

![capture d’écran Windows PowerShell ISE](images/windows7-devguide-solidfig1-powershell.jpg)

Figure 1. Windows PowerShell est un langage de script géré .net complet qui possède un interpréteur de ligne de commande interactif et un environnement ISE graphique

## <a name="windows-installer"></a>Windows Installer

Windows Le programme d’installation a été mis à jour pour améliorer l’efficacité des développeurs en réduisant la quantité de code personnalisé nécessaire à la création d’un package d’installation et en créant de véritables installations logicielles par utilisateur.

Plusieurs transactions de package permettent aux développeurs de créer une transaction unique à partir de plusieurs packages à l’aide d’un « programme de chaînage » pour inclure de manière dynamique des packages dans la transaction. Si un ou plusieurs des packages ne s’installent pas comme prévu, il vous suffit de restaurer l’installation.

le gestionnaire d’interface utilisateur incorporé facilite l’intégration des interfaces utilisateur personnalisées en incorporant un gestionnaire d’interface utilisateur personnalisé dans le package Windows Installer.

Embedded multi package Chaining permet aux développeurs d’activer des événements d’installation sur plusieurs packages. Par exemple, ils peuvent activer des événements d’installation à la demande, réparer des événements et désinstaller des événements sur plusieurs packages.

Les nouvelles fonctionnalités permettent également la création d’installations par utilisateur vraies, notamment la prise en charge des fichiers programme par utilisateur et la fonctionnalité « élever les privilèges », ainsi que la prise en charge de l’inventaire logiciel hors connexion et de la mise en application des correctifs via la gestion et la maintenance des images de déploiement. (voir [nouveautés de Windows Installer 5,0](../msi/what-s-new-in-windows-installer-5-0.md).)

 

 