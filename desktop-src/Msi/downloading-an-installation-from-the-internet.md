---
description: Windows Installer accepte une Uniform Resource Locator (URL) comme source valide pour une installation.
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: Téléchargement d’une installation à partir d’Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527373"
---
# <a name="downloading-an-installation-from-the-internet"></a>Téléchargement d’une installation à partir d’Internet

Windows Installer accepte une Uniform Resource Locator (URL) comme source valide pour une installation. Windows Installer pouvez installer des packages, des correctifs et des transformations à partir d’un emplacement d’URL.

Si la base de données d’installation se trouve sur une URL, le programme d’installation télécharge la base de données dans un emplacement de cache avant de commencer l’installation. Le programme d’installation télécharge également les fichiers et fichiers CAB à partir de la source Internet qui sont appropriés pour les sélections de l’utilisateur. Pour plus d’informations, consultez [un exemple d’installation de Windows Installer basé sur une URL](a-url-based-windows-installer-installation-example.md) .

Par exemple, pour installer un package avec une source située sur un serveur Web à https://server/share/package.msi l’adresse, vous pouvez utiliser les options de [ligne de commande](command-line-options.md) pour installer le package et définir des propriétés [publiques](public-properties.md) .

msiexec/i https://server/share/package.msi *Property = value*

Une ligne de commande semblable à celle présentée précédemment doit être passée au programme d’installation pour démarrer une installation à partir d’un navigateur Web. En général, vous ne devez pas télécharger et installer le package simplement en double-cliquant sur le fichier. msi à partir du navigateur. Cela permet de télécharger le fichier. msi dans le dossier Temporary Internet Files et de transmettre la commande suivante au programme d’installation :

**msiexec/i c : \\ \\ fichiers Internet temporaires Windows \\package.msi**

L’installation échoue si le package nécessite des fichiers sources externes ou des armoires, car ceux-ci ne se trouvent pas au même emplacement que le fichier. msi.

Notez que, étant donné que l’objet [**installer**](installer-object.md) n’est pas marqué comme [SafeForScripting](safeforscripting.md) sur l’ordinateur de l’utilisateur, les utilisateurs doivent ajuster les paramètres de sécurité de leur navigateur pour que l’exemple fonctionne correctement.

La méthode [**InstallProduct**](installer-installproduct.md) peut être utilisée pour exécuter la commande précédente à partir d’un navigateur en tant qu’événement de clic.


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



Notez que, étant donné que certains serveurs Web respectent la casse, le champ de nom de fichier dans la table de [fichiers](file-table.md) doit correspondre exactement à la casse des fichiers sources pour garantir la prise en charge des téléchargements Internet.

Consultez [téléchargement et installation d’un correctif à partir d’Internet](downloading-and-installing-a-patch-from-the-internet.md). Pour plus d’informations sur la sécurisation des installations et l’utilisation des certificats numériques, consultez [instructions pour la création d’installations sécurisées](guidelines-for-authoring-secure-installations.md) et de [signatures numériques et de Windows Installer](digital-signatures-and-windows-installer.md). Pour plus d’informations sur la création d’une installation Web d’un package de Windows Installer, consultez [démarrage du téléchargement sur Internet](internet-download-bootstrapping.md).

## <a name="available-internet-protocols"></a>Protocoles Internet disponibles

À compter de Windows Server 2003 et Windows XP, le programme d’installation peut utiliser les protocoles HTTP, HTTPs et de fichiers. Le programme d’installation ne prend pas en charge les protocoles FTP et GOPHER.

Windows Installer version 2,0 peut utiliser les protocoles HTTP, fichier et FTP et ne peut pas utiliser les protocoles HTTPs et GOPHER.

 

 



