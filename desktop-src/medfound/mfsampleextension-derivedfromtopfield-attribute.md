---
description: Spécifie si une image vidéo désentrelacée a été dérivée du champ supérieur ou du champ inférieur.
ms.assetid: 3710ab94-afb3-44d3-a680-b4a716810ec1
title: Attribut MFSampleExtension_DerivedFromTopField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f90a67edf0b08337748bc118b0aa4ff024ec0ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544787"
---
# <a name="mfsampleextension_derivedfromtopfield-attribute"></a>\_Attribut MFSampleExtension DerivedFromTopField

Spécifie si une image vidéo désentrelacée a été dérivée du champ supérieur ou du champ inférieur. Cet attribut s’applique aux exemples de supports.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Notes

Cet attribut n’est valide que pour les exemples désentrelacés. Définissez cet attribut si le frame a été désentrelacé en interpolant l’un des champs.

Si la valeur est **true**, le champ inférieur a été interpolé à partir du champ supérieur. Si la valeur est **false**, le champ supérieur a été interpolé à partir du champ inférieur.

Si l’attribut n’est pas défini, le frame n’a pas été désentrelacé. Le cadre est soit une vraie image progressive, soit une image entrelacée.

Cet attribut est informatif. Un désentrelaceur logiciel peut définir cet attribut. Si cet attribut est défini, il fournit une indication que vous pouvez récupérer le champ d’origine en supprimant les lignes de numérisation interpolées. Par exemple, si l’attribut a la **valeur true**, vous pouvez récupérer le champ supérieur d’origine en supprimant le champ inférieur interpolé.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Exemples d’attributs](sample-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> <dt>

[Entrelacement de vidéos](video-interlacing.md)
</dt> </dl>

 

 




