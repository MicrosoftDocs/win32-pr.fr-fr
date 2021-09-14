---
description: Les services de translittération ELS mappent du texte UTF-16 d’un système d’écriture à un autre système d’écriture.
ms.assetid: 32e46c52-5c3c-4e22-8f4e-05286ee213ba
title: Services de translittération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc00b96d56e6b05e70b352c81da0280e9ef35043
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121809"
---
# <a name="transliteration-services"></a>Services de translittération

Les services de translittération ELS mappent du texte UTF-16 d’un système d’écriture à un autre système d’écriture. Chaque service est en réalité des données qui s’appliquent à un ensemble spécifique de scripts Unicode d’entrée et de sortie, et la translittération réelle est interne à la plateforme ELS. L’application peut éventuellement énumérer les services disponibles pour des scripts d’entrée et de sortie spécifiques et sélectionner le service requis.

La plateforme gère les métadonnées pour les services de translittération ELS. Les métadonnées de chaque service fournissent une description du service et répertorient les scripts d’entrée et de sortie pris en charge par le service. Les métadonnées sont représentées par une structure d' [**\_ \_ informations de service de mappage**](/windows/desktop/api/Elscore/ns-elscore-mapping_service_info) récupérée par la fonction [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices) .

## <a name="input-to-a-transliteration-service"></a>Entrée d’un service de translittération

L’entrée d’un service de translittération est du texte UTF-16 dans un système d’écriture.

## <a name="output-of-a-transliteration-service"></a>Sortie d’un service de translittération

La sortie d’un service de translittération est un texte UTF-16 mappé à un deuxième système d’écriture. Si aucun mappage de translittération approprié n’est disponible pour un segment donné du texte d’entrée, le bloc reste inchangé.

## <a name="transliteration-service-operation"></a>Opération de service de translittération

Un service de translittération mappe le texte Unicode d’un script d’entrée à un script de sortie, caractère par caractère ou par terme, le cas échéant. L’application peut choisir d’obtenir le service de translittération spécifique qui vous intéresse en spécifiant des scripts d’entrée et de sortie lors de l’appel de [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices), ou en fournissant le GUID du service. Une autre option pour l’application consiste à énumérer tous les services de translittération disponibles en spécifiant la catégorie de service « translittération » lors de l’appel de **MappingGetServices**. Dans ce cas, l’application appelle chaque service et compare les résultats avec le texte d’origine pour voir si les résultats ont été modifiés par l’opération d’un service particulier.

L’application peut demander la reconnaissance de texte pour un service de translittération ELS à l’aide d’un appel à [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext). Lorsqu’il reçoit la demande, le service de translittération alloue une mémoire tampon pour contenir les données de transcription, puis effectue la reconnaissance du texte pour chaque point de code dans la chaîne d’entrée fournie par l’application.

> [!Note]  
> Le texte d’origine et le texte de transcription peuvent avoir des longueurs différentes.

 

## <a name="transliteration-service-guids"></a>GUID du service de translittération

Les GUID pour les services de translittération sont déclarés dans Elssrvc. h, comme indiqué dans le code suivant.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des services linguistiques étendus](about-extended-linguistic-services.md)
</dt> </dl>

 

 



