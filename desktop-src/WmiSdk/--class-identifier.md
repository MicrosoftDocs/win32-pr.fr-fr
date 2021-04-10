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
# <a name="__class-identifier"></a><span data-ttu-id="7c6f3-103">\_\_Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="7c6f3-103">\_\_CLASS Identifier</span></span>

<span data-ttu-id="7c6f3-104">La classe d’identificateur bien connue \_ \_ fait référence à une pseudo-propriété sur chaque objet WMI qui indique la classe de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="7c6f3-104">The well-known identifier \_\_CLASS refers to a pseudo-property on every WMI object that indicates the class of the current object.</span></span>

<span data-ttu-id="7c6f3-105">Utilisez \_ \_ la classe dans une clause [Where](where-clause.md) pour filtrer les objets des classes dérivées de votre jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="7c6f3-105">Use \_\_CLASS in a [WHERE](where-clause.md) clause to filter out any objects of derived classes from your result set.</span></span> <span data-ttu-id="7c6f3-106">Par exemple, le jeu de résultats de la requête suivante contient non seulement des objets dont la classe est un [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), mais également des objets dont la classe est dérivée du **\_ disque logique Win32**.</span><span class="sxs-lookup"><span data-stu-id="7c6f3-106">For example, the result set of the following query contains not only objects whose class is [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), but also objects whose class is derived from **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk
```



<span data-ttu-id="7c6f3-107">Dans l’exemple suivant, l’utilisation de la \_ \_ classe dans la clause **Where** élimine tous les objets des classes dérivées de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , car leur classe n’est pas un **\_ disque logique Win32**.</span><span class="sxs-lookup"><span data-stu-id="7c6f3-107">In the following example, the use of \_\_CLASS in the **WHERE** clause filters out all objects of classes derived from [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) because their class is not **Win32\_LogicalDisk**.</span></span>


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



<span data-ttu-id="7c6f3-108">Utilisez \_ \_ la classe dans les fournisseurs qui sont invités à fournir des instances d’une classe spécifique, quelle que soit la sous-classe.</span><span class="sxs-lookup"><span data-stu-id="7c6f3-108">Use \_\_CLASS in providers that are asked to provide instances of a specific class, irrespective of any subclasses.</span></span>

 

 
