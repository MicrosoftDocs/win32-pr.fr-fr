---
description: Spécifie si un encodeur doit être inclus dans la topologie de transcodage.
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: Attribut MF_TRANSCODE_DONOT_INSERT_ENCODER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412960"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a>MF \_ transcodage \_ ne \_ \_ attribut d’encodeur d’insertion

Spécifie si un encodeur doit être inclus dans la topologie de transcodage.

La fonction [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) vérifie cet attribut pendant la génération de la topologie. Si cet attribut n’est pas défini, un encodeur est inséré dans la topologie de transcodage.

## <a name="data-type"></a>Type de données

**UINT32**



| Valeur                                                                        | Signification                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Un encodeur est inséré dans la topologie de transcodage.<br/>                                                      |
| <dl> <dt>1</dt> </dl> | Un encodeur n’est pas inclus dans la topologie de transcodage. Le nœud source est connecté au nœud de sortie.<br/> |



 

## <a name="remarks"></a>Notes

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Spécifications



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

 

 




