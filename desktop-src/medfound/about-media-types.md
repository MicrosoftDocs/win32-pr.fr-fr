---
description: En savoir plus sur les types de média dans Microsoft Media Foundation. Un type de média décrit le format d’un flux multimédia.
ms.assetid: 169cdb00-0c1a-4530-90b7-bc89c71d1d04
title: À propos des types de média (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3abce5d86b931a472dc07e1b6daf244f1456cfd3220f85c2b0e311f243a122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975078"
---
# <a name="about-media-types-microsoft-media-foundation"></a>À propos des types de média (Microsoft Media Foundation)

Un *type de média* décrit le format d’un flux multimédia. Dans Microsoft Media Foundation, les types de média sont représentés par l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Cette interface hérite de l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Les détails d’un type de média sont spécifiés en tant qu’attributs.

Pour créer un type de média, appelez la fonction [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) . Cette fonction retourne un pointeur vers l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Initialement, le type de média n’a pas d’attribut. Pour définir les détails du format, définissez les attributs appropriés.

Pour obtenir la liste des attributs de type de média, consultez [attributs de type de média](media-type-attributes.md).

## <a name="major-types-and-subtypes"></a>Types et sous-types principaux

Deux informations importantes relatives à un type de support sont le type principal et le sous-type.

-   Le *type principal* est un GUID qui définit la catégorie globale des données dans un flux de données multimédia. Les types principaux incluent la vidéo et l’audio. Pour spécifier le type principal, définissez l’attribut de [ \_ \_ \_ type principal MF MT](mf-mt-major-type-attribute.md) . La méthode [**IMFMediaType :: GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) retourne la valeur de cet attribut.
-   Le *sous-type* définit davantage le format. Par exemple, dans le type principal vidéo, il existe des sous-types pour RGB-24, RGB-32, YUY2, et ainsi de suite. Dans l’audio, il y a des données audio PCM, des données audio à virgule flottante IEEE et d’autres. Le sous-type fournit plus d’informations que le type principal, mais il ne définit pas tout ce qui concerne le format. Par exemple, les sous-types vidéo ne définissent pas la taille de l’image ni la fréquence d’images. Pour spécifier le sous-type, définissez l’attribut de [ \_ sous- \_ type MF MT](mf-mt-subtype-attribute.md) .

Tous les types de média doivent avoir un GUID de type principal et un GUID de sous-type. Pour obtenir la liste des principaux GUID de type et de sous-type, consultez [GUID type Media](media-type-guids.md).

## <a name="why-attributes"></a>Pourquoi des attributs ?

les attributs présentent plusieurs avantages par rapport aux structures de format qui ont été utilisés dans les technologies précédentes telles que DirectShow et le kit de développement logiciel (SDK) Windows Media format.

-   Il est plus facile de représenter les valeurs « ne sais pas » ou « ne pas se soucier ». Par exemple, si vous écrivez une transformation vidéo, vous savez peut-être à l’avance quels sont les formats RVB et YUV que la transformation prend en charge, mais pas les dimensions de la trame vidéo, jusqu’à ce que vous les obteniez de la source vidéo. De même, vous risquez de ne pas vous soucier de certains détails, tels que les vidéos primaires. Avec une structure de format, chaque membre doit être rempli avec une *certaine* valeur. Par conséquent, il est devenu courant d’utiliser zéro pour indiquer une valeur inconnue ou par défaut. Cette pratique peut provoquer des erreurs si un autre composant traite zéro comme une valeur légitime. Avec les attributs, il vous suffit d’omettre les attributs qui sont inconnus ou non pertinents pour votre composant.

-   À mesure que les spécifications ont évolué au fil du temps, les structures de format ont été étendues en ajoutant des données supplémentaires à la fin de la structure. Par exemple, **WAVEFORMATEXTENSIBLE** étend la structure **WAVEFORMATEX** . Cette pratique est sujette à une erreur, car les composants doivent convertir les pointeurs de structure en d’autres types de structure. Les attributs peuvent être étendus en toute sécurité.
-   Des structures de format mutuellement incompatibles ont été définies. par exemple, DirectShow définit les structures **VIDEOINFOHEADER** et **VIDEOINFOHEADER2** . Les attributs étant définis indépendamment l’un de l’autre, ce problème ne se pose pas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 



