---
title: Entrée du Registre du Runtime
description: Entrée du Registre du Runtime
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Lecteur Windows Media, entrées de registre du runtime
- Lecteur Windows Media, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, entrées du Runtime
- registre, paramètres pour Lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- entrées de Registre du Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677cb5edb397089a7c432e2464a4d38d6cf5f4c4948070bbef1b1b9cb5c5bebf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933679"
---
# <a name="runtime-registry-entry"></a>Entrée du Registre du Runtime

lorsque Lecteur Windows Media rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de registre qui correspond à l’extension. la sous-clé est décrite dans la [Paramètres du registre](file-name-extension-registry-settings.md)de l’Extension de nom de fichier. L’une des entrées de Registre qui peuvent apparaître sous la sous-clé de l’extension est l’entrée **Runtime** .

l’entrée **Runtime** spécifie la technologie sous-jacente que Lecteur Windows Media pouvez utiliser pour lire ou convertir des fichiers multimédias numériques qui ont l’extension personnalisée. L’entrée d' **exécution** se présente sous la forme suivante.



|   Name   |   Type         |   Valeur                                                       |
|----------|----------------|---------------------------------------------------------------|
| Runtime  | **\_valeur DWORD reg** | Entier positif qui identifie la technologie sous-jacente. |



 

La valeur de l’entrée d' **exécution** doit être l’une des suivantes.



| **Valeur (décimal)** | **Description**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | rendu à l’aide du kit de développement logiciel (SDK) Windows Media Format.                                                 |
| 7                   | Effectuer un rendu à l’aide de Microsoft DirectShow.                                                         |
| 13                  | Convertit le fichier à l’aide du plug-in de conversion spécifié. requiert Lecteur Windows Media 11. |



 

les valeurs 6 et 7 de l’entrée de registre du **Runtime** sont prises en charge par Lecteur Windows Media série 9 et versions ultérieures. la valeur 13 est prise en charge par Lecteur Windows Media 11.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sous-clé ConvertPluginCLSID**](convertpluginclsid-subkey.md)
</dt> <dt>

[**Paramètres de registre de l’Extension de nom de fichier**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




