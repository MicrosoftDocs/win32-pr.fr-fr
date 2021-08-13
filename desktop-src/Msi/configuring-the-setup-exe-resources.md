---
description: un exécutable de démarrage configurable (Setup.exe) et un outil de configuration (Msistuff.exe) sont inclus dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: Configuration des ressources Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c181453f689b7f2c273ba8726097e5d1cd134d1b9675c8ffc42de42d902b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638728"
---
# <a name="configuring-the-setupexe-resources"></a>Configuration des ressources Setup.exe

un exécutable de démarrage configurable (Setup.exe) et un outil de configuration ( [Msistuff.exe](msistuff-exe.md)) sont inclus dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). en utilisant Msistuff.exe pour configurer les ressources dans Setup.exe, les développeurs peuvent facilement créer une installation web d’un package de Windows Installer. Pour plus d’informations, consultez [démarrage du téléchargement Internet](internet-download-bootstrapping.md).

la saisie de la ligne de commande suivante permet de configurer les ressources de l’exemple décrit dans [une URL basée sur un exemple d’Installation Windows Installer](a-url-based-windows-installer-installation-example.md).

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[Continuer](sign-setup-exe-and-mysetup-msi.md)

 

 



