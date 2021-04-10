---
description: La classe d’identificateur bien connue \_ \_ fait référence à une pseudo-propriété sur chaque objet WMI qui indique la classe de l’objet actuel.
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: Identificateur de __CLASS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b4db6cacb6943619cf6468cf7f03d4a4c08278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115659"
---
# <a name="__class-identifier"></a>\_\_Identificateur de classe

La classe d’identificateur bien connue \_ \_ fait référence à une pseudo-propriété sur chaque objet WMI qui indique la classe de l’objet actuel.

Utilisez \_ \_ la classe dans une clause [Where](where-clause.md) pour filtrer les objets des classes dérivées de votre jeu de résultats. Par exemple, le jeu de résultats de la requête suivante contient non seulement des objets dont la classe est un [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), mais également des objets dont la classe est dérivée du **\_ disque logique Win32**.


```sql
SELECT * FROM Win32_LogicalDisk
```



Dans l’exemple suivant, l’utilisation de la \_ \_ classe dans la clause **Where** élimine tous les objets des classes dérivées de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , car leur classe n’est pas un **\_ disque logique Win32**.


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



Utilisez \_ \_ la classe dans les fournisseurs qui sont invités à fournir des instances d’une classe spécifique, quelle que soit la sous-classe.

 

 
