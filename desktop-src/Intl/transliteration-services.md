---
description: Les services de translittération ELS mappent du texte UTF-16 d’un système d’écriture à un autre système d’écriture.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Services de translittération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc00b96d56e6b05e70b352c81da0280e9ef35043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115619"
---
# <a name="transliteration-services"></a><span data-ttu-id="2b1ba-103">Services de translittération</span><span class="sxs-lookup"><span data-stu-id="2b1ba-103">Transliteration Services</span></span>

<span data-ttu-id="2b1ba-104">Les services de translittération ELS mappent du texte UTF-16 d’un système d’écriture à un autre système d’écriture.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-104">The ELS transliteration services map UTF-16 text from one writing system to another writing system.</span></span> <span data-ttu-id="2b1ba-105">Chaque service est en réalité des données qui s’appliquent à un ensemble spécifique de scripts Unicode d’entrée et de sortie, et la translittération réelle est interne à la plateforme ELS.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-105">Each service is really data applying to a specific set of input and output Unicode scripts, and the actual transliteration is internal to the ELS platform.</span></span> <span data-ttu-id="2b1ba-106">L’application peut éventuellement énumérer les services disponibles pour des scripts d’entrée et de sortie spécifiques et sélectionner le service requis.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-106">The application can optionally enumerate the available services for specific input and output scripts and select the service that it requires.</span></span>

<span data-ttu-id="2b1ba-107">La plateforme gère les métadonnées pour les services de translittération ELS.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-107">The platform maintains metadata for the ELS transliteration services.</span></span> <span data-ttu-id="2b1ba-108">Les métadonnées de chaque service fournissent une description du service et répertorient les scripts d’entrée et de sortie pris en charge par le service.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-108">Metadata for each service provides a description of the service and lists the input and output scripts that the service supports.</span></span> <span data-ttu-id="2b1ba-109">Les métadonnées sont représentées par une structure d' [**\_ \_ informations de service de mappage**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) récupérée par la fonction [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) .</span><span class="sxs-lookup"><span data-stu-id="2b1ba-109">The metadata is represented by a [**MAPPING\_SERVICE\_INFO**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) structure retrieved by the [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) function.</span></span>

## <a name="input-to-a-transliteration-service"></a><span data-ttu-id="2b1ba-110">Entrée d’un service de translittération</span><span class="sxs-lookup"><span data-stu-id="2b1ba-110">Input to a Transliteration Service</span></span>

<span data-ttu-id="2b1ba-111">L’entrée d’un service de translittération est du texte UTF-16 dans un système d’écriture.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-111">The input to a transliteration service is UTF-16 text in one writing system.</span></span>

## <a name="output-of-a-transliteration-service"></a><span data-ttu-id="2b1ba-112">Sortie d’un service de translittération</span><span class="sxs-lookup"><span data-stu-id="2b1ba-112">Output of a Transliteration Service</span></span>

<span data-ttu-id="2b1ba-113">La sortie d’un service de translittération est un texte UTF-16 mappé à un deuxième système d’écriture.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-113">The output of a transliteration service is UTF-16 text mapped to a second writing system.</span></span> <span data-ttu-id="2b1ba-114">Si aucun mappage de translittération approprié n’est disponible pour un segment donné du texte d’entrée, le bloc reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-114">If no appropriate transliteration mapping is available for any given chunk of the input text, the chunk remains unchanged.</span></span>

## <a name="transliteration-service-operation"></a><span data-ttu-id="2b1ba-115">Opération de service de translittération</span><span class="sxs-lookup"><span data-stu-id="2b1ba-115">Transliteration Service Operation</span></span>

<span data-ttu-id="2b1ba-116">Un service de translittération mappe le texte Unicode d’un script d’entrée à un script de sortie, caractère par caractère ou par terme, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-116">A transliteration service maps Unicode text from an input script to an output script, character by character or term by term, as appropriate.</span></span> <span data-ttu-id="2b1ba-117">L’application peut choisir d’obtenir le service de translittération spécifique qui vous intéresse en spécifiant des scripts d’entrée et de sortie lors de l’appel de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), ou en fournissant le GUID du service.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-117">The application can choose to obtain the specific transliteration service of interest by specifying input and output scripts when calling [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), or by providing the service GUID.</span></span> <span data-ttu-id="2b1ba-118">Une autre option pour l’application consiste à énumérer tous les services de translittération disponibles en spécifiant la catégorie de service « translittération » lors de l’appel de **MappingGetServices**.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-118">Another option for the application is to enumerate all available transliteration services by specifying the service category "Transliteration" when calling **MappingGetServices**.</span></span> <span data-ttu-id="2b1ba-119">Dans ce cas, l’application appelle chaque service et compare les résultats avec le texte d’origine pour voir si les résultats ont été modifiés par l’opération d’un service particulier.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-119">In this case, the application calls each service and compares the results with the original text to see if the results have been changed by the operation of a particular service.</span></span>

