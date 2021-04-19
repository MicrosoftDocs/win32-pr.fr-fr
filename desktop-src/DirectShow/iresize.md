---
description: 'L’interface IResize doit être prise en charge par n’importe quel filtre de redimensionnement vidéo personnalisé pour les services de modification DirectShow (DES). Pour définir un filtre de redimensionnement personnalisé, appelez la méthode IRenderEngine2 :: SetResizerGUID sur le moteur de rendu.'
ms.assetid: 4740dbff-0881-45e8-b382-98ed9d055403
title: Interface IResize (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1b9684ed6f2d2901159dde5a79bb4563ca0b2bda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538754"
---
# <a name="iresize-interface"></a>Interface IResize

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IResize` interface doit être prise en charge par n’importe quel filtre de redimensionnement vidéo personnalisé pour les services d’édition DirectShow (des). Pour définir un filtre de redimensionnement personnalisé, appelez la méthode [**IRenderEngine2 :: SetResizerGUID**](irenderengine2-setresizerguid.md) sur le moteur de rendu.

## <a name="members"></a>Membres

L’interface **IResize** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IResize** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IResize** possède ces méthodes.



| Méthode                                          | Description                                                  |
|:------------------------------------------------|:-------------------------------------------------------------|
| [**récupération inversée \_**](iresize-get-inputsize.md) | Retourne la taille d’entrée actuelle du filtre de redimensionnement.<br/>  |
| [**Obtient le \_ MediaType**](iresize-get-mediatype.md) | Retourne le type de média de sortie du filtre de redimensionnement.<br/>   |
| [**récupérer la \_ taille**](iresize-get-size.md)           | Retourne la taille de sortie actuelle et le mode Stretch.<br/> |
| [**Placer le \_ MediaType**](iresize-put-mediatype.md) | Définit le type de média de sortie.<br/>                       |
| [**taille de l’put \_**](iresize-put-size.md)           | Définit la taille de sortie et le mode Stretch.<br/>            |



 

## <a name="remarks"></a>Notes

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

[Fournir un redimensionnement vidéo personnalisé](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
