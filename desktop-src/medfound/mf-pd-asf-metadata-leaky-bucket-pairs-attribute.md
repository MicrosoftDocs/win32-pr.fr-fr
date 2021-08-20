---
description: Spécifie une liste de vitesses de transmission et les fenêtres de mémoire tampon correspondantes pour un fichier ASF (variable bit rate).
ms.assetid: e45d055f-d404-47e9-b3c8-ac743b290138
title: Attribut MF_PD_ASF_METADATA_LEAKY_BUCKET_PAIRS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9444292ad437551622e1f418a6f21198ecd8341f01e4e5bda0a2047f847cfd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740747"
---
# <a name="mf_pd_asf_metadata_leaky_bucket_pairs-attribute"></a>\_Attribut des \_ \_ paires de \_ \_ compartiments avec fuite de métadonnées ASF PD \_

Spécifie une liste de vitesses de transmission et les fenêtres de mémoire tampon correspondantes pour un fichier ASF (variable bit rate).

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut qui s’applique au descripteur de présentation pour le contenu ASF.

La valeur de l’attribut a le format suivant :

``` syntax
struct {
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

La structure de la **\_ \_ \_ paire de compartiments de fuites WM** est définie comme suit :

``` syntax
typedef struct _WMLeakyBucketPair {
  DWORD  dwBitrate;
  DWORD  msBufferWindow;
} WM_LEAKY_BUCKET_PAIR;
```

Pour chaque vitesse de transmission, le membre **msBufferWindow** indique la quantité de contenu mis en mémoire tampon avant le début de la lecture, en millisecondes. La taille de la mémoire tampon en octets est égale à **msBufferWinow** x **dwBitrate** /8000.

> [!Note]  
> cet attribut correspond à l’attribut **ASFLeakyBucketPairs** dans le kit de développement logiciel (SDK) de Format multimédia Windows.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> <dt>

[Descripteurs de présentation](presentation-descriptors.md)
</dt> </dl>

 

 




