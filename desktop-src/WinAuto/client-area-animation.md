---
title: Paramètre d’animation de la zone client
description: L’indicateur d’animation de la zone cliente indique si l’utilisateur souhaite désactiver les animations dans les éléments d’interface utilisateur.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199361"
---
# <a name="client-area-animation-parameter"></a><span data-ttu-id="8b849-103">Paramètre d’animation de la zone client</span><span class="sxs-lookup"><span data-stu-id="8b849-103">Client area animation parameter</span></span>

<span data-ttu-id="8b849-104">Le paramètre d’animation de la zone cliente indique si l’utilisateur souhaite désactiver les animations dans les éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8b849-104">The client area animation parameter indicates whether the user wants to disable animations in UI elements.</span></span> <span data-ttu-id="8b849-105">Les fonctionnalités d’affichage telles que le clignotement, le clignotement, le scintillement et le déplacement de contenu peuvent entraîner des crises chez les utilisateurs avec une épilepsie photosensible.</span><span class="sxs-lookup"><span data-stu-id="8b849-105">Display features such as flashing, blinking, flickering, and moving content can cause seizures in users with photo-sensitive epilepsy.</span></span> <span data-ttu-id="8b849-106">Ce paramètre vous permet d’activer ou de désactiver toutes les animations de ce type.</span><span class="sxs-lookup"><span data-stu-id="8b849-106">This parameter enables you to enable or disable all such animations.</span></span>

<span data-ttu-id="8b849-107">Les applications utilisent les indicateurs **SPI \_ GETCLIENTAREAANIMATION** et **SPI \_ SETCLIENTAREAANIMATION** avec la fonction [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) pour activer ou désactiver les animations de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="8b849-107">Applications use the **SPI\_GETCLIENTAREAANIMATION** and **SPI\_SETCLIENTAREAANIMATION** flags with the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function to turn client area animations on or off.</span></span>

 

 