---
title: Constantes WINBIO_ANSI_385_FACE ( \_ types WINBIO. h)
description: Spécifiez les types d’images de face frontale pour la reconnaissance faciale.
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6bc6ba28de799795a049dde3ab98ebdb4c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105412"
---
# <a name="winbio_ansi_385_face-constants"></a>\_ \_ Constantes de visage WINBIO ANSI 385 \_

Les constantes suivantes sont des valeurs de **\_ sous- \_ type biométriques WINBIO** qui peuvent être utilisées pour spécifier les deux types d’images de face frontale, comme défini par ANSI INCITS 385-2004 : « format de reconnaissance faciale pour l’échange de données » : résolution complète et résolution faible. Dans la pratique, l’infrastructure biométrique utilise uniquement des images de résolution complète pour la reconnaissance faciale.



| Constante/valeur                                                                                                                                                                                                                                                                          | Description                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <dt>**WINBIO \_ \_Type de \_ visage ANSI 385 \_ \_ inconnu**</dt> <dt>0</dt> </dl>    | Le type d’image de visage frontal est inconnu.<br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ face \_ frontale \_ Full**</dt> <dt>1</dt> </dl>    | Le type d’image de visage frontal est à résolution complète.<br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <dt>**WINBIO \_ ANSI \_ 385 \_ face \_ frontale \_**</dt> <dt>2</dt> </dl> | Le type d’image de visage frontal est de faible résolution.<br/>  |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



 

 





