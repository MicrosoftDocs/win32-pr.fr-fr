---
description: Spécifie si un fichier ASF (Advanced Systems Format) est diffusé ou recherché. Cette valeur correspond au champ Flags de l’objet de propriétés de fichier, défini dans la spécification ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: Attribut MF_PD_ASF_FILEPROPERTIES_FLAGS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313902"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a>MF \_ PD \_ ASF \_ - \_ attribut flags

Spécifie si un fichier ASF (Advanced Systems Format) est diffusé ou recherché. Cette valeur correspond au champ Flags de l’objet de propriétés de fichier, défini dans la spécification ASF.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Cet attribut s’applique aux descripteurs de présentation pour le contenu ASF. La valeur de l’attribut est une opération or au niveau du bit des indicateurs suivants :



| Indicateur | Description                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x01 | Indicateur de diffusion. Le fichier est en cours de création.                                                                                                                                                                                                                                      |
| 0x02 | Indicateur de recherche. Le fichier peut être recherché.<br/> Un fichier peut être recherché si un flux audio est présent et que la taille maximale des paquets de données est égale à la taille minimale des paquets de données. Il peut également être recherché si le fichier a un flux audio et un flux vidéo avec un objet index simple correspondant.<br/> |



 

La méthode [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) génère cet attribut à partir des métadonnées ASF.

Si l’indicateur de diffusion est défini, les attributs suivants dans le descripteur de présentation ne sont pas valides :

-   [**ID du fichier. MF \_ PD \_ ASF \_ FichierPropriétés \_ \_**](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [**heure de création de MF \_ PD \_ ASF \_ FichierPropriétés \_ \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [**\_paquets MF PD \_ ASF FM \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)
-   [**\_durée de \_ \_ \_ lecture \_ MF PD ASF**](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [**durée d’envoi de la norme MF \_ PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)

En outre, les valeurs d’attribut taille de paquet [**\_ maximale MF PD \_ ASF \_ FichierPropriétés \_ Max \_ \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) et [**MF \_ PD \_ ASF \_ FichierPropriétés \_ Min \_ Packet \_ Size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) sont définies sur la taille de paquet réelle.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> <dt>

[Objet d’en-tête ASF](asf-file-structure.md)
</dt> <dt>

[Descripteurs de présentation](presentation-descriptors.md)
</dt> </dl>

 

 




