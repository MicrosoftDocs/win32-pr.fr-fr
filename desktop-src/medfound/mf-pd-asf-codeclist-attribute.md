---
description: Contient des informations sur les codecs et les formats utilisés pour encoder le contenu dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de liste de codec dans l’en-tête ASF, défini dans la spécification ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: Attribut MF_PD_ASF_CODECLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c512dee499dbd2d006fb695c89d59add449e64fb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471305"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>\_ \_ Attribut CODECLIST MF PD ASF \_

Contient des informations sur les codecs et les formats utilisés pour encoder le contenu dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de liste de codec dans l’en-tête ASF, défini dans la spécification ASF.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’objet de liste de codecs dans l’en-tête ASF. Une application qui utilise la [source de média ASF](asf-media-source.md) peut obtenir cet attribut en appelant [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , puis en obtenant l’attribut à partir du descripteur de présentation.

Le tableau suivant montre la disposition de l’objet blob d’attributs.



| Champ d’objet de liste de codecs | Type de données    | Taille    | Description                           |
|-------------------------|--------------|---------|---------------------------------------|
| Nombre d’entrées de codec     | **DWORD**    | 4 octets | Nombre de codecs                      |
| Entrées de codec           | **POIDS**\[\] | Variable  | Tableau de structures d’informations de codec |



 

Le champ entrées de code est un tableau de structures. Le tableau suivant présente le format de chaque entrée :




| Champ d’objet de liste de codecs | Type de données | Taille | Description | 
|-------------------------|-----------|------|-------------|
| Type | <strong>DWORD</strong> | 4 octets | Type de codec. Il peut s’agir de l’une des valeurs suivantes :<br /><ul><li>0x0001 : codec audio</li><li>0x0002 : codec vidéo</li><li>0xFFFF : inconnu</li></ul> | 
| Longueur du nom du codec | <strong>DWORD</strong> | 4 octets | Taille, en octets, de la chaîne de nom du codec, y compris le caractère <strong>null</strong> . | 
| Nom du codec | <strong>WCHAR</strong>[] | Variable | chaîne Unicode terminée par le caractère Null qui contient le nom du codec, par exemple « Windows Media Video 9 ». | 
| Longueur de la description du codec | <strong>DWORD</strong> | 4 octets | Taille, en octets, de la chaîne de description du codec, y compris le caractère <strong>null</strong> . | 
| Description du codec | <strong>WCHAR</strong>[] | Variable | Chaîne Unicode terminée par le caractère null qui contient une description du codec. | 
| Longueur des informations du codec | <strong>DWORD</strong> | 4 octets | Taille du champ d’informations du codec, en octets. | 
| Informations sur le codec | <strong>Byte</strong>[] | Variable | Données de codec. La signification de ces données dépend du codec. En règle générale, ces données indiquent le format. | 




 

> [!Note]  
> La disposition de l’objet blob d’attribut ne correspond pas exactement à la disposition de l’objet de liste de codec dans l’en-tête ASF. En particulier, les longueurs de chaîne sont fournies en octets et incluent la taille de la marque de fin **null** .

 

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

 

 




