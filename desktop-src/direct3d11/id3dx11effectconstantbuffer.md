---
title: Interface ID3DX11EffectConstantBuffer (D3dx11effect. h)
description: Une interface de mémoire tampon constante accède aux mémoires tampons constantes ou aux mémoires tampons de texture.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Interface ID3DX11EffectConstantBuffer Direct3D 11
- Interface ID3DX11EffectConstantBuffer Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323078"
---
# <a name="id3dx11effectconstantbuffer-interface"></a>Interface ID3DX11EffectConstantBuffer

Une interface de mémoire tampon constante accède aux mémoires tampons constantes ou aux mémoires tampons de texture.

## <a name="members"></a>Membres

L’interface **ID3DX11EffectConstantBuffer** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectConstantBuffer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11EffectConstantBuffer** possède ces méthodes.



| Méthode                                                                             | Description                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetConstantBuffer**](id3dx11effectconstantbuffer-getconstantbuffer.md)         | Obtient une mémoire tampon constante.<br/>                    |
| [**GetTextureBuffer**](id3dx11effectconstantbuffer-gettexturebuffer.md)           | Obtenir une mémoire tampon de texture.<br/>                     |
| [**SetConstantBuffer**](id3dx11effectconstantbuffer-setconstantbuffer.md)         | Définissez une mémoire tampon constante.<br/>                    |
| [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md)           | Définissez une texture-buffer.<br/>                     |
| [**UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | Restaure une mémoire tampon constante définie précédemment.<br/> |
| [**UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | Restaure une mémoire tampon de texture précédemment définie.<br/>  |



 

## <a name="remarks"></a>Notes

Utilisez des mémoires tampons constantes pour stocker de nombreuses constantes d’effet ; regroupement de constantes dans des tampons en fonction de leur fréquence de mise à jour. Cela vous permet de réduire le nombre de modifications d’État et d’effectuer le moins d’appels d’API pour modifier l’État. Ces deux facteurs conduisent à de meilleures performances.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effets 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





