---
description: 'Les méthodes image :: Save et image :: SaveAdd méthodes de la classe image reçoivent un objet EncoderParameters qui contient un tableau d’objets EncoderParameter.'
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Constantes d’encodeur d’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8130b90ad7f1d559ca480a581a0b157ff152fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202436"
---
# <a name="image-encoder-constants"></a><span data-ttu-id="c2c88-103">Constantes d’encodeur d’image</span><span class="sxs-lookup"><span data-stu-id="c2c88-103">Image Encoder Constants</span></span>

<span data-ttu-id="c2c88-104">Les méthodes [image :: Save](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) et [image :: SaveAdd](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) méthodes de la classe [**image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) reçoivent un objet [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) qui contient un tableau d’objets [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="c2c88-104">The [Image::Save Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) and [Image::SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class receive an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that contains an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="c2c88-105">Chaque objet **EncoderParameter** a un membre de données GUID qui spécifie la catégorie de paramètre.</span><span class="sxs-lookup"><span data-stu-id="c2c88-105">Each **EncoderParameter** object has a GUID data member that specifies the parameter category.</span></span> <span data-ttu-id="c2c88-106">Les constantes suivantes, définies dans Gdiplusimaging. h, représentent des GUID qui spécifient les différentes catégories de paramètres.</span><span class="sxs-lookup"><span data-stu-id="c2c88-106">The following constants, defined in Gdiplusimaging.h, represent GUIDs that specify the various parameter categories.</span></span>

-   <span data-ttu-id="c2c88-107">EncoderChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="c2c88-107">EncoderChrominanceTable</span></span>
-   <span data-ttu-id="c2c88-108">EncoderColorDepth</span><span class="sxs-lookup"><span data-stu-id="c2c88-108">EncoderColorDepth</span></span>
-   <span data-ttu-id="c2c88-109">EncoderColorSpace</span><span class="sxs-lookup"><span data-stu-id="c2c88-109">EncoderColorSpace</span></span>
-   <span data-ttu-id="c2c88-110">EncoderCompression</span><span class="sxs-lookup"><span data-stu-id="c2c88-110">EncoderCompression</span></span>
-   <span data-ttu-id="c2c88-111">EncoderLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="c2c88-111">EncoderLuminanceTable</span></span>
-   <span data-ttu-id="c2c88-112">EncoderQuality</span><span class="sxs-lookup"><span data-stu-id="c2c88-112">EncoderQuality</span></span>
-   <span data-ttu-id="c2c88-113">EncoderRenderMethod</span><span class="sxs-lookup"><span data-stu-id="c2c88-113">EncoderRenderMethod</span></span>
-   <span data-ttu-id="c2c88-114">EncoderSaveFlag</span><span class="sxs-lookup"><span data-stu-id="c2c88-114">EncoderSaveFlag</span></span>
-   <span data-ttu-id="c2c88-115">EncoderScanMethod</span><span class="sxs-lookup"><span data-stu-id="c2c88-115">EncoderScanMethod</span></span>
-   <span data-ttu-id="c2c88-116">EncoderTransformation</span><span class="sxs-lookup"><span data-stu-id="c2c88-116">EncoderTransformation</span></span>
-   <span data-ttu-id="c2c88-117">EncoderVersion</span><span class="sxs-lookup"><span data-stu-id="c2c88-117">EncoderVersion</span></span>
-   <span data-ttu-id="c2c88-118">EncoderImageItems</span><span class="sxs-lookup"><span data-stu-id="c2c88-118">EncoderImageItems</span></span>
-   <span data-ttu-id="c2c88-119">EncoderSaveAsCMYK</span><span class="sxs-lookup"><span data-stu-id="c2c88-119">EncoderSaveAsCMYK</span></span>

 

 
