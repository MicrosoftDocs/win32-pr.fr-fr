---
description: Les développeurs peuvent étendre l’infrastructure WMI en développant des fournisseurs WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Création de fournisseurs WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cb15b911cb549e28e3536da0a9da31de8df1d6f395ede5f9c9176d21239abc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679739"
---
# <a name="creating-wmi-providers"></a>Création de fournisseurs WMI

Les développeurs peuvent étendre l’infrastructure WMI en développant des fournisseurs WMI. Les fournisseurs WMI sont des objets COM qui implémentent un ensemble d’interfaces spécifié et, jusqu’à récemment, ont toujours été implémentées en C++. Vous pouvez désormais utiliser des langages managés tels que C# pour implémenter des fournisseurs WMI. La version 3,5 du .NET Framework a introduit l’infrastructure des extensions fournisseur WMI qui rend cela possible. Pour en savoir plus sur la création de fournisseurs WMI à l’aide de ce Framework, consultez l’article [écrire des fournisseurs WMI couplés à l’aide de l’extension de fournisseur WMI.NET 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).

> [!Note]  
> vous pouvez également créer un fournisseur à l’aide de l’Infrastructure de gestion de Windows (MI), la prochaine version de WMI. Pour plus d’informations, consultez [comment implémenter un fournisseur mi](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).

 

Le tableau suivant décrit le contenu de cette section.



| Rubrique                                                      | Description                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Fourniture de données à WMI](providing-data-to-wmi.md)         | Fournit une vue d’ensemble des étapes nécessaires à la création d’un fournisseur WMI.         |
| [Développement d’un fournisseur WMI](developing-a-wmi-provider.md) | Décrit les tâches que vous devez effectuer lors de la création de différents types de fournisseurs WMI. |



 

 

 
