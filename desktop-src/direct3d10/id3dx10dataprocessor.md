---
description: Objet de traitement de données utilisé par l’interface ID3DX10ThreadPump pour le traitement des données chargées de façon asynchrone.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interface ID3DX10DataProcessor (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ddb192a0591ce241e216b3bd0471212fc4801fbf1c901430c187f5370237049d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128369"
---
# <a name="id3dx10dataprocessor-interface"></a>Interface ID3DX10DataProcessor

Objet de traitement de données utilisé par l' [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour le traitement des données chargées de façon asynchrone.

## <a name="members"></a>Membres

L’interface **ID3DX10DataProcessor** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataProcessor** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX10DataProcessor** possède ces méthodes.



| Méthode                                                                | Description                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md) | Créez un objet d’appareil.<br/>                                                                                                  |
| [**Suppression**](id3dx10dataprocessor-destroy.md)                       | Utilisé par une [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour détruire le processeur après l’achèvement d’un élément de travail.<br/> |
| [**Processus**](id3dx10dataprocessor-process.md)                       | Traitez des données.<br/>                                                                                                       |



 

## <a name="remarks"></a>Remarques

Cet objet peut être hérité et ses membres redéfinis. Cela vous permettrait de personnaliser l’API pour le traitement de vos propres formats de fichier personnalisés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
