---
description: Pour accéder à une application serveur COM+ à distance à partir d’un autre ordinateur (client), l’ordinateur client doit disposer d’un sous-ensemble des attributs de l’application serveur installée, y compris les dll proxy/stub et les bibliothèques de types pour la communication à distance de l’interface DCOM/QC.
ms.assetid: 293b424c-4cd4-43a9-9b56-687c753a34f2
title: Déploiement de proxys d’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5e6439574602005ca53917945fa9005f8959b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950875"
---
# <a name="deploying-application-proxies"></a>Déploiement de proxys d’application

Pour accéder à une application serveur COM+ à distance à partir d’un autre ordinateur (client), l’ordinateur client doit disposer d’un sous-ensemble des attributs de l’application serveur installée, y compris les dll proxy/stub et les bibliothèques de types pour la communication à distance de l’interface DCOM/QC. Ce sous-ensemble est appelé *proxy d’application*.

À l’aide de l’outil d’administration Services de composants, vous pouvez facilement exporter une application serveur COM+ en tant que proxy d’application. Pour que COM+ génère un proxy d’application, il est important que tous les composants de l’application serveur aient été installés et non importés. (Pour plus d’informations sur cette distinction, consultez [importation de composants](importing-components.md).) Cela permet de s’assurer que l’application comprend toutes les informations d’inscription nécessaires.

> [!Note]  
> Il est recommandé de séparer les définitions d’interface des implémentations de classe. Dans le cas contraire, le jeu de dll ou de bibliothèques de types inclus dans le proxy d’application COM+ inclut le code serveur réel.

 

Les proxys d’application générés par COM+ sont des packages d’installation Windows Installer. Après l’installation, les proxys d’application s’affichent dans le panneau de configuration Ajout/suppression de programmes de l’ordinateur client (sauf si le fichier. msi est modifié à l’aide d’un outil de création de Windows Installer).

## <a name="remote-access-via-application-proxies"></a>Accès à distance via des proxys d’application

Lors de la génération d’un proxy d’application, COM+ fournit automatiquement les informations suivantes, nécessaires au proxy d’application pour accéder à distance à une application serveur COM+ :

-   Informations d’identité de classe (CLSID et ProgID). Un proxy d’application prend en charge jusqu’à deux ProgID.
-   Identité de l’application et relation des classes avec les applications (AppID).
-   Informations d’emplacement par application (nom du serveur distant).
-   Informations de marshaling pour toutes les interfaces exposées par l’application (par exemple, les bibliothèques de types et les proxy/stubs).
-   Noms et identificateurs de files d’attente MSMQ (si le service Queued Components est activé pour l’application).
-   Attributs de classe, d’interface et de méthode, à l’exception des informations de rôle.
-   Attributs d’application.

## <a name="installing-application-proxies-on-other-operating-systems"></a>Installation de proxys d’application sur d’autres systèmes d’exploitation

Contrairement aux applications serveur COM+, les proxys d’application peuvent être installés sur n’importe quel système d’exploitation prenant en charge DCOM (et Windows Installer). Sur les ordinateurs qui n’exécutent pas COM+, seul le sous-ensemble d’informations requis pour la communication à distance DCOM est installé. Ces informations sont installées dans le Registre Windows (à l’aide de la \_ racine de classes HKEY \_ , des clés AppID/CLSID).

> [!Note]  
> Lors de l’installation d’un proxy d’application (fichier. msi) sur des ordinateurs qui n’exécutent pas COM+, il est nécessaire d’avoir des Windows Installer en cours d’exécution sur ces ordinateurs. Il est recommandé que les développeurs livrent le Windows Installer fichier redistribuable (instmsi.exe) ainsi que le fichier. msi de l’application. Cela permet de s’assurer que les administrateurs système disposent d’Windows Installer disponibles lors du déploiement de proxys d’application sur des clients qui n’exécutent pas COM+.

 

Sur les ordinateurs exécutant COM+, les informations de proxy d’application sont installées dans le catalogue COM+ et sont visibles dans l’outil d’administration Services de composants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de packages d’installation pour les applications COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Le catalogue COM+](the-com--catalog.md)
</dt> <dt>

[L’utilitaire de réplication COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



