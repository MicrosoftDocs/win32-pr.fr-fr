---
title: Configuration de l’environnement
description: Le kit de développement logiciel (SDK) de plateforme installé fournit un fichier Setenv.bat situé dans le répertoire racine du kit de développement logiciel (SDK) de plateforme que vous pouvez exécuter pour configurer votre environnement en vue de créer des applications qui utilisent le kit de développement logiciel (SDK) de plateforme.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509998"
---
# <a name="environment-setup"></a>Configuration de l’environnement

Le kit de développement logiciel (SDK) de plateforme installé fournit un fichier Setenv.bat situé dans le répertoire racine du kit de développement logiciel (SDK) de plateforme que vous pouvez exécuter pour configurer votre environnement en vue de créer des applications qui utilisent le kit de développement logiciel (SDK) de plateforme.

## <a name="settings-and-variables"></a>Paramètres et variables

Vous pouvez également configurer manuellement votre environnement en ajoutant ce qui suit à votre fichier Autoexec.bat. À l’aide de Windows, vous pouvez modifier le fichier Autoexec.bat pour inclure ces commandes. À l’aide de Windows Server 2003, Windows XP, Windows 2000 ou Windows NT, vous pouvez modifier ou ajouter ces paramètres à vos variables d’environnement à l’aide de la boîte de dialogue système que vous pouvez exécuter à partir du panneau de configuration.


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



Ces paramètres conviennent pour une plateforme Intel 80386 ou ultérieure exécutant Windows Me, Windows 98 ou Windows 95 avec Microsoft Visual C++ et le kit de développement logiciel (SDK) de plateforme installé. Par exemple, sur ce système, Visual C++ version 5,0 est installée sous le répertoire C : \\ msdev. Le kit de développement Platform SDK est installé sous le répertoire D : \\ MSSDK La configuration de votre disque peut être différente. Les répertoires du kit de développement Platform SDK (pour cet exemple, ceux avec D : \\ MSSDK dans ceux-ci) sont tous antérieurs dans chaque séquence de chemin d’accès. Cette séquence suppose que les compilations de ligne de commande sont destinées à être exécutées dans la fenêtre d’invite de commandes et que les fichiers de bibliothèque include et. lib dans le kit de développement Platform SDK sont préférés pour ces compilations.

La variable d’environnement UC est définie pour contrôler les builds Win32, en fonction de la plateforme. Les valeurs possibles actuelles sont i386, MIPS, ALPHA et PPC. Pour plus d’informations, consultez le fichier Win32. mak fourni dans le kit de développement logiciel (SDK) de plateforme dans le \\ \\ répertoire include MSSDK. Tous les exemples de fichiers de code du didacticiel COM incluent Win32. mak.

 

 




