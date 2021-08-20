---
description: Les terminaux enfichables sont classés en superclasses de terminaux.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Entrées de Registre (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd6e4e4d91b65e3ef886fd4d2d44b571f4ac4696697aef8b8d8b2715e273e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761166"
---
# <a name="registry-entries-telephony-api"></a>Entrées de Registre (API de téléphonie)

Les terminaux enfichables sont classés en superclasses de terminaux. Chaque superclasse de terminal a une entrée dans le Registre sous la clé suivante :

**HKEY \_ logiciel de l' \_ ordinateur LOCAL** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **telephony** \\ **TerminalManager**

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



 

 

 
