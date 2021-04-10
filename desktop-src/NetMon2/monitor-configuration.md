---
description: Les analyses peuvent être configurées à l’aide de l’interface utilisateur Moniteur réseau. Les utilisateurs finaux peuvent passer des critères de configuration à votre moniteur à l’aide d’un formulaire HTML stocké en tant que fichier HTM dans le sous-dossier suivant de votre kit de développement logiciel (SDK) Moniteur réseau installé.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Configuration de l’analyse (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b89125450fc71bba21250a66f5c5458317138899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951265"
---
# <a name="monitor-configuration-network-monitor"></a><span data-ttu-id="88653-104">Configuration de l’analyse (Moniteur réseau)</span><span class="sxs-lookup"><span data-stu-id="88653-104">Monitor Configuration (Network Monitor)</span></span>

<span data-ttu-id="88653-105">Les analyses peuvent être configurées à l’aide de l’interface utilisateur Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="88653-105">Monitors can be configured using the Network Monitor UI.</span></span> <span data-ttu-id="88653-106">Les utilisateurs finaux peuvent passer des critères de configuration à votre moniteur à l’aide d’un formulaire HTML stocké en tant que fichier HTM dans le sous-dossier suivant de votre kit de développement logiciel (SDK) Moniteur réseau installé.</span><span class="sxs-lookup"><span data-stu-id="88653-106">End-users can pass configuration criteria to your monitor using an HTML form stored as an HTM file in the following sub folder of your installed Network Monitor SDK.</span></span>

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

<span data-ttu-id="88653-107">Lorsqu’un utilisateur final sélectionne le bouton définir la configuration de l' **analyseur** , le navigateur génère un message HTML de **publication** , qui comprend les noms et les valeurs de tous les éléments de formulaire HTML.</span><span class="sxs-lookup"><span data-stu-id="88653-107">When an end user selects the **Set Monitor Configuration** button, the browser generates an HTML **POST** message, which includes the names and values for all the HTML form elements.</span></span>

<span data-ttu-id="88653-108">Lorsque MCSVC appelle la méthode [Imonitor ::D oconfigure](imonitor-doconfigure.md) , le paramètre *pConfiguration* pointe vers les données du message de publication.</span><span class="sxs-lookup"><span data-stu-id="88653-108">When the MCSVC calls the [IMonitor::DoConfigure](imonitor-doconfigure.md) method, the *pConfiguration* parameter points to the data from the POST message.</span></span> <span data-ttu-id="88653-109">L’exemple de code suivant fournit un exemple de données de message de publication :</span><span class="sxs-lookup"><span data-stu-id="88653-109">The following example code provides an example of POST message data:</span></span>

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Ces données sont transmises sous la forme d’une chaîne ASCII longue. La chaîne semble particulière, à la fois pour sa longueur et pour l’apparence des sections telles que% 3A% 5C et% 0D% 0A. Cette particularité est provoquée par HTML, ce qui nécessite qu’une méthode place toutes les chaînes ANSI, DBCS et Unicode possibles dans un format ASCII. Par exemple, la méthode **configure** insère certains caractères tels que l’esperluette (&) devant chaque nom de variable pour l’identifier en tant que nom de variable. % 3A% 5C est une forme encodée du signe deux-points et% 0D% 0A indique une paire retour chariot/saut de ligne. <span data-ttu-id="88653-115">L’exemple de code suivant fournit le code HTML obtenu tel qu’il est interprété par le moniteur.</span><span class="sxs-lookup"><span data-stu-id="88653-115">The following example code provides the resulting HTML code as interpreted by the monitor.</span></span>

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



