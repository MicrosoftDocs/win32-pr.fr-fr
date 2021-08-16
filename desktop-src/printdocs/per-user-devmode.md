---
description: Un utilisateur peut spécifier les paramètres de document par défaut pour une imprimante. C’est ce que l’on appelle la DEVMODE par utilisateur, car elle affecte uniquement les valeurs par défaut pour un utilisateur particulier, et les informations de chaque imprimante sont définies dans une structure DEVMODE distincte.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: DEVMODE Per-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5e9fd2872d055dba6d04f060e6d2e581e461fd20ddc418f643d09170cda31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731923"
---
# <a name="per-user-devmode"></a>DEVMODE Per-User

Un utilisateur peut spécifier les paramètres de document par défaut pour une imprimante. C’est ce que l’on appelle la *DEVMODE par utilisateur* , car elle affecte uniquement les valeurs par défaut pour un utilisateur particulier, et les informations de chaque imprimante sont définies dans une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) distincte.

Pour définir le DEVMODE par utilisateur, appelez [**SetPrinter**](setprinter.md) avec la structure [**\_ info \_ 2**](printer-info-2.md) ou [**Printer \_ info \_ 9**](printer-info-9.md) . Pour réinitialiser le DEVMODE par utilisateur à la valeur [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)par défaut globale, appelez **SetPrinter** avec la structure [**\_ info \_ 8**](printer-info-8.md) de l’imprimante.

 

 



