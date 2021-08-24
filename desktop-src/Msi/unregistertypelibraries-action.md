---
description: L’action UnregisterTypeLibraries annule l’inscription des bibliothèques de types à partir du système. Cette action s’applique à chaque fichier figurant dans la table TypeLib qui est déclenchée pour être désinstallé.
ms.assetid: fea5bdc1-ac27-4d02-bcea-5c97366dd394
title: Action UnregisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6066dbac7e63696f838375261fbb63e8348faf630a7439ec7531cdd71d4ace97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810119"
---
# <a name="unregistertypelibraries-action"></a>Action UnregisterTypeLibraries

L’action UnregisterTypeLibraries annule l’inscription des bibliothèques de types à partir du système. Cette action s’applique à chaque fichier figurant dans la table [TypeLib](typelib-table.md) qui est déclenchée pour être désinstallé.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action UnregisterTypeLibraries doit précéder l’action [RemoveFiles](removefiles-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                        |
|-------|---------------------------------------------------|
| \[1\] | [GUID](guid.md) d’une bibliothèque de types non inscrite. |



 

 

 



