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
# <a name="per-user-devmode"></a><span data-ttu-id="3cf65-104">DEVMODE Per-User</span><span class="sxs-lookup"><span data-stu-id="3cf65-104">Per-User DEVMODE</span></span>

<span data-ttu-id="3cf65-105">Un utilisateur peut spécifier les paramètres de document par défaut pour une imprimante.</span><span class="sxs-lookup"><span data-stu-id="3cf65-105">A user can specify the default document settings for a printer.</span></span> <span data-ttu-id="3cf65-106">C’est ce que l’on appelle la *DEVMODE par utilisateur* , car elle affecte uniquement les valeurs par défaut pour un utilisateur particulier, et les informations de chaque imprimante sont définies dans une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) distincte.</span><span class="sxs-lookup"><span data-stu-id="3cf65-106">This is called the *per-user DEVMODE* because it only affects the defaults for a particular user, and the information for each printer is defined in a separate [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>

<span data-ttu-id="3cf65-107">Pour définir le DEVMODE par utilisateur, appelez [**SetPrinter**](setprinter.md) avec la structure [**\_ info \_ 2**](printer-info-2.md) ou [**Printer \_ info \_ 9**](printer-info-9.md) .</span><span class="sxs-lookup"><span data-stu-id="3cf65-107">To set the per-user DEVMODE, call [**SetPrinter**](setprinter.md) with either the [**PRINTER\_INFO\_2**](printer-info-2.md) or the [**PRINTER\_INFO\_9**](printer-info-9.md) structure.</span></span> <span data-ttu-id="3cf65-108">Pour réinitialiser le DEVMODE par utilisateur à la valeur [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)par défaut globale, appelez **SetPrinter** avec la structure [**\_ info \_ 8**](printer-info-8.md) de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="3cf65-108">To reset the per-user DEVMODE to the global default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), call **SetPrinter** with the [**PRINTER\_INFO\_8**](printer-info-8.md) structure.</span></span>

 

 



