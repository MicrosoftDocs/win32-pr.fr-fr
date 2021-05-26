---
title: Entrée du Registre du Runtime
description: Entrée du Registre du Runtime
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Lecteur Windows Media, entrées de Registre du Runtime
- Windows Media Player, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, entrées du Runtime
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- entrées de Registre du Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf485038965184add320e49c29482672c770f48
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424108"
---
# <a name="runtime-registry-entry"></a>Entrée du Registre du Runtime

Lorsque le lecteur Windows Media rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de Registre qui correspond à l’extension. La sous-clé est décrite dans les paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md). L’une des entrées de Registre qui peuvent apparaître sous la sous-clé de l’extension est l’entrée **Runtime** .

L’entrée **Runtime** spécifie la technologie sous-jacente que le lecteur Windows Media peut utiliser pour lire ou convertir des fichiers multimédias numériques qui ont l’extension personnalisée. L’entrée d' **exécution** se présente sous la forme suivante.



|   Nom   |   Type         |   Valeur                                                       |
|----------|----------------|---------------------------------------------------------------|
| Runtime  | **\_valeur DWORD reg** | Entier positif qui identifie la technologie sous-jacente. |



 

La valeur de l’entrée d' **exécution** doit être l’une des suivantes.



| **Valeur (décimal)** | **Description**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | Rendu à l’aide du kit de développement logiciel (SDK) Windows Media format.                                                 |
| 7                   | Rendu à l’aide de Microsoft DirectShow.                                                         |
| 13                  | Convertit le fichier à l’aide du plug-in de conversion spécifié. Requiert le lecteur Windows Media 11. |



 

Les valeurs 6 et 7 de l’entrée de Registre du **Runtime** sont prises en charge par le lecteur Windows Media série 9 et versions ultérieures. La valeur 13 est prise en charge par le lecteur Windows Media 11.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sous-clé ConvertPluginCLSID**](convertpluginclsid-subkey.md)
</dt> <dt>

[**Paramètres de registre de l’extension de nom de fichier**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




