---
description: Codes FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Codes FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108546"
---
# <a name="fourcc-codes"></a><span data-ttu-id="deb16-103">Codes FOURCC</span><span class="sxs-lookup"><span data-stu-id="deb16-103">FOURCC Codes</span></span>

<span data-ttu-id="deb16-104">De nombreux formats multimédias numériques ont des Codes FOURCC qui leur sont affectés.</span><span class="sxs-lookup"><span data-stu-id="deb16-104">Many digital media formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="deb16-105">Un code FOURCC est un entier non signé 32 bits créé par la concaténation de quatre caractères ASCII.</span><span class="sxs-lookup"><span data-stu-id="deb16-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="deb16-106">Par exemple, le code FOURCC pour la vidéo YUY2 est « YUY2 ».</span><span class="sxs-lookup"><span data-stu-id="deb16-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span> <span data-ttu-id="deb16-107">Pour les formats vidéo compressés et les formats vidéo non RVB (tels que YUV), le membre de la **compression** de la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) doit être défini sur le code FourCC.</span><span class="sxs-lookup"><span data-stu-id="deb16-107">For compressed video formats and non-RGB video formats (such as YUV), the **biCompression** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure should be set to the FOURCC code.</span></span>

<span data-ttu-id="deb16-108">Il existe plusieurs macros C/C++ qui facilitent la déclaration de valeurs FOURCC dans le code source.</span><span class="sxs-lookup"><span data-stu-id="deb16-108">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="deb16-109">Par exemple, la macro **MAKEFOURCC** est déclarée dans Mmsystem. h, et la macro **FCC** est déclarée dans Aviriff. h.</span><span class="sxs-lookup"><span data-stu-id="deb16-109">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="deb16-110">Utilisez-les comme suit :</span><span class="sxs-lookup"><span data-stu-id="deb16-110">Use them as follows:</span></span>


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



<span data-ttu-id="deb16-111">Vous pouvez également déclarer directement un code FOURCC en tant que littéral de chaîne en inversant l’ordre des caractères.</span><span class="sxs-lookup"><span data-stu-id="deb16-111">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="deb16-112">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="deb16-112">For example:</span></span>


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



<span data-ttu-id="deb16-113">L’inversion de l’ordre est nécessaire, car le système d’exploitation Microsoft Windows utilise une architecture Little endian.</span><span class="sxs-lookup"><span data-stu-id="deb16-113">Reversing the order is necessary because the Microsoft Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="deb16-114">'Y' = 0x59, 'U' = 0x55, et' 2 ' = 0x32, donc' 2YUY’est 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="deb16-114">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

### <a name="converting-fourcc-codes-to-subtype-guids"></a><span data-ttu-id="deb16-115">Conversion de codes FOURCC en GUID de sous-type</span><span class="sxs-lookup"><span data-stu-id="deb16-115">Converting FOURCC Codes to Subtype GUIDs</span></span>

<span data-ttu-id="deb16-116">Une plage de 2 \* 32 GUID est réservée à la représentation de FOURCCs.</span><span class="sxs-lookup"><span data-stu-id="deb16-116">A range of 2\*32 GUIDs is reserved for representing FOURCCs.</span></span> <span data-ttu-id="deb16-117">Ces GUID se présentent sous la forme `XXXXXXXX-0000-0010-8000-00AA00389B71` `XXXXXXXX` du code FourCC.</span><span class="sxs-lookup"><span data-stu-id="deb16-117">These GUIDs are all of the form `XXXXXXXX-0000-0010-8000-00AA00389B71` where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="deb16-118">Ainsi, le GUID de sous-type pour YUY2 est `32595559-0000-0010-8000-00AA00389B71` .</span><span class="sxs-lookup"><span data-stu-id="deb16-118">Thus, the subtype GUID for YUY2 is `32595559-0000-0010-8000-00AA00389B71`.</span></span>

<span data-ttu-id="deb16-119">Un grand nombre de ces GUID sont déjà définis dans le fichier d’en-tête UUID. h.</span><span class="sxs-lookup"><span data-stu-id="deb16-119">Many of these GUIDs are defined already in the header file Uuids.h.</span></span> <span data-ttu-id="deb16-120">Par exemple, le sous-type YUY2 est défini en tant que MEDIASUBTYPE \_ YUY2.</span><span class="sxs-lookup"><span data-stu-id="deb16-120">For example, the YUY2 subtype is defined as MEDIASUBTYPE\_YUY2.</span></span> <span data-ttu-id="deb16-121">La bibliothèque de classes de base DirectShow fournit également une classe d’assistance, [**FOURCCMap**](fourccmap.md), qui peut être utilisée pour convertir les codes FourCC en valeurs GUID.</span><span class="sxs-lookup"><span data-stu-id="deb16-121">The DirectShow base class library also provides a helper class, [**FOURCCMap**](fourccmap.md), which can be used to convert FOURCC codes into GUID values.</span></span> <span data-ttu-id="deb16-122">Le constructeur **FOURCCMap** prend un code FourCC comme paramètre d’entrée.</span><span class="sxs-lookup"><span data-stu-id="deb16-122">The **FOURCCMap** constructor takes a FOURCC code as an input parameter.</span></span> <span data-ttu-id="deb16-123">Vous pouvez ensuite effectuer un cast de l’objet **FOURCCMap** vers le GUID correspondant :</span><span class="sxs-lookup"><span data-stu-id="deb16-123">You can then cast the **FOURCCMap** object to the corresponding GUID:</span></span>


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a><span data-ttu-id="deb16-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="deb16-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="deb16-125">**Sous-types audio**</span><span class="sxs-lookup"><span data-stu-id="deb16-125">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="deb16-126">Sous-types de vidéos</span><span class="sxs-lookup"><span data-stu-id="deb16-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> <dt>

[<span data-ttu-id="deb16-127">Utilisation des codecs</span><span class="sxs-lookup"><span data-stu-id="deb16-127">Working with Codecs</span></span>](working-with-codecs.md)
</dt> </dl>

 

 



