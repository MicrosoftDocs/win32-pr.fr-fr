---
description: Les analyses peuvent être configurées à l’aide de l’interface utilisateur Moniteur réseau. Les utilisateurs finaux peuvent passer des critères de configuration à votre moniteur à l’aide d’un formulaire HTML stocké en tant que fichier HTM dans le sous-dossier suivant de votre kit de développement logiciel (SDK) Moniteur réseau installé.
ms.assetid: 7add5984-5bef-431c-a026-06575514397c
title: Configuration de l’analyse (Moniteur réseau)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b55765774df3be2722c448a1af264162bcd9cdc51ac958cc555bf820d646b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364697"
---
# <a name="monitor-configuration-network-monitor"></a>Configuration de l’analyse (Moniteur réseau)

Les analyses peuvent être configurées à l’aide de l’interface utilisateur Moniteur réseau. Les utilisateurs finaux peuvent passer des critères de configuration à votre moniteur à l’aide d’un formulaire HTML stocké en tant que fichier HTM dans le sous-dossier suivant de votre kit de développement logiciel (SDK) Moniteur réseau installé.

``` syntax
%SystemRoot%\System32\Npp\Monitors
```

Lorsqu’un utilisateur final sélectionne le bouton définir la configuration de l' **analyseur** , le navigateur génère un message HTML de **publication** , qui comprend les noms et les valeurs de tous les éléments de formulaire HTML.

Lorsque MCSVC appelle la méthode [Imonitor ::D oconfigure](imonitor-doconfigure.md) , le paramètre *pConfiguration* pointe vers les données du message de publication. L’exemple de code suivant fournit un exemple de données de message de publication :

``` syntax
ConfigString="FilePath=c%3A%5Ccaptures&StartingNumber=50 \ 
    &EndingNumber=256&MaximumNumberEver=10000 \ 
    &TimeBetweenNotification=120&\
    Addresses=157.54.23.23%0D%0A157.54.23.22% 0D%0A
```

Ces données sont transmises sous la forme d’une chaîne ASCII longue. La chaîne semble particulière, à la fois pour sa longueur et pour l’apparence des sections telles que% 3A% 5C et% 0D% 0A. Cette particularité est provoquée par HTML, ce qui nécessite qu’une méthode place toutes les chaînes ANSI, DBCS et Unicode possibles dans un format ASCII. Par exemple, la méthode **configure** insère certains caractères tels que l’esperluette (&) devant chaque nom de variable pour l’identifier en tant que nom de variable. % 3A% 5C est une forme encodée du signe deux-points et% 0D% 0A indique une paire retour chariot/saut de ligne. L’exemple de code suivant fournit le code HTML obtenu tel qu’il est interprété par le moniteur.

``` syntax
FilePath = c:\captures
StartingNumber=50
EndingNumber = 256
MaximumNumberEver = 10000
TimeBetweenNotification = 120
Addresses= {157.54.23.23, 157.54.23.22}
```

 

 



