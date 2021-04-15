---
title: Constantes WINBIO_IRIS ( \_ types WINBIO. h)
description: Spécifiez les types de reconnaissance d’IRIS.
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465823"
---
# <a name="winbio_iris-constants"></a>\_Constantes Iris WINBIO

Les constantes suivantes sont des valeurs de **\_ sous- \_ type biométriques WINBIO** qui peuvent être utilisées pour spécifier les types de reconnaissance d’IRIS au-delà de l’INCITS ANSI 379-2004 : « Iris image Interchange Format », qui ne définit aucune valeur d’œil gauche/droite :



| Constante/valeur                                                                                                                                                                                                                                                                   | Description                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **\_ Type d’IRIS WINBIO \_ \_ inconnu**</dt> <dt>0</dt> </dl>                       | Le type d’iris est inconnu. <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **WINBIO \_ Iris \_ gauche \_**</dt> <dt>0xF5</dt> </dl>                               | Le type d’iris est l’œil gauche. <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **WINBIO \_ Iris \_ droit \_**</dt> <dt>0XF6</dt> </dl>                            | Le type d’iris est l’œil droit. <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**WINBIO \_ IRIS \_ non spécifié du \_ PDV \_ 01**</dt> <dt>0xF7</dt> </dl>    | Sous-type associé à un utilisateur s premier modèle lorsqu’un seul œil est le cadre de l’appareil photo et qu’il ne peut pas être déterminé s’il s’agit de l’utilisateur ou de l’œil droit.<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **WINBIO \_ Iris \_ non spécifié \_ pos \_**</dt> <dt>0xf8</dt> </dl> | Sous-type associé à un second modèle utilisateur lorsqu’un seul œil est le cadre de l’appareil photo et qu’il ne peut pas être déterminé s’il s’agit de l’utilisateur ou de l’œil droit.<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **WINBIO \_ Iris \_ des \_ yeux**</dt> <dt>0xf9</dt> </dl>                             | Le type d’iris est à la fois un œil. <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **WINBIO \_ Iris des \_ deux \_ yeux**</dt> <dt>0xFA</dt> </dl>                          | Le type d’iris est l’œil. <br/>                                                                                                                              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



 

 





