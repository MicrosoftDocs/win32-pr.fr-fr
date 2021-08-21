---
description: La fonction CheckVideoInfo2Type vérifie un type de média qui contient une structure de format VIDEOINFOHEADER2 pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.
ms.assetid: 6a71ce7e-c6fc-4811-9182-67949644a0a5
title: CheckVideoInfo2Type, fonction (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfo2Type
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 48d9deab4d87868cbc9e5418ccd6b7e2c7e9ecf93350ad70cb6c934d365e4655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074183"
---
# <a name="checkvideoinfo2type-function"></a>CheckVideoInfo2Type fonction)

La `CheckVideoInfo2Type` fonction vérifie un type de média qui contient une structure de format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) pour certaines erreurs courantes qui peuvent provoquer des dépassements de mémoire tampon ou des débordements d’entiers.

> [!Note]  
> Cette fonction ne garantit pas que le type de média est valide ou que le code qui utilise la structure est sécurisé.

 

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CheckVideoInfo2Type(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*crédit* 
</dt> <dd>

Pointeur vers la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) à valider.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes.



| Code de retour                                                                                                | Description                       |
|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                       | Succès<br/>                |
| <dl> <dt>**\_pointeur E**</dt> </dl>                  | Valeur de pointeur **null**<br/> |
| <dl> <dt>**TYPE de VFW \_ E \_ \_ non \_ accepté**</dt> </dl> | Type de média non valide<br/>     |



 

## <a name="remarks"></a>Remarques

Cette fonction appelle [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) pour valider la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dans le type de média. Si le type de format n’est pas le **format \_ VideoInfo2**, la fonction retourne un **\_ type VFW E \_ \_ non \_ accepté**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Checkbmi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions vidéo et image](video-and-image-functions.md)
</dt> </dl>

 

 




