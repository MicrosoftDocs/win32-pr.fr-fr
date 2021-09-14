---
description: La méthode GetBitmapBits récupère une image vidéo à l’heure du média spécifiée. Le frame retourné est toujours au format RGB 24 bits.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'IMediaDet :: GetBitmapBits, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126853851"
---
# <a name="imediadetgetbitmapbits-method"></a>IMediaDet :: GetBitmapBits, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetBitmapBits` méthode récupère une image vidéo à l’heure du média spécifiée. Le frame retourné est toujours au format RGB 24 bits.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StreamTime* 
</dt> <dd>

Heure à laquelle récupérer l’image vidéo, en secondes.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Reçoit la taille de mémoire tampon requise. Si *pbuffer* a la **valeur null**, la variable reçoit la taille de la mémoire tampon nécessaire pour récupérer le frame. Si *pbuffer* n’a pas la **valeur null**, ce paramètre est ignoré.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit une structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) suivie des bits dib.

</dd> <dt>

*Width* 
</dt> <dd>

Largeur de l’image vidéo, en pixels.

</dd> <dt>

*Height* 
</dt> <dd>

Hauteur de l’image vidéo, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Il peut prendre les valeurs suivantes :



| Code de retour                                                                                             | Description                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Réussite.<br/>                                                                               |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>           | Impossible d’ajouter l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) au graphique.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>           | Mémoire insuffisante.<br/>                                                                   |
| <dl> <dt>**\_pointeur E**</dt> </dl>               | Erreur de pointeur **null** .<br/>                                                                |
| <dl> <dt>**E \_ inattendu**</dt> </dl>            | Erreur inattendue.<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Type de média non valide.<br/>                                                                    |



 

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Pour déterminer la taille de la mémoire tampon requise, appelez cette méthode avec *pbuffer* égal à **null**. La taille est retournée dans la variable vers laquelle pointe *pBufferSize*. Créez ensuite la mémoire tampon et rappelez la méthode, avec *pbuffer* égal à l’adresse de la mémoire tampon. Lorsque la méthode est retournée, la mémoire tampon contient une structure **BITMAPINFOHEADER** suivie de l’image bitmap. La bitmap est mise à l’échelle selon les dimensions spécifiées dans les paramètres de *largeur* et de *hauteur* .

Cette méthode met le détecteur de média en mode de manipulation bitmap. Une fois cette méthode appelée, les différentes méthodes d’informations de flux de **IMediaDet** ne fonctionnent pas, sauf si vous créez une nouvelle instance du détecteur de média.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="examples"></a>Exemples

Le code suivant utilise la `GetBitmapBits` méthode pour créer une image bitmap indépendante du périphérique.


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IMediaDet**](imediadet.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




