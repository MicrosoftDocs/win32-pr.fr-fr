---
description: le WiToAnsi.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. Cet exemple montre comment le script est utilisé pour réécrire un fichier texte Unicode sous la forme d’un fichier texte ANSI.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Copier un fichier Unicode dans un fichier ANSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091946"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>Copier un fichier Unicode dans un fichier ANSI

le WiToAnsi.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Cet exemple montre comment le script est utilisé pour réécrire un fichier texte Unicode sous la forme d’un fichier texte ANSI.

l’utilisation de cet exemple nécessite la version CScript.exe ou WScript.exe de Windows Script Host. Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante. L’aide s’affiche si le premier argument est/ ? ou si le nombre d’arguments spécifié est insuffisant. Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ *chemin d’accès au fichier* \] . L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.

**cscript WiToAnsi.vbs \[ chemin d’accès du fichier Unicode \] \[ au fichier ANSI\]**

Spécifiez le fichier texte Unicode en cours de conversion. Spécifiez le fichier texte ANSI en cours de création. Si aucun fichier ANSI n’est spécifié, le fichier Unicode est remplacé.

pour obtenir des exemples supplémentaires de scripts, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md). pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows hôte de Script, consultez [Windows Installer outils de développement](windows-installer-development-tools.md).

 

 



