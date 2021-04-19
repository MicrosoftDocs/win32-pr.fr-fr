---
description: Indique que Moov sera écrit avant la boîte de MDAT dans le fichier généré.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Attribut MF_MPEG4SINK_MOOV_BEFORE_MDAT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524272"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>MF \_ MPEG4SINK \_ Moov \_ avant \_ attribut MDAT

Indique que « Moov » sera écrit avant la zone « MDAT » dans le fichier généré.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Le comportement par défaut du récepteur multimédia MPEG4 consiste à écrire « Moov » après la zone « MDAT ». La définition de cet attribut fait que le fichier généré écrit « Moov » avant la zone « MDAT ».

Pour que le récepteur MPEG4 utilise cet attribut, le flux d’octets transmis ne doit pas être lent ou distant pour.

Cette fonctionnalité implique une copie de fichier supplémentaire/remuxing.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




