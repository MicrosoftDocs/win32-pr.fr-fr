---
title: Fichier d' Module-Definition du lecteur d’installation
description: Fichier d' Module-Definition du lecteur d’installation
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- pilotes installables, fichiers de définition de module
- pilotes installables, fichiers DEF
- pilotes nstallable, fonction DriverProc
- DriverProc fonction)
- fichiers de définition de module
- fichiers DEF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369039"
---
# <a name="installable-drive-module-definition-file"></a>Fichier d' Module-Definition du lecteur d’installation

La définition de module (. DEF) d’un pilote installable nomme le pilote, exporte la fonction [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) et définit une description du pilote. L’exemple suivant montre un fichier de définition de module standard pour un pilote installable :


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



Certaines applications d’installation peuvent ouvrir le pilote et récupérer la ligne de description à utiliser lors de l’installation du pilote. Pour rester compatible avec ces applications d’installation, la ligne de description doit avoir la forme suivante :

*Alias* \[ de description,*alias* \] ... **:**_texte_  

L' *alias* spécifie un nom unique pour le pilote que les applications peuvent utiliser pour ouvrir le pilote. L’alias sert également de nom de valeur associé au pilote dans le registre. Les alias multiples sont séparés par des virgules. Le *texte* décrit l’objectif du pilote.

 

 