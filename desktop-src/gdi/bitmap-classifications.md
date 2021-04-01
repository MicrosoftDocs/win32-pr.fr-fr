---
description: Classifications bitmap
ms.assetid: 669ffaef-55c5-4cbc-b23a-de3d66bd6ab2
title: Classifications bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9632b2617eda6fc94ec4836f0e0aa4cc927af113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202058"
---
# <a name="bitmap-classifications"></a><span data-ttu-id="16312-103">Classifications bitmap</span><span class="sxs-lookup"><span data-stu-id="16312-103">Bitmap Classifications</span></span>

<span data-ttu-id="16312-104">Il existe deux classes de bitmaps :</span><span class="sxs-lookup"><span data-stu-id="16312-104">There are two classes of bitmaps:</span></span>

-   <span data-ttu-id="16312-105">[Bitmaps indépendantes du périphérique](device-independent-bitmaps.md) (DIB).</span><span class="sxs-lookup"><span data-stu-id="16312-105">[Device-independent bitmaps](device-independent-bitmaps.md) (DIB).</span></span> <span data-ttu-id="16312-106">Le format de fichier DIB a été conçu pour garantir que les graphiques bitmap créés à l’aide d’une application peuvent être chargés et affichés dans une autre application, conservant ainsi la même apparence que l’original.</span><span class="sxs-lookup"><span data-stu-id="16312-106">The DIB file format was designed to ensure that bitmapped graphics created using one application can be loaded and displayed in another application, retaining the same appearance as the original.</span></span>

-   <span data-ttu-id="16312-107">Les [bitmaps dépendantes](device-dependent-bitmaps.md) de l’appareil (DDB), également appelées bitmaps GDI, étaient les seules bitmaps disponibles dans les versions antérieures de Microsoft Windows 16 bits (antérieures à la version 3,0).</span><span class="sxs-lookup"><span data-stu-id="16312-107">[Device-dependent bitmaps](device-dependent-bitmaps.md) (DDB), also known as GDI bitmaps, were the only bitmaps available in early versions of 16-bit Microsoft Windows (prior to version 3.0).</span></span> <span data-ttu-id="16312-108">Toutefois, à mesure que la technologie d’affichage a été améliorée et que la diversité des périphériques d’affichage disponibles a augmenté, certains problèmes inhérents, qui ne pouvaient être résolus qu’à l’aide de DIB, sont certains problèmes.</span><span class="sxs-lookup"><span data-stu-id="16312-108">However, as display technology improved and as the variety of available display devices increased, certain inherent problems surfaced which could only be solved using DIBs.</span></span> <span data-ttu-id="16312-109">Par exemple, il n’existait aucune méthode de stockage (ou d’extraction) de la résolution du type d’affichage sur lequel une image bitmap a été créée, de sorte qu’une application de dessin n’a pas pu déterminer rapidement si une image bitmap était adaptée au type de périphérique d’affichage vidéo sur lequel l’application s’exécutait.</span><span class="sxs-lookup"><span data-stu-id="16312-109">For example, there was no method of storing (or retrieving) the resolution of the display type on which a bitmap was created, so a drawing application could not quickly determine whether a bitmap was suitable for the type of video display device on which the application was running.</span></span>

    <span data-ttu-id="16312-110">Malgré ces problèmes, DDB (également connu sous le nom de bitmaps compatibles) est toujours utile pour de meilleures performances GDI et dans d’autres situations.</span><span class="sxs-lookup"><span data-stu-id="16312-110">Despite these problems, DDBs (also known as compatible bitmaps) are still useful for better GDI performance and for other situations.</span></span>

 

 



