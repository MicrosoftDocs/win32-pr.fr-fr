---
title: Pour créer une configuration de redistribution
description: Pour créer une configuration de redistribution
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Media Format SDK, redistribution de logiciels
- Format de systèmes avancés (ASF), redistribution de logiciels
- ASF (format des systèmes avancés), redistribution de logiciels
- Windows Media Format SDK, redistribution
- Format de systèmes avancés (ASF), redistribution
- ASF (format des systèmes avancés), redistribution
- redistribution de logiciels, création
- redistribution de logiciels, WMFDist.exe
- redistribution, création
- redistribution, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294403"
---
# <a name="to-create-a-redistribution-setup"></a>Pour créer une configuration de redistribution

1.  Faites en sorte que votre routine d’installation installe les fichiers de votre application et effectuez les paramètres requis avant d’appeler le package de redistribution.
2.  Installez WMFDist.exe. Vous pouvez utiliser l’indicateur/Q : A pour effectuer une installation silencieuse et sans assistance et supprimer l’interface utilisateur de la configuration de la redistribution lors de l’installation de votre application. Votre routine doit ensuite déterminer si le redémarrage est nécessaire à la fin.

    Par exemple :

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Redistribution de logiciels**](software-redistribution.md)
</dt> </dl>

 

 




