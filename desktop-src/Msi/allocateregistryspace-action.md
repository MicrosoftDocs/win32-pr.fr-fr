---
description: L’action AllocateRegistrySpace garantit que la quantité d’espace disponible dans le registre, spécifiée par la propriété AVAILABLEFREEREG, existe dans le registre.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Action AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e47a0a0ebc3edec4605cbfac45443e4d30ee25df82ad3eaeb9da9ec9d3a94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639576"
---
# <a name="allocateregistryspace-action"></a>Action AllocateRegistrySpace

L’action AllocateRegistrySpace garantit que la quantité d’espace disponible dans le registre, spécifiée par la propriété [**AVAILABLEFREEREG**](availablefreereg.md) , existe dans le registre.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action AllocateRegistrySpace doit être appelée après [InstallInitialize](installinitialize-action.md). Il est recommandé de planifier le AllocateRegistrySpace avant toutes les autres actions pour vous assurer que l’espace disponible dans le Registre est suffisant pour continuer.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action     |
|-------|--------------------------------|
| \[1\] | Espace du registre requis en Ko. |



 

 

 



