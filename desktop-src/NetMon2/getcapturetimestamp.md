---
description: La fonction GetCaptureTimeStamp retourne la date et l’heure de début de l’enregistrement des trames par la capture.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: GetCaptureTimeStamp, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119289"
---
# <a name="getcapturetimestamp-function"></a>GetCaptureTimeStamp fonction)

La fonction **GetCaptureTimeStamp** retourne la date et l’heure de début de l’enregistrement des trames par la capture.

## <a name="syntax"></a>Syntaxe


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCapture* \[ dans\]
</dt> <dd>

Handle de la capture. Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes de cette rubrique **GetCaptureTimeStamp** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est un pointeur vers une structure [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

La fonction **GetCaptureTimeStamp** retourne l’heure à laquelle le fournisseur de paquets réseau (NPP) commence à collecter des données, et non lorsque l’expert charge la capture pour l’analyse.

Ne remplacez pas les données dans la structure **SystemTime** . Les données font partie de la capture. Toute tentative de modification des données entraîne une violation d’accès.

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureTimeStamp** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

