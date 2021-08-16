---
description: Indique que Moov sera écrit avant la boîte de MDAT dans le fichier généré.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: Attribut MF_MPEG4SINK_MOOV_BEFORE_MDAT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98614484beee5187364570e3c5517ba0f61e0d77161484b59af93a9f5a6512c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104735"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>MF \_ MPEG4SINK \_ Moov \_ avant \_ attribut MDAT

Indique que « Moov » sera écrit avant la zone « MDAT » dans le fichier généré.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Remarques

Le comportement par défaut du récepteur multimédia MPEG4 consiste à écrire « Moov » après la zone « MDAT ». La définition de cet attribut fait que le fichier généré écrit « Moov » avant la zone « MDAT ».

Pour que le récepteur MPEG4 utilise cet attribut, le flux d’octets transmis ne doit pas être lent ou distant pour.

Cette fonctionnalité implique une copie de fichier supplémentaire/remuxing.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




