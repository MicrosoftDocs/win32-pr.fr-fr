---
description: Un exécutable de démarrage configurable (Setup.exe) et un outil de configuration (Msistuff.exe) sont inclus dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configuration des ressources Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b7907310ff6efcf41e984bf132bbbaedf38b6a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106543019"
---
# <a name="configuring-the-setupexe-resources"></a>Configuration des ressources Setup.exe

Un exécutable de démarrage configurable (Setup.exe) et un outil de configuration ( [Msistuff.exe](msistuff-exe.md)) sont inclus dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). En utilisant Msistuff.exe pour configurer les ressources dans Setup.exe, les développeurs peuvent facilement créer une installation Web d’un package de Windows Installer. Pour plus d’informations, consultez [démarrage du téléchargement Internet](internet-download-bootstrapping.md).

La saisie de la ligne de commande suivante permet de configurer les ressources de l’exemple décrit dans [une URL basée sur un exemple d’Installation Windows Installer](a-url-based-windows-installer-installation-example.md).

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Continuer](sign-setup-exe-and-mysetup-msi.md)

 

 



