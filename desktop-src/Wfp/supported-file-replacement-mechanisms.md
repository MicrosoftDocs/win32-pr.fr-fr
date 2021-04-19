---
description: Le remplacement des ressources protégées est pris en charge par les mécanismes suivants.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Mécanismes de remplacement des ressources pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545062"
---
# <a name="supported-resource-replacement-mechanisms"></a>Mécanismes de remplacement des ressources pris en charge

Le remplacement des ressources protégées est pris en charge par les mécanismes suivants.

L’autorisation d’accès complet pour modifier les ressources protégées par WRP sur Windows Vista et Windows Server 2008 est limitée à TrustedInstaller avec le service d’installation de modules Windows à l’aide des mécanismes suivants :

-   Service Packs Windows installés par TrustedInstaller.
-   Correctifs installés par TrustedInstaller.
-   Mises à niveau du système d’exploitation installées par TrustedInstaller.
-   Windows Update installé par TrustedInstaller.

Les applications et les programmes d’installation qui tentent de remplacer une ressource protégée par WRP par un autre moyen que les méthodes spécifiées se voient refuser l’accès pour modifier la ressource et générer un message d’erreur d’accès refusé.

Pour les programmes d’installation connus qui tentent de remplacer les ressources protégées par WRP, le message d’erreur et d’erreur Accès refusé peut être supprimé. Dans ce cas, l’opération retourne avec succès, le message d’erreur et d’erreur est supprimé, mais aucune modification n’est appliquée à la ressource protégée par WRP. L’erreur peut être supprimée pour un programme d’installation connu uniquement lorsque tous les critères suivants sont remplis :

-   Il s’agit d’une application héritée. L’application n’inclut pas de manifeste avec un requestedExecutionlevel qui identifie l’application telle qu’elle est conçue pour Windows Vista ou Windows Server 2008.
-   L’erreur Accès refusé est due uniquement à la tentative de modification d’une ressource protégée par WRP.
-   Un administrateur installe l’application.

Pour plus d’informations sur l’utilisation de l’Windows Installer avec WRP, consultez [utilisation de Windows Installer et de protection des ressources Windows](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) dans le kit de développement logiciel (SDK) [Windows Installer](/windows/desktop/Msi/windows-installer-portal) .

**Windows Server 2003 et Windows XP :** Le remplacement des fichiers système protégés par WFP est pris en charge uniquement par le biais des mécanismes suivants :

-   Installation du Service Pack Windows à l’aide de Update.exe
-   Correctifs installés à l’aide de Hotfix.exe
-   Mises à niveau du système d’exploitation à l’aide de Winnt32.exe
-   Windows Update

Le remplacement de fichiers protégés par d’autres moyens que ceux spécifiés entraîne la restauration des fichiers d’origine par WFP.

 

 