<span data-ttu-id="2b1ba-120">L’application peut demander la reconnaissance de texte pour un service de translittération ELS à l’aide d’un appel à [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span><span class="sxs-lookup"><span data-stu-id="2b1ba-120">The application can request text recognition for an ELS transliteration service with a call to [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext).</span></span> <span data-ttu-id="2b1ba-121">Lorsqu’il reçoit la demande, le service de translittération alloue une mémoire tampon pour contenir les données de transcription, puis effectue la reconnaissance du texte pour chaque point de code dans la chaîne d’entrée fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-121">When it receives the request, the transliteration service allocates a buffer to contain the transliterated data, and then performs text recognition for each code point in the input string supplied by the application.</span></span>

> [!Note]  
> <span data-ttu-id="2b1ba-122">Le texte d’origine et le texte de transcription peuvent avoir des longueurs différentes.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-122">The original text and the transliterated text might have different lengths.</span></span>

 

## <a name="transliteration-service-guids"></a><span data-ttu-id="2b1ba-123">GUID du service de translittération</span><span class="sxs-lookup"><span data-stu-id="2b1ba-123">Transliteration Service GUIDs</span></span>

<span data-ttu-id="2b1ba-124">Les GUID pour les services de translittération sont déclarés dans Elssrvc. h, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="2b1ba-124">The GUIDs for the transliteration services are declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {A3A8333B-F4FC-42f6-A0C4-0462FE7317CB}
static const GUID ELS_GUID_TRANSLITERATION_HANT_TO_HANS =
    { 0xA3A8333B, 0xF4FC, 0x42f6, { 0xA0, 0xC4, 0x04, 0x62, 0xFE, 0x73, 0x17, 0xCB } };

// {3CACCDC8-5590-42dc-9A7B-B5A6B5B3B63B}
static const GUID ELS_GUID_TRANSLITERATION_HANS_TO_HANT =
    { 0x3CACCDC8, 0x5590, 0x42dc, { 0x9A, 0x7B, 0xB5, 0xA6, 0xB5, 0xB3, 0xB6, 0x3B } };

// {D8B983B1-F8BF-4a2b-BCD5-5B5EA20613E1}
static const GUID ELS_GUID_TRANSLITERATION_MALAYALAM_TO_LATIN =
    { 0xD8B983B1, 0xF8BF, 0x4a2b, { 0xBC, 0xD5, 0x5B, 0x5E, 0xA2, 0x06, 0x13, 0xE1 } };

// {C4A4DCFE-2661-4d02-9835-F48187109803}
static const GUID ELS_GUID_TRANSLITERATION_DEVANAGARI_TO_LATIN =
    { 0xC4A4DCFE, 0x2661, 0x4d02, { 0x98, 0x35, 0xF4, 0x81, 0x87, 0x10, 0x98, 0x03 } };

// {3DD12A98-5AFD-4903-A13F-E17E6C0BFE01}
static const GUID ELS_GUID_TRANSLITERATION_CYRILLIC_TO_LATIN =
    { 0x3DD12A98, 0x5AFD, 0x4903, { 0xA1, 0x3F, 0xE1, 0x7E, 0x6C, 0x0B, 0xFE, 0x01 } };

// {F4DFD825-91A4-489f-855E-9AD9BEE55727}
static const GUID ELS_GUID_TRANSLITERATION_BENGALI_TO_LATIN =
    { 0xF4DFD825, 0x91A4, 0x489f, { 0x85, 0x5E, 0x9A, 0xD9, 0xBE, 0xE5, 0x57, 0x27 } };
```



## <a name="related-topics"></a><span data-ttu-id="2b1ba-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2b1ba-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b1ba-126">À propos des services linguistiques étendus</span><span class="sxs-lookup"><span data-stu-id="2b1ba-126">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



