---
description: Spécifie si le récepteur d’accrochage utilise l’horloge de présentation pour planifier des exemples.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: Attribut MF_SAMPLEGRABBERSINK_IGNORE_CLOCK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d757b02a060b4e598ff42d3bd8b9ad7f38af41143c807647aa6f2b8528677cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474422"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>SAMPLEGRABBERSINK MF- \_ \_ attribut ignorer l' \_ horloge

Spécifie si le récepteur d’accrochage utilise l’horloge de présentation pour planifier des exemples.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarques

Vous pouvez définir cet attribut sur l’objet d’activation créé par la fonction [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) . Définissez l’attribut avant d’appeler la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sur l’objet d’activation.

Par défaut, lorsque le récepteur d’accrochage d’échantillon reçoit un exemple, il attend l’heure de présentation de l’exemple pour appeler le rappel de l’application. Si l’attribut de l' \_ horloge SAMPLEGRABBERSINK MF \_ \_ est différent de zéro, le récepteur d’accroche d’échantillon ignore l’horloge de présentation et appelle le rappel dès qu’il reçoit chaque échantillon.

Utilisation recommandée :

-   Si vous souhaitez traiter les exemples aussi rapidement que possible, affectez la **valeur true** à cet attribut.
-   Si vous souhaitez que les appels à la méthode de rappel soient synchronisés avec l’horloge, ne définissez pas cet attribut ou affectez-lui la valeur **false**. Vous pouvez récupérer des échantillons légèrement avant l’horloge, tout en restant synchronisés, en définissant l’attribut de décalage de l' [**\_ heure d' \_ exemple \_ \_ MF SAMPLEGRABBERSINK**](mf-samplegrabbersink-sample-time-offset-attribute.md) .

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




