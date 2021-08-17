---
description: Déclaration d’informations de filtre
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Déclaration d’informations de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c22fb13b524bed56e8cc9d51e573f2729f843e56565db2793d1a8b4568af52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953198"
---
# <a name="declaring-filter-information"></a>Déclaration d’informations de filtre

La première étape consiste à déclarer les informations de filtre, si nécessaire. DirectShow définit les structures suivantes pour décrire les filtres, les codes confidentiels et les types de média :



| Structure                                               | Description             |
|---------------------------------------------------------|-------------------------|
| [**\_filtre AMOVIESETUP**](amoviesetup-filter.md)       | Décrit un filtre.     |
| [**\_code PIN AMOVIESETUP**](amoviesetup-pin.md)             | Décrit un code confidentiel.        |
| [**\_MediaType AMOVIESETUP**](amoviesetup-mediatype.md) | Décrit un type de média. |



 

Ces structures sont imbriquées. La structure de **\_ filtre AMOVEIESETUP** a un pointeur vers un tableau de structures de **\_ code confidentiel AMOVIESETUP** , et chacune d’entre elles a un pointeur vers un tableau de structures de **\_ MediaType AMOVEIESETUP** . Pris ensemble, ces structures fournissent suffisamment d’informations pour que l’interface [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) localise un filtre. Il ne s’agit pas d’une description complète d’un filtre. Par exemple, si le filtre crée plusieurs instances du même code confidentiel, vous devez déclarer une seule structure [**AMOVIESETUP \_ pin**](amoviesetup-pin.md) pour ce code PIN. En outre, un filtre n’est pas requis pour prendre en charge toutes les combinaisons de types de médias qu’il enregistre. vous n’avez pas non plus besoin d’inscrire chaque type de média qu’il prend en charge.

Déclarez les structures de configuration en tant que variables globales dans votre DLL. L’exemple suivant montre un filtre avec une broche de sortie :


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



Le nom du filtre est déclaré en tant que variable globale statique, car il sera réutilisé ailleurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[comment inscrire des filtres de DirectShow](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



