---
description: La méthode SetMediaType définit le type de média non compressé pour le groupe.
ms.assetid: 51778563-f119-42e0-826b-966324a85024
title: 'IAMTimelineGroup :: SetMediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8ac32439be94234ee612bce4f3c962839099bb8239a1cfc8b48222129680d01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107819"
---
# <a name="iamtimelinegroupsetmediatype-method"></a>IAMTimelineGroup :: SetMediaType, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `SetMediaType` méthode définit le type de média non compressé pour le groupe.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMediaType(
  [in] AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PMT* \[ dans\]
</dt> <dd>

Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) décrivant le format.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs **HRESULT** suivantes :



| Code de retour                                                                                             | Description                                     |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                             |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Argument de pointeur **null** .<br/>           |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Le type de média spécifié n’est pas valide.<br/> |



 

## <a name="remarks"></a>Remarques

Les types de média suivants sont pris en charge :

-   Vidéo RVB non compressée
-   16 bits par pixel, format 555 (MEDIASUBTYPE \_ RGB555)
-   24 bits par pixel (MEDIASUBTYPE \_ Rgb24)
-   32 bits par pixel, avec alpha (MEDIASUBTYPE \_ ARGB32, et non MEDIASUBTYPE \_ RGB32)
-   audio PCM stéréo 16 bits (MEDIASUBTYPE \_ PCM)

Les types de vidéos doivent utiliser \_ le format videoinfo pour le type de format et [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) pour le bloc de format. Le format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) n’est pas pris en charge. En outre, les formats vidéo descendants (*biheight* < 0) ne sont pas pris en charge.

Pour spécifier un format de compression pour le groupe, appelez la méthode [**IAMTimelineGroup :: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) .

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMTimelineGroup**](iamtimelinegroup.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




