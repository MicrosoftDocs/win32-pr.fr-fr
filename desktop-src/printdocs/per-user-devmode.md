---
description: Un utilisateur peut spécifier les paramètres de document par défaut pour une imprimante. C’est ce que l’on appelle la DEVMODE par utilisateur, car elle affecte uniquement les valeurs par défaut pour un utilisateur particulier, et les informations de chaque imprimante sont définies dans une structure DEVMODE distincte.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: DEVMODE Per-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dee5a79d314e0f9ab89210ba4d2644d2b8ec99c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524212"
---
# <a name="per-user-devmode"></a>DEVMODE Per-User

Un utilisateur peut spécifier les paramètres de document par défaut pour une imprimante. C’est ce que l’on appelle la *DEVMODE par utilisateur* , car elle affecte uniquement les valeurs par défaut pour un utilisateur particulier, et les informations de chaque imprimante sont définies dans une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) distincte.

Pour définir le DEVMODE par utilisateur, appelez [**SetPrinter**](setprinter.md) avec la structure [**\_ info \_ 2**](printer-info-2.md) ou [**Printer \_ info \_ 9**](printer-info-9.md) . Pour réinitialiser le DEVMODE par utilisateur à la valeur [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)par défaut globale, appelez **SetPrinter** avec la structure [**\_ info \_ 8**](printer-info-8.md) de l’imprimante.

 

 



