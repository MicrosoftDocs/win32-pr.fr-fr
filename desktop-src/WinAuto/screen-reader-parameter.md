---
title: Paramètre de lecteur d’écran
description: Le paramètre de lecteur d’écran indique si une application doit fournir des informations textuelles dans les situations où elle présenterait autrement les informations sous forme graphique.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031512"
---
# <a name="screen-reader-parameter"></a><span data-ttu-id="42e99-103">Paramètre de lecteur d’écran</span><span class="sxs-lookup"><span data-stu-id="42e99-103">Screen reader parameter</span></span>

<span data-ttu-id="42e99-104">Le paramètre de lecteur d’écran indique si une application doit fournir des informations textuelles dans les situations où elle présenterait autrement les informations sous forme graphique.</span><span class="sxs-lookup"><span data-stu-id="42e99-104">The screen reader parameter indicates whether an application should provide textual information in situations where it would otherwise present the information graphically.</span></span>

<span data-ttu-id="42e99-105">Ce paramètre est généralement défini par des aides à l’accessibilité, telles que les lecteurs d’écran.</span><span class="sxs-lookup"><span data-stu-id="42e99-105">This parameter is typically set by accessibility aids such as screen readers.</span></span> <span data-ttu-id="42e99-106">Les applications utilisent les indicateurs **SPI \_ GETSCREENREADER** et **SPI \_ SETSCREENREADER** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour récupérer et définir le paramètre de lecteur d’écran.</span><span class="sxs-lookup"><span data-stu-id="42e99-106">Applications use the **SPI\_GETSCREENREADER** and **SPI\_SETSCREENREADER** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to get and set the screen reader parameter.</span></span>

> [!Note]  
> <span data-ttu-id="42e99-107">Le narrateur, le lecteur d’écran inclus avec Windows, ne définit pas les indicateurs **SPI \_ SETSCREENREADER** ou **SPI \_ GETSCREENREADER** .</span><span class="sxs-lookup"><span data-stu-id="42e99-107">Narrator, the screen reader that is included with Windows, does not set the **SPI\_SETSCREENREADER** or **SPI\_GETSCREENREADER** flags.</span></span>

 

 

 