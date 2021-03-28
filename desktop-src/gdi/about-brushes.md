---
description: 'Il existe deux types de pinceaux : logique et physique.'
ms.assetid: 2e15376d-6b4c-41c5-aef8-0dbb91b81505
title: À propos des pinceaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c825892748b317807377bff12675ea04d2d2535
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114250"
---
# <a name="about-brushes"></a><span data-ttu-id="0b26b-103">À propos des pinceaux</span><span class="sxs-lookup"><span data-stu-id="0b26b-103">About Brushes</span></span>

<span data-ttu-id="0b26b-104">Il existe deux types de pinceaux : logique et physique.</span><span class="sxs-lookup"><span data-stu-id="0b26b-104">There are two types of brushes: logical and physical.</span></span> <span data-ttu-id="0b26b-105">Un *pinceau logique* est une description de la bitmap idéale qu’une application utilise pour peindre des formes.</span><span class="sxs-lookup"><span data-stu-id="0b26b-105">A *logical brush* is a description of the ideal bitmap that an application uses to paint shapes.</span></span> <span data-ttu-id="0b26b-106">Un *pinceau physique* est le bitmap réel créé par un pilote de périphérique en fonction de la définition du pinceau logique d’une application.</span><span class="sxs-lookup"><span data-stu-id="0b26b-106">A *physical brush* is the actual bitmap that a device driver creates based on an application's logical-brush definition.</span></span> <span data-ttu-id="0b26b-107">Pour plus d’informations sur les bitmaps, consultez [bitmaps](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="0b26b-107">For more information about bitmaps, see [Bitmaps](bitmaps.md).</span></span>

<span data-ttu-id="0b26b-108">Quand une application appelle l’une des fonctions qui crée un pinceau, elle récupère un handle qui identifie un pinceau logique.</span><span class="sxs-lookup"><span data-stu-id="0b26b-108">When an application calls one of the functions that creates a brush, it retrieves a handle that identifies a logical brush.</span></span> <span data-ttu-id="0b26b-109">Lorsque l’application transmet ce descripteur à la fonction [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) , le pilote de périphérique pour l’affichage ou l’imprimante correspondante crée le pinceau physique.</span><span class="sxs-lookup"><span data-stu-id="0b26b-109">When the application passes this handle to the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function, the device driver for the corresponding display or printer creates the physical brush.</span></span>

<span data-ttu-id="0b26b-110">Les rubriques suivantes décrivent les pinceaux :</span><span class="sxs-lookup"><span data-stu-id="0b26b-110">The following topics describe brushes:</span></span>

-   [<span data-ttu-id="0b26b-111">Origine du pinceau</span><span class="sxs-lookup"><span data-stu-id="0b26b-111">Brush Origin</span></span>](brush-origin.md)
-   [<span data-ttu-id="0b26b-112">Types Brush logiques</span><span class="sxs-lookup"><span data-stu-id="0b26b-112">Logical Brush Types</span></span>](logical-brush-types.md)
-   [<span data-ttu-id="0b26b-113">Transfert de bloc de modèle</span><span class="sxs-lookup"><span data-stu-id="0b26b-113">Pattern Block Transfer</span></span>](pattern-block-transfer.md)
-   [<span data-ttu-id="0b26b-114">Fonctions de brosse compatibles ICM</span><span class="sxs-lookup"><span data-stu-id="0b26b-114">ICM-Enabled Brush Functions</span></span>](icm-enabled-brush-functions.md)

 

 



