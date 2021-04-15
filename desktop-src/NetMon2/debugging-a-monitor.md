---
description: La procédure suivante montre comment déboguer une analyse.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Débogage d’une analyse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529019"
---
# <a name="debugging-a-monitor"></a>Débogage d’une analyse

La procédure suivante montre comment déboguer une analyse.

**Pour déboguer une analyse**

1.  Installez la DLL du moniteur et le fichier de base de données du programme (. pdb) généré lorsque vous avez compilé le moniteur à l’emplacement approprié. Pour plus d’informations, consultez [installation d’une analyse pour moniteur réseau](installing-a-monitor-to-network-monitor.md) .
2.  Vérifiez que le service de contrôle de l’analyse est configuré en tant que serveur au lieu d’un service en sélectionnant Panneau de configuration, services.
3.  Ouvrez une invite de commandes et accédez au répertoire Moniteur réseau. Tapez :

    **Mcsvc.exe/RegServer**

    Une fois la session de débogage de l’analyse terminée, vous pouvez rétablir la valeur par défaut de MCSVC en tapant ce qui suit :

    **Mcsvc.exe/service**

4.  Dans Microsoft Visual Studio, lancez Microsoft Visual C++.
5.  Dans l’option de menu **fichier**, **ouvrir** , sélectionnez le nom de votre dll d’analyse.
6.  Après le chargement de Microsoft Visual C++, cliquez sur **projet**, **paramètres**.
7.  Cliquez sur l’onglet **Déboguer** sous **exécutable** pour session de débogage et tapez le chemin d’accès complet de Mcsvc.exe. Par exemple, C : \\ Program Files \\ Netmon2 \\Mcsvc.exe.
8.  Définissez les points d’arrêt dans le code.

> [!Note]  
> N’utilisez pas de boîte de message pour surveiller le débogage. Si le MCSVC s’exécute en tant que service, vous ne verrez pas la fenêtre contextuelle et MCSVC semblera bloqué.

 

 

 



