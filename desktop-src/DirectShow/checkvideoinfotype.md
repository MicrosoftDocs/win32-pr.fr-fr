---
description: La fonction CheckVideoInfoType vérifie un type de média qui contient une structure de format VIDEOINFOHEADER pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: CheckVideoInfoType, fonction (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540543"
---
# <a name="checkvideoinfotype-function"></a>CheckVideoInfoType fonction)

La `CheckVideoInfoType` fonction vérifie un type de média qui contient une structure de format [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.

> [!Note]  
> Cette fonction ne garantit pas que le type de média est valide ou que le code qui utilise la structure est sécurisé.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) à valider

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                                | Description                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Opération réussie.<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl>                  | Valeur de pointeur **null** .<br/> |
| <dl> <dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt> </dl> | Type de média non valide.<br/>     |



 

## <a name="remarks"></a>Notes

Cette fonction appelle [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) pour valider la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dans le type de média. Si le type de format n’est pas le FORMAT \_ videoinfo, la fonction retourne un \_ type VFW E \_ \_ non \_ accepté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




