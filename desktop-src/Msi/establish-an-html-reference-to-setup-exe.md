---
description: La dernière étape consiste à placer une référence à la Setup.exe sur la page Web MySetup MySetup (MySetup.html) décrite dans un exemple d’installation basé sur une URL Windows Installer.
ms.assetid: 1a040bd9-242b-4528-858a-2218099acbe3
title: Établissez une référence HTML à Setup.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c16e15f7f25c64467bcd38abf2941f6d99fc12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203207"
---
# <a name="establish-an-html-reference-to-setupexe"></a><span data-ttu-id="860be-103">Établissez une référence HTML à Setup.exe</span><span class="sxs-lookup"><span data-stu-id="860be-103">Establish an HTML Reference to Setup.exe</span></span>

<span data-ttu-id="860be-104">La dernière étape consiste à placer une référence à la Setup.exe sur la page Web MySetup MySetup (MySetup.html) décrite dans [un exemple d’installation basé sur une URL Windows Installer](a-url-based-windows-installer-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="860be-104">The final step is to place a reference to the Setup.exe on the hypothetical MySetup webpage (MySetup.html) described in [A URL Based Windows Installer Installation Example](a-url-based-windows-installer-installation-example.md).</span></span> <span data-ttu-id="860be-105">Utilisez le script HTML suivant :</span><span class="sxs-lookup"><span data-stu-id="860be-105">Use the following HTML script:</span></span>

``` syntax
[MySetup Installation](https://www.blueyonderairlines.com/Products/MySetup/setup.exe)
```

<span data-ttu-id="860be-106">Cliquer sur le lien « installation MySetup » présente aux utilisateurs l’option d’enregistrer ou d’exécuter à partir de cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="860be-106">Clicking on the "MySetup Installation" link presents users with the option to save or run from that location.</span></span> <span data-ttu-id="860be-107">Si l’utilisateur sélectionne exécuter à partir de cet emplacement, le Setup.exe met à niveau la version de Windows Installer sur l’ordinateur, si nécessaire, vérifie la signature numérique du package d’installation et installe le package sur son ordinateur.</span><span class="sxs-lookup"><span data-stu-id="860be-107">If the user selects run from that location, the Setup.exe upgrades the version of Windows Installer on the computer, if necessary, verifies the digital signature on the installer package, and installs the package on their computer.</span></span>

<span data-ttu-id="860be-108">Cela termine l’exemple.</span><span class="sxs-lookup"><span data-stu-id="860be-108">This completes the example.</span></span>

 

 



