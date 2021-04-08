---
title: Redistribution de logiciels
description: Redistribution de logiciels
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Media Format SDK, redistribution de logiciels
- Format de systèmes avancés (ASF), redistribution de logiciels
- ASF (format des systèmes avancés), redistribution de logiciels
- Windows Media Format SDK, redistribution
- Format de systèmes avancés (ASF), redistribution
- ASF (format des systèmes avancés), redistribution
- redistribution de logiciels, à propos de
- redistribution, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672517"
---
# <a name="software-redistribution"></a>Redistribution de logiciels

L’inclusion du logiciel Windows Media format dans une installation d’application est appelée redistribution. Le kit de développement logiciel (SDK) Windows Media Format inclut un package d’installation qui peut être inclus dans le programme d’installation de votre application. Le package d’installation est un fichier exécutable nommé wmfdist95.exe. Lorsque vous installez le kit de développement logiciel (SDK) Windows Media format, le package d’installation est copié dans le \\ dossier Redist du répertoire d’installation (c : \\ WMSDK \\ wmfsdk par défaut).

Les sections suivantes fournissent des procédures et d’autres informations sur la configuration de la redistribution de logiciels.



| Section                                                                            | Description                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pour créer une configuration de redistribution](to-create-a-redistribution-setup.md)           | Décrit la procédure de création d’une configuration d’application.                                                                                                                       |
| [Détection de l’état de l’installation](detecting-setup-status.md)                               | Fournit un exemple de code qui vérifie l’état de l’installation dans le registre pour déterminer si le package de redistribution doit être installé.                                    |
| [Exemple de code pour la configuration de la redistribution](example-code-for-redistribution-setup.md) | Fournit un exemple de code qui peut être utilisé dans votre routine d’installation pour exécuter les packages de redistribution en mode silencieux et notifier votre routine d’installation lorsque l’ordinateur doit être redémarré. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Considérations relatives aux projets**](project-considerations.md)
</dt> </dl>

 

 




