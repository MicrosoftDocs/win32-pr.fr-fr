---
description: Retourne un pointeur vers le commentaire d’une capture.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: GetCaptureComment, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121417"
---
# <a name="getcapturecomment-function"></a>GetCaptureComment fonction)

La fonction **GetCaptureComment** retourne un pointeur vers le commentaire d’une capture.

## <a name="syntax"></a>Syntaxe


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCapture* \[ dans\]
</dt> <dd>

Handle de la capture. Pour plus d’informations sur l’obtention du descripteur de capture, consultez la section Notes.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit (autrement dit, si la capture contient un commentaire), la valeur de retour est un pointeur vers la chaîne de commentaire.

Si la fonction échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

Ne modifiez pas la chaîne de commentaire retournée qui est la chaîne de commentaire réelle qui se trouve dans la capture chargée. Toute modification peut endommager la capture. Toute tentative de modification de la chaîne entraîne une violation d’accès.

Le descripteur de la capture peut être obtenu de plusieurs façons, en fonction de l’appel effectué par un expert ou un analyseur. Pour les experts, le descripteur est spécifié dans le membre **hCapture** de la structure [EXPERTSTARTUPINFO](expertstartupinfo.md) . Pour les analyseurs, le handle de capture peut être obtenu en appelant la fonction [GetFrameCaptureHandle](getframecapturehandle.md) .

Pour récupérer le commentaire d’une capture à partir de son fichier de capture, appelez la fonction [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) .

Les [*experts*](e.md) et les [*analyseurs*](p.md) peuvent appeler la fonction **GetCaptureComment** .

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

[EXPERTSTARTUPINFO](expertstartupinfo.md)
</dt> <dt>

[GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)
</dt> <dt>

[GetFrameCaptureHandle](getframecapturehandle.md)
</dt> </dl>

 

 




