---
description: Cette section décrit les structures que vous pouvez utiliser pour développer des analyseurs. Ces structures sont utilisées par les fonctions que vous pouvez utiliser pour développer des analyseurs et des fonctions que vous pouvez utiliser pour développer des analyseurs ou des experts.
ms.assetid: ce45a8ef-4355-46fd-909e-3ab4d63a3bf1
title: Structures de l’analyseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a9b767974214472f24ea9e1ec9359c97d26fc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119218"
---
# <a name="parser-structures"></a>Structures de l’analyseur

Cette section décrit les structures que vous pouvez utiliser pour développer des analyseurs. Ces structures sont utilisées par les fonctions que vous pouvez utiliser pour développer des analyseurs et des fonctions que vous pouvez utiliser pour développer des analyseurs ou des experts.



| Structure                                 | Description                                                                                                                     |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [MACFRAME](macframe.md)                  | Définit les protocoles initiaux les plus couramment utilisés.                                                                               |
| [ENTRYPOINTS](entrypoints.md)            | Spécifie des pointeurs vers les points d’entrée de la DLL de l’analyseur.                                                                      |
| [\_FOLLOWENTRY PF](pf-followentry.md)     | Spécifie le protocole qui suit le protocole en cours.                                                                       |
| [\_FOLLOWSET PF](pf-followset.md)         | Spécifie l’ensemble des protocoles qui suivent le protocole en cours.                                                               |
| [\_HANDOFFENTRY PF](pf-handoffentry.md)   | Spécifie le protocole qui transmet au protocole en cours ou le protocole que le protocole en cours transmet.    |
| [\_HANDOFFSET PF](pf-handoffset.md)       | Spécifie le jeu de protocoles qui transmet au protocole en cours ou l’ensemble de protocoles vers lequel le protocole en cours est mis. |
| [\_PARSERDLLINFO PF](pf-parserdllinfo.md) | Spécifie le nombre d’analyseurs dans la DLL de l’analyseur et les informations sur chaque analyseur.                                            |
| [\_PARSERINFO PF](pf-parserinfo.md)       | Spécifie les informations relatives à un analyseur spécifique.                                                                                  |
| [\_bit étiqueté](labeled-bit.md)           | Spécifie des handles, des champs de bits ou des indicateurs.                                                                                        |
| [\_octet étiqueté](labeled-byte.md)         | Spécifie une paire d’étiquettes d' **octets** .                                                                                                |
| [\_DWORD étiqueté](labeled-dword.md)       | Spécifie une paire d’étiquettes **DWORD** .                                                                                               |
| [\_mot étiqueté](labeled-word.md)         | Spécifie une paire d’étiquettes **Word** .                                                                                                |
| [PROPERTYINFO](propertyinfo.md)          | Spécifie les propriétés dont l’analyseur de protocole a besoin pour décrire les frames.                                                  |
| [PROPERTYINST](propertyinst.md)          | Spécifie une instance d’une propriété dans un frame.                                                                                 |
| [PROPERTYINSTEX](propertyinstex.md)      | Spécifie une instance de propriété étendue et de forme libre.                                                                              |
| [PROTOCOLINFO](protocolinfo.md)          | Spécifie un protocole.                                                                                                           |
| [VONT](range.md)                        | Spécifie une plage pour un nombre.                                                                                                 |
| [SET](set.md)                            | Spécifie une table de valeurs pour une propriété.                                                                                     |



 

Pour plus d’informations sur les fonctions utilisées pour développer des dll d’analyseur, consultez les rubriques suivantes.



| Pour obtenir des informations sur                                         | Consultez                                                                          |
|---------------------------------------------------------------|------------------------------------------------------------------------------|
| Fonctions exportées par les dll de l’analyseur.                        | [Fonctions d’exportation de DLL de l’analyseur](parser-dll-export-functions.md)               |
| Fonctions que vous pouvez utiliser pour développer des dll d’analyseur.            | [Fonctions de l’analyseur](parser-functions.md)                                     |
| Fonctions que vous pouvez utiliser pour développer des dll de l’analyseur et des experts. | [Fonctions courantes des experts et de l’analyseur](expert-and-parser-common-functions.md) |



 

 

 



