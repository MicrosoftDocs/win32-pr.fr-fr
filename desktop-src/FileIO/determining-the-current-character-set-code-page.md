---
description: La fonction AreFileApisANSI détermine si les fonctions d’e/s de fichier utilisent la page de codes du jeu de caractères ANSI ou OEM.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Détermination de la page de codes du jeu de caractères en cours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18361c0553407ade59c2d1de61ac2fb20d18d5b9d46018bcbc74dc3a114917b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150656"
---
# <a name="determining-the-current-character-set-code-page"></a>Détermination de la page de codes du jeu de caractères en cours

La fonction [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) détermine si les fonctions d’e/s de fichier utilisent la page de codes du jeu de caractères ANSI ou OEM. La fonction [**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) fait en sorte que les fonctions utilisent la page de codes ANSI. La fonction [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) fait en sorte que les fonctions utilisent la page de codes OEM.

Par défaut, les fonctions d’e/s de fichier utilisent des noms de fichiers ANSI. Les fonctions exportées par Kernel32.dll qui acceptent ou retournent des noms de fichiers sont affectées par le paramètre de page de codes du fichier.

[**SetFileApisToANSI**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) et [**SetFileApisToOEM**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) définissent la page de codes par processus, plutôt que par thread ou par ordinateur.

 

 



