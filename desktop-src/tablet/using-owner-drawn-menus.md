---
description: Utilisation de menus owner-drawn pour la prise en charge des fonctionnalités vocales pour Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Utilisation des menus Owner-Drawn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751269"
---
# <a name="using-owner-drawn-menus"></a><span data-ttu-id="1bcdb-103">Utilisation des menus Owner-Drawn</span><span class="sxs-lookup"><span data-stu-id="1bcdb-103">Using Owner-Drawn Menus</span></span>

<span data-ttu-id="1bcdb-104">Lorsque vous utilisez des menus owner-drawn, vous devez rendre les menus accessibles en vue de la prise en charge des fonctionnalités vocales.</span><span class="sxs-lookup"><span data-stu-id="1bcdb-104">When using owner-drawn menus, you must make the menu names available to support speech functionality.</span></span> <span data-ttu-id="1bcdb-105">Il existe deux façons d'effectuer cette opération :</span><span class="sxs-lookup"><span data-stu-id="1bcdb-105">There are two ways to do this:</span></span>

-   <span data-ttu-id="1bcdb-106">Exposez le nom d’élément de menu à l’aide de la structure MSAAMENUINFO.</span><span class="sxs-lookup"><span data-stu-id="1bcdb-106">Expose the menu item name by using the MSAAMENUINFO structure.</span></span>
-   <span data-ttu-id="1bcdb-107">Fournissez une option pour remplacer les menus graphiques par des menus de texte standard lorsqu’une aide à l’accessibilité est active.</span><span class="sxs-lookup"><span data-stu-id="1bcdb-107">Provide an option to replace graphic menus with standard text menus when an accessibility aid is active.</span></span> <span data-ttu-id="1bcdb-108">Si la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) retourne la **valeur true** avec son paramètre *uiaction* défini sur SPI \_ GETSCREENREADER, utilisez les menus standard. L’application doit surveiller le message WM \_ SETTINGSCHANGE et répondre en interrogeant l’état de cette option et en ajustant son affichage de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="1bcdb-108">If the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function returns **TRUE** with its *uiAction* parameter set to SPI\_GETSCREENREADER, use standard menus.The application should watch for the WM\_SETTINGSCHANGE message and respond by querying the state of this option and adjusting its display appropriately.</span></span> <span data-ttu-id="1bcdb-109">Par exemple, Microsoft Visual Studio fournit une option permettant d’utiliser des menus standard à la place des menus personnalisés qui sont affichés par défaut.</span><span class="sxs-lookup"><span data-stu-id="1bcdb-109">For example, Microsoft Visual Studio provides an option to use standard menus instead of the custom menus that are displayed by default.</span></span>

 

 
