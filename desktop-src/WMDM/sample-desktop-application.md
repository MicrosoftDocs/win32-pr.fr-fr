---
title: Exemple d’application de bureau
description: Exemple d’application de bureau
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Gestionnaire de périphériques de média, exemples
- Gestionnaire de périphériques, exemples
- applications de bureau, exemples
- Windows Media Gestionnaire de périphériques, exemple d’application de bureau
- Gestionnaire de périphériques, exemple d’application de bureau
- exemple d’application wmdmapp
- exemples, applications de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414577"
---
# <a name="sample-desktop-application"></a>Exemple d’application de bureau

le Gestionnaire de périphériques Windows Media est livré avec un exemple d’application de bureau appelée wmdmapp. Cette application possède une interface graphique utilisateur qui vous permet de parcourir les appareils connectés, de créer des sélections sur l’appareil et de faire glisser des fichiers multimédias vers l’appareil.

Cet exemple d’application se compose de deux éléments :

-   wmdapp.exe, un fichier exécutable qui affiche une fenêtre et effectue la plupart de l’interface utilisateur et des fonctionnalités de base du programme, et
-   proghelp.dll, DLL d’assistance qui exécute des fonctions utilitaires pour l’application. Vous devez inscrire cette DLL après avoir généré le projet.

Pour compiler l’exemple d’application, vous pouvez utiliser Visual Studio. La section suivante décrit comment procéder :

-   [Compilation de l’exemple d’application à l’aide de Visual Studio](compiling-the-sample-application-using-visual-studio.md)

Après avoir compilé le projet, enregistrez le fichier proghelp.dll. Pour inscrire cette DLL, ouvrez une invite de commandes et accédez au répertoire contenant cette DLL et tapez `regsvr32 proghelp.dll` .

 

 




