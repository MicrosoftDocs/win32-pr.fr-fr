---
description: Spécifie les marqueurs dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet marqueur dans l’en-tête ASF, défini dans la spécification ASF.
ms.assetid: 6458eb5f-72a2-4723-b26b-b63516aa2df3
title: Attribut MF_PD_ASF_MARKER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2ae9c5a6cfd79924b95a3b15a7146539d630aad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231798"
---
# <a name="mf_pd_asf_marker-attribute"></a>\_Attribut de \_ \_ marqueur ASF pour MF

Spécifie les marqueurs dans un fichier ASF (Advanced Systems Format). Cet attribut correspond à l’objet marqueur dans l’en-tête ASF, défini dans la spécification ASF.

## <a name="data-type"></a>Type de données

Tableau d’octets

## <a name="remarks"></a>Notes

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF.

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crée le descripteur de présentation et génère cet attribut à partir de l’objet marqueur. Le tableau suivant indique le format de l’objet BLOB :



| Champ d’objet de marqueur | Type de données    | Taille    | Description       |
|---------------------|--------------|---------|-------------------|
| Nombre de marqueurs       | **DWORD**    | 4 octets | Nombre de marqueurs |
| Marqueurs             | **POIDS**\[\] | Variable  | Tableau de marqueurs  |



 

Le premier **DWORD** est le nombre de marqueurs, suivi d’un tableau de marqueurs. Chaque marqueur a le format suivant :



| Champ d’objet de marqueur       | Type de données     | Taille    | Description                                                                       |
|---------------------------|---------------|---------|-----------------------------------------------------------------------------------|
| Longueur de la description du marqueur | **DWORD**     | 4 octets | Taille, en octets, de la chaîne de description, y compris le caractère NULL.           |
| Description du marqueur        | **WCHAR**\[\] | Variable  | Chaîne terminée par le caractère null qui décrit le marqueur.                                 |
| Heure de présentation         | **LONGLONG**  | 8 octets | Heure de présentation du marqueur, en unités de 100 nanosecondes.                         |
| Heure d’envoi                 | **LONGLONG**  | 8 octets | Heure d’envoi de l’entrée du marqueur, en millisecondes.                                   |
| Offset                    | **UINT64**    | 8 octets | Décalage, en octets, de l’objet de données qui spécifie la position du marché. |



 

## <a name="requirements"></a>Spécifications



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

 

 




