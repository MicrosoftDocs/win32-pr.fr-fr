---
title: ISRResGraphEx et IAttributes
description: ISRResGraphEx et IAttributes
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f5e08b77b917e4630afcaeb8baed5aac4e13c20a1ed289418681abbbdca20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748995"
---
# <a name="isrresgraphex-and-iattributes"></a>ISRResGraphEx et IAttributes

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Les objets de résultats retournés par le moteur doivent prendre en charge l’interface ISRResGraphEx et l’interface IAttributes. Il suffit de prendre en charge l’interface ISRResGraphEx pour permettre à l’éditeur de sons de fournir des informations sur les césures de mots, mais ne fournit pas la prise en charge nécessaire pour les informations de phonème.

L’éditeur Sound requiert que les moteurs prennent également en charge un attribut DWord spécial, **SRATTR \_ PHONESEG**. L’éditeur interroge les moteurs pour voir l’interface IAttributes et tente de définir **le \_ PHONESEG SRATTR** sur 1. Si cet appel aboutit, l’éditeur de sons suppose que les résultats du moteur prennent en charge la collecte des informations de segmentation de phonème à partir de l’objet de résultats.

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

Lorsqu’un objet de résultats est transmis à l’éditeur Sound, il interroge cet objet pour son implémentation de ISRResGraphEx. ISRResGraphEx contient une fonction membre, DataGet, avec une signature de type

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

Où **dwId** est l’identificateur de l’objet Graph, **GATTRIB** est un GUID correspondant à l’attribut recherché, et **psData** est un pointeur vers un objet SDATA contenant les données retournées. Le moteur est chargé d’allouer les données stockées dans **psData** à [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc). L’application appelante (dans le cas présent, l’éditeur Sound) est chargée de la libérer via [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) quand elle est terminée.

DataGet est requis pour reconnaître trois GUID prédéfinis, qui sont répertoriés dans la documentation SAPI. Un moteur qui retourne un code de réussite à l’appel à **DWORDSet (SRATTR \_ PHONESEG, 1)** est également requis pour reconnaître un GUID spécifique, **SRGARC \_ PHONEMESEGMENTATION**, lorsqu’il est appelé avec un **dwId** qui correspond à un bord dans le graphique.

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

Lorsque l’appel est retourné, **psData** doit pointer vers un tableau de structures alignées sur la valeur DWORD de type **PHONESEG**, défini par :

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

où **qwStartTime** et **qwEndTime** pointent vers le début et la fin de chaque phonème qui compose le mot couvert par l’arête, et **aPhones** est un tableau de caractères Unicode correspondant à la représentation de la Loi sur la loi du téléphone, qui ont été produits dans ce segment. (Dans certains langages, il existe des phonèmes avec plus d’un phonème de la Loi sur la Loi. En anglais, par exemple, le son « long I » dans le mot « Live » est en fait un diphthong, composé de deux phonèmes plus simples concaténés.) Le tableau **aPhones** doit être terminé par zéro et complété à la fin pour que chaque structure **SRPHONESEG** du tableau soit un multiple de 4 octets de long.

Par exemple, supposons que le mot parlé sur l’arc 4 soit « effectué ». Ensuite, l’appel à DataGet (4, **SRGARC \_ PHONEMESEGMENTATION**, &SD) peut retourner un tableau de trois segments de phonème,/m/exécuté à partir de **qwStartTime**= 328434 octets à **qwEndTime**= 330354 octets,/1e/s’exécutant à partir de **qwStartTime**= 330354 octets à **QwEndTime**= 344114 octets, et/d/à partir de **qwStartTime**= 344114 octets vers **qwEndTime**= 347314 octets. Ils sont présentés sous la forme d’un tableau condensé de trois structures **SRPHONESEG** de tailles 28, 32 et 28 octets, respectivement. Notez qu’il existe un remplissage à la fin de la structure **SRPHONESEG** du milieu, afin que l’élément suivant du tableau commence à une limite de 4 octets.

Le kit de développement logiciel (SDK) SAPI 4,0 intègre un outil (SRFunc) pour tester la conformité avec la spécification SAPI 4,0. Un test de compatibilité avec cet ensemble d’interfaces est inclus dans cet outil. Le code source de cet outil est un bon point de départ pour comprendre comment ces interfaces interagissent avec l’éditeur de sons et pour déboguer les interfaces pendant le développement.

 

 