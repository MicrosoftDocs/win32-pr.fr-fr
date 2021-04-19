---
description: Windows Update Agent (WUA) se met automatiquement à jour lorsqu’il est connecté à un serveur Windows Server Update Services (WSUS) ou Windows Update.
ms.assetid: 829112ab-b240-4cc4-8053-18b484934886
title: Mise à jour de l’agent de Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00fe439b1bea377e2699f6fe5714b208ac5d951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516491"
---
# <a name="updating-windows-update-agent"></a>Mise à jour de l’agent de Windows Update

Windows Update Agent (WUA) se met à jour par le biais de différents moyens, en fonction de la version de Windows exécutée sur l’appareil. Les anciennes versions de WUA peuvent ne pas être en mesure de se connecter aux services de mise à jour actuels. elles peuvent ne pas être compatibles avec toutes les mises à jour et peuvent ne pas prendre en charge toutes les API documentées. Voici comment s’assurer que WUA est entièrement mis à jour et compatible.

**Sur les versions de Windows à compter de Windows 7 et de Windows Server 2008 R2**

Les mises à jour de l’agent de Windows Update (WUA) sont incluses dans les mises à jour périodiques régulières de Windows distribué par le biais de Windows Update ou Windows Server Update Services (WSUS). Vous n’avez pas besoin de prendre des mesures spéciales pour mettre à jour WUA sur ces versions de Windows.

**Sur les versions de Windows antérieures à Windows 7 et Windows Server 2008 R2**

WUA se met automatiquement à jour quand Mises à jour automatiques se connecte à Windows Update ou à WSUS.

Si Mises à jour automatiques n’a pas encore été exécutée correctement, il est possible qu’un appareil exécutant ces versions de Windows exécute une version antérieure de WUA qui ne prenne pas en charge toutes les API documentées. Si vous recevez un résultat WU_E_SELFUPDATE_REQUIRED lorsque vous utilisez l’API WUA pour effectuer une analyse, un téléchargement ou une installation, cette erreur indique que la version installée de WUA est trop ancienne pour se connecter aux services Windows Update actuels. Vous ne pouvez pas utiliser les API WUA normales pour mettre à jour WUA sur ces systèmes d’exploitation. 

Un utilisateur peut mettre à jour manuellement WUA vers une version actuelle en ouvrant le Windows Update panneau de configuration, en sélectionnant Rechercher les mises à jour, puis en acceptant la mise à jour automatique qui s’affiche. Vous pouvez également mettre à jour WUA par programme.

**Pour mettre à jour par programme WUA sur les versions de Windows antérieures à Windows 7 et Windows Server 2008 R2**

1.  Utilisez les API [WinHTTP](../winhttp/winhttp-start-page.md) pour télécharger [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
2.  Utilisez les [fonctions de chiffrement](../seccrypto/cryptography-functions.md) pour vérifier que la copie téléchargée de [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab) a une signature numérique de Microsoft. Si vous ne pouvez pas vérifier la signature numérique, arrêtez.
3.  Utilisez les API de l' [interface de décompression du fichier](../devnotes/cabinet-api-functions.md) pour extraire le fichier XML de [Wuredist.cab](https://update.microsoft.com/redist/wuredist.cab).
4.  Utilisez les API Microsoft XML Core Services ([MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85))) pour charger le fichier XML et recherchez le nœud WURedist/StandaloneRedist/architecture pour l’architecture de l’ordinateur. Par exemple, pour x86, localisez le nœud WURedist/StandaloneRedist/architecture avec l’attribut **Name** de x86.
5.  Appelez [**IWindowsUpdateAgentInfo :: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) pour déterminer la version actuelle de WUA. Si **IWindowsUpdateAgentInfo :: GetInfo** retourne un numéro de version au moins aussi élevé que l’attribut **clientVersion** dans le nœud architecture que vous avez localisé, arrêtez.
6.  Utilisez les API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) pour lire l’attribut **DownloadURL** à partir du nœud architecture que vous avez localisé. **DownloadURL** vous donne l’URL de téléchargement du programme d’installation WUA approprié pour l’architecture de l’ordinateur.
7.  Utilisez les API [WinHTTP](../winhttp/winhttp-start-page.md) pour télécharger le programme d’installation approprié.
8.  Utilisez la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) ou une API similaire pour exécuter le programme d’installation téléchargé.

 

 
