---
description: Les terminaux enfichables sont classés en superclasses de terminaux.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Entrées de Registre (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035126f614e526f3b1557f5323d52b3bf6b2b12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531425"
---
# <a name="registry-entries-telephony-api"></a>Entrées de Registre (API de téléphonie)

Les terminaux enfichables sont classés en superclasses de terminaux. Chaque superclasse de terminal a une entrée dans le Registre sous la clé suivante :

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Telephony** \\ **TerminalManager**

Sous la clé de superclasse terminal sont des entrées pour chaque terminal enfichable au sein de la superclasse terminal.

L’entrée de chaque superclasse de terminal est identifiée par un CLSID de superclasse terminal. Il s’agit d’un identificateur unique pour une classe de terminal. La classe terminal possède un attribut facultatif : Name, qui est un nom convivial pour la classe terminal. Chaque terminal enfichable est identifié par une classe de terminal CLSID ; autrement dit, un GUID. Les attributs du terminal enfichable sont stockés dans des valeurs de clés de terminal enfichables. Les attributs d’un terminal enfichable sont les suivants.



| Classe de terminal | Nom de clé | Identificateur public                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| Nom           | SZ de REG \_  | Nom convivial du terminal                                                            |
| Company        | SZ de REG \_  | Nom de la société                                                                      |
| Version        | SZ de REG \_  | Informations sur la version                                                               |
| CLSID          | SZ de REG \_  | CLSID de terminal (utilisé dans la méthode [**COCREATEINSTANCE**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com) |
| Directions     | DWORD    | Direction du terminal                                                                |
| MediaTypes     | DWORD    | Types de média terminal pris en charge                                                    |



 

Pour une classe de terminal, les attributs sont les suivants.



| CLSID | Nom de clé | Identificateur public            |
|-------|----------|------------------------------|
| Nom  | SZ de REG \_  | Nom convivial de la classe terminal |



 

 

 
