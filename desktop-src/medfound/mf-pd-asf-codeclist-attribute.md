---
description: Contient des informations sur les codecs et les formats utilisés pour encoder le contenu dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de liste de codec dans l’en-tête ASF, défini dans la spécification ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: Attribut MF_PD_ASF_CODECLIST (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528286"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>\_ \_ Attribut CODECLIST MF PD ASF \_

Contient des informations sur les codecs et les formats utilisés pour encoder le contenu dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet de liste de codec dans l’en-tête ASF, défini dans la spécification ASF.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’objet de liste de codecs dans l’en-tête ASF. Une application qui utilise la [source de média ASF](asf-media-source.md) peut obtenir cet attribut en appelant [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , puis en obtenant l’attribut à partir du descripteur de présentation.

Le tableau suivant montre la disposition de l’objet blob d’attributs.



| Champ d’objet de liste de codecs | Type de données    | Taille    | Description                           |
|-------------------------|--------------|---------|---------------------------------------|
| Nombre d’entrées de codec     | **GRANDE**    | 4 octets | Nombre de codecs                      |
| Entrées de codec           | **POIDS**\[\] | Variable  | Tableau de structures d’informations de codec |



 

Le champ entrées de code est un tableau de structures. Le tableau suivant présente le format de chaque entrée :



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Champ d’objet de liste de codecs</th>
<th>Type de données</th>
<th>Taille</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Type</td>
<td><strong>GRANDE</strong></td>
<td>4 octets</td>
<td>Type de codec. Il peut s’agir de l’une des valeurs suivantes :<br/>
<ul>
<li>0x0001 : codec audio</li>
<li>0x0002 : codec vidéo</li>
<li>0xFFFF : inconnu</li>
</ul></td>
</tr>
<tr class="even">
<td>Longueur du nom du codec</td>
<td><strong>GRANDE</strong></td>
<td>4 octets</td>
<td>Taille, en octets, de la chaîne de nom du codec, y compris le caractère <strong>null</strong> .</td>
</tr>
<tr class="odd">
<td>Nom du codec</td>
<td><strong>WCHAR</strong>[]</td>
<td>Variable</td>
<td>Chaîne Unicode terminée par le caractère null qui contient le nom du codec, par exemple &quot; Windows Media Video 9 &quot; .</td>
</tr>
<tr class="even">
<td>Longueur de la description du codec</td>
<td><strong>GRANDE</strong></td>
<td>4 octets</td>
<td>Taille, en octets, de la chaîne de description du codec, y compris le caractère <strong>null</strong> .</td>
</tr>
<tr class="odd">
<td>Description du codec</td>
<td><strong>WCHAR</strong>[]</td>
<td>Variable</td>
<td>Chaîne Unicode terminée par le caractère null qui contient une description du codec.</td>
</tr>
<tr class="even">
<td>Longueur des informations du codec</td>
<td><strong>GRANDE</strong></td>
<td>4 octets</td>
<td>Taille du champ d’informations du codec, en octets.</td>
</tr>
<tr class="odd">
<td>Informations sur le codec</td>
<td><strong>Byte</strong>[]</td>
<td>Variable</td>
<td>Données de codec. La signification de ces données dépend du codec. En règle générale, ces données indiquent le format.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> La disposition de l’objet blob d’attribut ne correspond pas exactement à la disposition de l’objet de liste de codec dans l’en-tête ASF. En particulier, les longueurs de chaîne sont fournies en octets et incluent la taille de la marque de fin **null** .

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
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

 

 




