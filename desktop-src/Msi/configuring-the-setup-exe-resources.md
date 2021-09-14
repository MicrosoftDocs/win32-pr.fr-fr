---
description: un exécutable de démarrage configurable (Setup.exe) et un outil de configuration (Msistuff.exe) sont inclus dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configuration des ressources Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b7907310ff6efcf41e984bf132bbbaedf38b6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091989"
---
# <a name="configuring-the-setupexe-resources"></a>Configuration des ressources Setup.exe

un exécutable de démarrage configurable (Setup.exe) et un outil de configuration ( [Msistuff.exe](msistuff-exe.md)) sont inclus dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). en utilisant Msistuff.exe pour configurer les ressources dans Setup.exe, les développeurs peuvent facilement créer une installation web d’un package de Windows Installer. Pour plus d’informations, consultez [démarrage du téléchargement Internet](internet-download-bootstrapping.md).

la saisie de la ligne de commande suivante permet de configurer les ressources de l’exemple décrit dans [une URL basée sur un exemple d’Installation Windows Installer](a-url-based-windows-installer-installation-example.md).

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Continuer](sign-setup-exe-and-mysetup-msi.md)

 

 



