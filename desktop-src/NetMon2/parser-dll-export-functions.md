---
description: Les fonctions, répertoriées dans le tableau suivant, sont des points d’entrée pour les dll de l’analyseur. Les fonctions sont les points d’entrée pour les appels du système d’exploitation et Moniteur réseau.
ms.assetid: 67811ddb-1961-4306-a62f-b9fd2d2d2b55
title: Fonctions d’exportation de DLL de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929541a1eda60740fe219352fee285a5a34a89df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311917"
---
# <a name="parser-dll-export-functions"></a>Fonctions d’exportation de DLL de l’analyseur

Les fonctions, répertoriées dans le tableau suivant, sont des points d’entrée pour les dll de l’analyseur. Les fonctions sont les points d’entrée pour les appels du système d’exploitation et Moniteur réseau.



| Fonction                                           | Description                                                                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Analyseur DllMain](dllmain-parser.md)               | Indique à la DLL de l’analyseur qu’elle est chargée ou déchargée. Le système d’exploitation appelle la fonction d' **analyse DllMain** lorsqu’un processus charge ou décharge la dll. |
| [AttachProperties](attachproperties.md)           | Indique à l’analyseur d’attacher toutes les propriétés qui existent dans un frame.                                                                                            |
| [Désinscrire](deregister.md)                       | Notifie l’analyseur à nettoyer.                                                                                                                               |
| [FormatProperties](formatproperties.md)           | Indique à l’analyseur de prendre toutes les instances de propriété dans et de générer le membre **szPropertyText** de chaque structure **PROPERTYINST** .                       |
| [RecognizeFrame](recognizeframe.md)               | Détermine si l’analyseur peut interpréter les données de frame non traitées avec le protocole spécifié.                                                            |
| [Inscrire l’analyseur](register-parser.md)             | Détermine les informations de base relatives à l’analyseur dans la DLL. Moniteur réseau appelle la fonction d' **Analyseur de Registre** .                                          |
| [ParserAutoInstallInfo](parserautoinstallinfo.md) | Installe automatiquement un analyseur.                                                                                                                               |



 

Moniteur réseau fournit des structures et des fonctions d’assistance que l’analyseur peut appeler.



| Pour plus d’informations sur l’un des sujets suivants :                          | Consultez                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| Fonctions d’assistance que les experts et les analyseurs peuvent appeler. | [Fonctions courantes des experts et de l’analyseur](expert-and-parser-common-functions.md) |
| Fonctions d’assistance que seuls les analyseurs peuvent appeler.        | [Fonctions de l’analyseur](parser-functions.md)                                     |
| Structures utilisées par les fonctions d’analyseur.               | [Structures de l’analyseur](parser-structures.md)                                   |



 

 

 



