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
ms.openlocfilehash: b933df9319c342d8ed3502fc66757df2e6d8fd6e8d60309023ced6ffa042d5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807889"
---
# <a name="software-redistribution"></a>Redistribution de logiciels

l’inclusion de Windows Media Format software dans une installation d’application est appelée redistribution. le kit de développement logiciel (SDK) Windows Media Format inclut un package d’installation qui peut être inclus dans le programme d’installation de votre application. Le package d’installation est un fichier exécutable nommé wmfdist95.exe. lorsque vous installez le kit de développement logiciel (SDK) Windows Media Format, le package d’installation est copié dans le \\ dossier redist du répertoire d’installation (c : \\ wmsdk \\ wmfsdk par défaut).

Les sections suivantes fournissent des procédures et d’autres informations sur la configuration de la redistribution de logiciels.



| Section                                                                            | Description                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pour créer une configuration de redistribution](to-create-a-redistribution-setup.md)           | Décrit la procédure de création d’une configuration d’application.                                                                                                                       |
| [Détection de l’état de l’installation](detecting-setup-status.md)                               | Fournit un exemple de code qui vérifie l’état de l’installation dans le registre pour déterminer si le package de redistribution doit être installé.                                    |
| [Exemple de code pour la configuration de la redistribution](example-code-for-redistribution-setup.md) | Fournit un exemple de code qui peut être utilisé dans votre routine d’installation pour exécuter les packages de redistribution en mode silencieux et notifier votre routine d’installation lorsque l’ordinateur doit être redémarré. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Project Raisons**](project-considerations.md)
</dt> </dl>

 

 




