---
description: la dernière étape consiste à placer une référence à la Setup.exe sur la page web MySetup MySetup (MySetup.html) décrite dans un exemple d’Installation basé sur une URL Windows Installer.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Établissez une référence HTML à Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091321"
---
# <a name="establish-an-html-reference-to-setupexe"></a>Établissez une référence HTML à Setup.exe

la dernière étape consiste à placer une référence à la Setup.exe sur la page web MySetup MySetup (MySetup.html) décrite dans [un exemple d’Installation basé sur une URL Windows Installer](a-url-based-windows-installer-installation-example.md). Utilisez le script HTML suivant :

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

Cliquer sur le lien « installation MySetup » présente aux utilisateurs l’option d’enregistrer ou d’exécuter à partir de cet emplacement. si l’utilisateur sélectionne exécuter à partir de cet emplacement, le Setup.exe met à niveau la version de Windows Installer sur l’ordinateur, si nécessaire, vérifie la signature numérique du package d’installation et installe le package sur son ordinateur.

Cela termine l’exemple.

 

 



