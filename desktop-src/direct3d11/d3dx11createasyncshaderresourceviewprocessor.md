---
title: D3DX11CreateAsyncShaderResourceViewProcessor, fonction (D3DX11async. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.'
ms.assetid: bd9349af-f433-47f9-b443-3049c32fc286
keywords:
- Fonction D3DX11CreateAsyncShaderResourceViewProcessor Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncShaderResourceViewProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305705a4fd82b7f2267e3d56630b78c8c8d98473d946b1629e713162f4a6ae92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536568"
---
# <a name="d3dx11createasyncshaderresourceviewprocessor-function"></a>D3DX11CreateAsyncShaderResourceViewProcessor fonction)

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Consultez la section Notes.

 

Créez un processeur de données qui chargera une ressource, puis créez une vue de ressource de nuanceur pour celle-ci. Les processeurs de données sont un composant de la fonctionnalité de chargement de données asynchrone dans D3DX11 qui utilise des [**pompes de thread**](id3dx11threadpump.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX11CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D11Device           *pDevice,
  _In_  D3DX11_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX11DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\***

Pointeur vers le périphérique Direct3D (voir [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) qui sera utilisé pour créer une ressource et une vue de ressource Shader pour cette ressource.

</dd> <dt>

*pLoadInfo* \[ dans\]
</dt> <dd>

Type : **[ **\_ \_ \_ informations sur le chargement de l’image D3DX11**](d3dx11-image-load-info.md)\***

Facultatif. Identifie les caractéristiques d’une texture (voir informations sur le chargement de l' [**\_ image \_ \_ D3DX11**](d3dx11-image-load-info.md)) lorsque le processeur de données est créé ; affectez la valeur **null** pour lire les caractéristiques d’une texture lorsque la texture est chargée.

</dd> <dt>

*ppDataProcessor* \[ à\]
</dt> <dd>

Type : **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\*\***

Adresse d’un pointeur vers une mémoire tampon qui contient le processeur de données créé (voir [**interface ID3DX11DataProcessor**](id3dx11dataprocessor.md)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarques

Il n’y a aucune implémentation du chargeur asynchrone en dehors de D3DX 10 et D3DX 11.

pour les applications Windows store, les exemples DirectX (par exemple, l' [exemple de didacticiel Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluent le module **BasicLoader** qui utilise le Windows Runtime modèle de programmation asynchrone ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).

pour les applications de bureau Win32, vous pouvez utiliser le [runtime d’accès concurrentiel](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) pour implémenter un modèle semblable au Windows Runtime modèle de programmation asynchrone.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11async. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[D3DX, fonctions](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

