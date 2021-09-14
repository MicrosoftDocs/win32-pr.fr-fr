---
description: L’action RegisterTypeLibraries enregistre les bibliothèques de types avec le système. Cette action est appliquée à chaque fichier référencé dans la table TypeLib qui est planifiée pour l’installation.
ms.assetid: 374450bb-316c-4fe6-abb1-cd8a8a31f284
title: Action RegisterTypeLibraries
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469cc18fc2842a3258804fc012c48a49085f1598
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009685"
---
# <a name="registertypelibraries-action"></a>Action RegisterTypeLibraries

L’action RegisterTypeLibraries enregistre les bibliothèques de types avec le système. Cette action est appliquée à chaque fichier référencé dans la [table Typelib](typelib-table.md) qui est planifiée pour l’installation.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action RegisterTypeLibraries doit venir après l’action [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                   |
|-------|----------------------------------------------|
| \[1\] | [GUID](guid.md) de la bibliothèque de types inscrite. |



 

## <a name="remarks"></a>Remarques

L’action RegisterTypeLibraries nécessite que le langage de la bibliothèque de types soit correctement créé dans le champ Language de la table TypeLib. Une création incorrecte du champ Language peut provoquer l’échec de l’inscription d’une bibliothèque de types valide dans le programme d’installation.

 

 



