---
description: La méthode SetResizerGUID spécifie le CLSID d’un filtre de redimensionnement vidéo personnalisé.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'IRenderEngine2 :: SetResizerGUID, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530004"
---
# <a name="irenderengine2setresizerguid-method"></a>IRenderEngine2 :: SetResizerGUID, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

La `SetResizerGUID` méthode spécifie le CLSID d’un filtre de redimensionnement vidéo personnalisé. Appelez cette méthode pour remplacer le filtre de redimensionnement par défaut utilisé par les services d’édition DirectShow. Votre filtre doit être inscrit en tant qu’objet COM sur le système de l’utilisateur et doit prendre en charge l’interface [**IResize**](iresize.md) .

Appelez cette méthode avant d’appeler [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ResizerGuid* \[ dans\]
</dt> <dd>

CLSID du filtre.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Pour rétablir la valeur par défaut DES redimensionnements, utilisez le CLSID suivant :


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 ou version ultérieure<br/>                                                         |
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> <dt>

[**Interface IRenderEngine2**](irenderengine2.md)
</dt> </dl>

 

 




