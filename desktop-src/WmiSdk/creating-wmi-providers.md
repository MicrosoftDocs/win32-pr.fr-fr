---
description: Les développeurs peuvent étendre l’infrastructure WMI en développant des fournisseurs WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Création de fournisseurs WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042841"
---
# <a name="creating-wmi-providers"></a>Création de fournisseurs WMI

Les développeurs peuvent étendre l’infrastructure WMI en développant des fournisseurs WMI. Les fournisseurs WMI sont des objets COM qui implémentent un ensemble d’interfaces spécifié et, jusqu’à récemment, ont toujours été implémentées en C++. Vous pouvez désormais utiliser des langages managés tels que C# pour implémenter des fournisseurs WMI. La version 3,5 du .NET Framework a introduit l’infrastructure des extensions fournisseur WMI qui rend cela possible. Pour en savoir plus sur la création de fournisseurs WMI à l’aide de ce Framework, consultez l’article [écrire des fournisseurs WMI couplés à l’aide de l’extension de fournisseur WMI.NET 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).

> [!Note]  
> Vous pouvez également créer un fournisseur à l’aide de l’infrastructure de gestion Windows (MI), la version nouvelle génération de WMI. Pour plus d’informations, consultez [comment implémenter un fournisseur mi](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).

 

Le tableau suivant décrit le contenu de cette section.



| Rubrique                                                      | Description                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Fourniture de données à WMI](providing-data-to-wmi.md)         | Fournit une vue d’ensemble des étapes nécessaires à la création d’un fournisseur WMI.         |
| [Développement d’un fournisseur WMI](developing-a-wmi-provider.md) | Décrit les tâches que vous devez effectuer lors de la création de différents types de fournisseurs WMI. |



 

 

 
