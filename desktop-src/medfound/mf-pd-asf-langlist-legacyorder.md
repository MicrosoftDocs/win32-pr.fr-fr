---
description: Contient la liste des langages RFC 1766 utilisés dans la présentation actuelle.
ms.assetid: 8853bd88-d51a-478c-8c78-cf69a260e295
title: Attribut MF_PD_ASF_LANGLIST_LEGACYORDER (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32693550ecbe48d14d6e26b9c509f3b90cfd1c327fd945583f1cdff729db7bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102929"
---
# <a name="mf_pd_asf_langlist_legacyorder-attribute"></a>MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER (attribut)

Contient la liste des langages RFC 1766 utilisés dans la présentation actuelle.

## <a name="data-type"></a>Type de données

**POIDS \[\]**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>S’applique à

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux descripteurs de présentation générés à partir de l' [objet ASF ContentInfo](asf-contentinfo-object.md) par un appel à [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Le format du tableau d’octets est le suivant :



| Champ de l’objet de liste de langues | Type de données    | Taille    | Description                            |
|----------------------------|--------------|---------|----------------------------------------|
| Nombre d’enregistrements de l’ID de langue  | **DWORD**    | 4 octets | Nombre de langues                    |
| Enregistrements d’ID de langue        | **POIDS**\[\] | Variable  | Tableau de chaînes de langage (voir ci-dessous). |



 

Le premier **DWORD** est le nombre de langages, suivi d’un tableau de chaînes d’identificateur de langue. Chaque chaîne a le format suivant :



| Champ de l’objet de liste de langues | Type de données     | Taille    | Description                                                                               |
|----------------------------|---------------|---------|-------------------------------------------------------------------------------------------|
| Longueur de l’ID de langue         | **DWORD**     | 4 octets | Longueur de la chaîne en octets, y compris la taille du caractère **null** de fin. |
| ID de langue                | **WCHAR**\[\] | Variable  | Chaîne terminée par le caractère null qui contient le nom du langage RFC 1766.                           |



 

Chaque chaîne est une balise de langue conforme à la norme RFC 1766.

utilisez cet attribut uniquement pour la compatibilité descendante avec l’ordre d’énumération de l’interface [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) dans le kit de développement logiciel (SDK) de Format multimédia Windows. Les chaînes de langue sont stockées dans un ordre différent dans l’attribut [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du descripteur de présentation](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
