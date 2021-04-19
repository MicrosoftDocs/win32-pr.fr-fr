---
description: La méthode WriteBitmapBits récupère une image vidéo à l’heure du média spécifiée et l’écrit dans un fichier. La trame vidéo est toujours au format RGB 24 bits.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'IMediaDet :: WriteBitmapBits, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542570"
---
# <a name="imediadetwritebitmapbits-method"></a>IMediaDet :: WriteBitmapBits, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `WriteBitmapBits` méthode récupère une image vidéo à l’heure du média spécifiée et l’écrit dans un fichier. La trame vidéo est toujours au format RGB 24 bits.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*StreamTime* 
</dt> <dd>

Heure à laquelle récupérer l’image vidéo.

</dd> <dt>

*Width* 
</dt> <dd>

Largeur de l’image, en pixels.

</dd> <dt>

*Height* 
</dt> <dd>

Hauteur de l’image, en pixels.

</dd> <dt>

*Nom du fichier* 
</dt> <dd>

Chemin d’accès du fichier dans lequel enregistrer l’image bitmap. Si le fichier existe déjà, cette méthode le remplace.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK correctement. Sinon, retourne une valeur **HRESULT** qui indique la cause de l’erreur. Les codes d’erreur possibles sont les suivants :



| Code de retour                                                                                             | Description                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ NOinterface**</dt> </dl>           | Impossible d’ajouter l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) au graphique.<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl>                  | Échec.<br/>                                                                               |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl>           | Mémoire insuffisante.<br/>                                                                   |
| <dl> <dt>**E \_ inattendu**</dt> </dl>            | Erreur inattendue.<br/>                                                                      |
| <dl> <dt>**STG \_ E \_ ACCESSDENIED**</dt> </dl>     | Impossible de remplacer le fichier.<br/>                                                                 |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Type de média non valide.<br/>                                                                    |



 

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Cette méthode met le détecteur de média en mode de manipulation bitmap. Une fois cette méthode appelée, les différentes méthodes d’informations de flux de **IMediaDet** ne fonctionnent pas, sauf si vous créez une nouvelle instance du détecteur de média.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



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

 

 




