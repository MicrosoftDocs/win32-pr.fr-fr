---
description: L’action UnregisterTypeLibraries annule l’inscription des bibliothèques de types à partir du système. Cette action s’applique à chaque fichier figurant dans la table TypeLib qui est déclenchée pour être désinstallé.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Action UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399f80d940839c5e94028a9c32e706f4826341a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535636"
---
# <a name="unregistertypelibraries-action"></a>Action UnregisterTypeLibraries

L’action UnregisterTypeLibraries annule l’inscription des bibliothèques de types à partir du système. Cette action s’applique à chaque fichier figurant dans la table [TypeLib](typelib-table.md) qui est déclenchée pour être désinstallé.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action UnregisterTypeLibraries doit précéder l’action [RemoveFiles](removefiles-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) d’une bibliothèque de types non inscrite. |



 

 

 



