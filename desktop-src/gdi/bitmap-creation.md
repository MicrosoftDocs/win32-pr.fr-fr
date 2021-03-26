---
description: Pour créer une image bitmap, utilisez la fonction CreateBitmap, CreateBitmapIndirect ou CreateCompatibleBitmap, CreateDIBitmap et CreateDiscardableBitmap.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Création d’une image bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202057"
---
# <a name="bitmap-creation"></a><span data-ttu-id="04749-103">Création d’une image bitmap</span><span class="sxs-lookup"><span data-stu-id="04749-103">Bitmap Creation</span></span>

<span data-ttu-id="04749-104">Pour créer une image bitmap, utilisez la fonction [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)ou [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)et [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span><span class="sxs-lookup"><span data-stu-id="04749-104">To create a bitmap, use the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap), and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span></span>

<span data-ttu-id="04749-105">Ces fonctions vous permettent de spécifier la largeur et la hauteur, en pixels, de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="04749-105">These functions allow you to specify the width and height, in pixels, of the bitmap.</span></span> <span data-ttu-id="04749-106">La fonction [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) et [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) vous permettent également de spécifier le nombre de plans de couleur et le nombre de bits requis pour identifier la couleur.</span><span class="sxs-lookup"><span data-stu-id="04749-106">The [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) and [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) function also allow you to specify the number of color planes and the number of bits required to identify the color.</span></span> <span data-ttu-id="04749-107">En revanche, les fonctions [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) et [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) utilisent un contexte de périphérique spécifié pour obtenir le nombre de plans de couleur et le nombre de bits requis pour identifier la couleur.</span><span class="sxs-lookup"><span data-stu-id="04749-107">On the other hand, the [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) functions use a specified device context to obtain the number of color planes and the number of bits required to identify the color.</span></span>

<span data-ttu-id="04749-108">La fonction [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) crée une image bitmap dépendante de l’appareil à partir d’une image bitmap indépendante du périphérique.</span><span class="sxs-lookup"><span data-stu-id="04749-108">The [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) function creates a device-dependent bitmap from a device-independent bitmap.</span></span> <span data-ttu-id="04749-109">Il contient une table des couleurs qui décrit comment les valeurs de pixel correspondent aux valeurs de couleur RVB.</span><span class="sxs-lookup"><span data-stu-id="04749-109">It contains a color table that describes how pixel values correspond to RGB color values.</span></span> <span data-ttu-id="04749-110">Pour plus d’informations, consultez [bitmaps dépendantes](device-dependent-bitmaps.md) de l’appareil et [bitmaps indépendantes du périphérique](device-independent-bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="04749-110">For more information, see [Device-Dependent Bitmaps](device-dependent-bitmaps.md) and [Device-Independent Bitmaps](device-independent-bitmaps.md).</span></span>

<span data-ttu-id="04749-111">Une fois la bitmap créée, vous ne pouvez pas modifier sa taille, le nombre de plans de couleurs ou le nombre de bits requis pour identifier la couleur.</span><span class="sxs-lookup"><span data-stu-id="04749-111">After the bitmap has been created, you cannot change its size, number of color planes, or number of bits required to identify the color.</span></span>

<span data-ttu-id="04749-112">Lorsque vous n’avez plus besoin d’une image bitmap, appelez la fonction [**SupprimerObjet**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) pour la supprimer.</span><span class="sxs-lookup"><span data-stu-id="04749-112">When you no longer need a bitmap, call the [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) function to delete it.</span></span>

 

 



