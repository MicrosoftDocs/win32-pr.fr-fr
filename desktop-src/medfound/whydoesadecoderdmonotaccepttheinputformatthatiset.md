---
description: Pourquoi un décodeur n’accepte-t-il pas le format d’entrée que j’ai défini ?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Pourquoi un décodeur n’accepte-t-il pas le format d’entrée que j’ai défini ?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534183"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a><span data-ttu-id="92faa-103">Pourquoi un décodeur n’accepte-t-il pas le format d’entrée que j’ai défini ?</span><span class="sxs-lookup"><span data-stu-id="92faa-103">Why does a decoder not accept the input format that I set?</span></span>

<span data-ttu-id="92faa-104">Il existe de nombreuses raisons pour lesquelles un décodeur peut rejeter un format.</span><span class="sxs-lookup"><span data-stu-id="92faa-104">There are many reasons why a decoder might reject a format.</span></span> <span data-ttu-id="92faa-105">Les données de format étendu sont manquantes ou incorrectes.</span><span class="sxs-lookup"><span data-stu-id="92faa-105">The most common is missing or incorrect extended format data.</span></span> <span data-ttu-id="92faa-106">Les données de format étendu sont des informations spécifiques au codec qui sont ajoutées à la structure décrivant le type de média.</span><span class="sxs-lookup"><span data-stu-id="92faa-106">The extended format data is codec-specific information that is appended to the structure describing the media type.</span></span>

<span data-ttu-id="92faa-107">Quand vous énumérez un type de sortie à l’aide d’un objet encodeur, le membre **pbFormat** de la structure de  [**\_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) pointera vers une structure WAVEFORMATEX.</span><span class="sxs-lookup"><span data-stu-id="92faa-107">When you enumerate an output type using an encoder object, the **pbFormat** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure will point to a **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="92faa-108">Les données de format étendu sont ajoutées à cette structure et la taille de ces données est stockée dans le membre **WAVEFORMATEX. cbSize** .</span><span class="sxs-lookup"><span data-stu-id="92faa-108">This structure has extended format data appended to it, and the size of that data is stored in the **WAVEFORMATEX.cbSize** member.</span></span> <span data-ttu-id="92faa-109">Quel que soit le conteneur utilisé pour stocker les données compressées, vous devez conserver la structure **WAVEFORMATEX** et l’utiliser dans le type d’entrée pour le décodeur.</span><span class="sxs-lookup"><span data-stu-id="92faa-109">Regardless of the container used to store the compressed data, you must persist the **WAVEFORMATEX** structure and use it in the input type for the decoder.</span></span> <span data-ttu-id="92faa-110">Sans les données de format étendu, le décodeur ne peut pas décompresser le contenu.</span><span class="sxs-lookup"><span data-stu-id="92faa-110">Without the extended format data, the decoder cannot decompress the content.</span></span>

<span data-ttu-id="92faa-111">Pour les formats vidéo, vous devez récupérer manuellement les données de format étendu et les ajouter à la structure **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="92faa-111">For video formats, you must manually retrieve the extended format data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="92faa-112">Pour plus d’informations, consultez [utilisation de données privées de codec vidéo](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="92faa-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="92faa-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92faa-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92faa-114">Questions fréquentes (FAQ)</span><span class="sxs-lookup"><span data-stu-id="92faa-114">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 
