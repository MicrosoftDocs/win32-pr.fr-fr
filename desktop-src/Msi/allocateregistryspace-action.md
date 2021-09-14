---
description: L’action AllocateRegistrySpace garantit que la quantité d’espace disponible dans le registre, spécifiée par la propriété AVAILABLEFREEREG, existe dans le registre.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Action AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092729"
---
# <a name="allocateregistryspace-action"></a>Action AllocateRegistrySpace

L’action AllocateRegistrySpace garantit que la quantité d’espace disponible dans le registre, spécifiée par la propriété [**AVAILABLEFREEREG**](availablefreereg.md) , existe dans le registre.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action AllocateRegistrySpace doit être appelée après [InstallInitialize](installinitialize-action.md). Il est recommandé de planifier le AllocateRegistrySpace avant toutes les autres actions pour vous assurer que l’espace disponible dans le Registre est suffisant pour continuer.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action     |
|-------|--------------------------------|
| \[1\] | Espace du registre requis en Ko. |



 

 

 



