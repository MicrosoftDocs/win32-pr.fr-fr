---
description: Le décodeur vocal Windows Media Audio décode les flux qui ont été encodés par l’encodeur vocal Windows Media Audio.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Windows Media Audio le décodeur vocal (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532828"
---
# <a name="windows-media-audio-voice-decoder"></a><span data-ttu-id="4133c-103">Décodeur vocal Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="4133c-103">Windows Media Audio Voice Decoder</span></span>

<span data-ttu-id="4133c-104">Le décodeur vocal Windows Media Audio décode les flux qui ont été encodés par l’encodeur [**vocal Windows Media Audio**](windowsmediaaudiovoiceencoder.md).</span><span class="sxs-lookup"><span data-stu-id="4133c-104">The Windows Media Audio Voice decoder decodes streams that were encoded by the [**Windows Media Audio Voice Encoder**](windowsmediaaudiovoiceencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="4133c-105">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="4133c-105">Class Identifier</span></span>

<span data-ttu-id="4133c-106">L’identificateur de classe (CLSID) du décodeur Windows Media Audio Voice est représenté par la constante **CLSID \_ CWMSPDecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="4133c-106">The class identifier (CLSID) for the Windows Media Audio Voice decoder is represented by the constant **CLSID\_CWMSPDecMediaObject**.</span></span> <span data-ttu-id="4133c-107">Vous pouvez créer une instance du décodeur vocal en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="4133c-107">You can create an instance of the voice decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="4133c-108">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="4133c-108">Input Formats</span></span>

<span data-ttu-id="4133c-109">Windows Media Audio contenu encodé en voix est identifié par la balise de format 0x00A.</span><span class="sxs-lookup"><span data-stu-id="4133c-109">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="requirements"></a><span data-ttu-id="4133c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4133c-110">Requirements</span></span>



| <span data-ttu-id="4133c-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4133c-111">Requirement</span></span> | <span data-ttu-id="4133c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="4133c-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4133c-113">Client</span><span class="sxs-lookup"><span data-stu-id="4133c-113">Client</span></span><br/> | <span data-ttu-id="4133c-114">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="4133c-114">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="4133c-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="4133c-115">Header</span></span><br/> | <dl> <span data-ttu-id="4133c-116"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4133c-116"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="4133c-117">DLL</span><span class="sxs-lookup"><span data-stu-id="4133c-117">DLL</span></span><br/>    | <dl> <span data-ttu-id="4133c-118"><dt>Wmspdmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4133c-118"><dt>Wmspdmod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4133c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4133c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4133c-120">Objets codec</span><span class="sxs-lookup"><span data-stu-id="4133c-120">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="4133c-121">Utilisation du codec Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="4133c-121">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="4133c-122">Encodeur vocal Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="4133c-122">Windows Media Audio Voice Encoder</span></span>](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




