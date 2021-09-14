---
description: l’interface ISmartRenderEngine fournit des méthodes qui prennent en charge la recompression intelligente dans DirectShow Services d’édition. Le moteur de rendu intelligent expose cette interface.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Interface ISmartRenderEngine (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007524"
---
# <a name="ismartrenderengine-interface"></a>Interface ISmartRenderEngine

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `ISmartRenderEngine` interface fournit des méthodes qui prennent en charge la recompression intelligente dans [DirectShow Services d’édition](directshow-editing-services.md) . Le moteur de rendu intelligent expose cette interface.

## <a name="members"></a>Membres

L’interface **ISmartRenderEngine** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISmartRenderEngine** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISmartRenderEngine** possède ces méthodes.



| Méthode                                                                | Description                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**GetGroupCompressor**](ismartrenderengine-getgroupcompressor.md)   | Récupère le filtre de compression pour le groupe spécifié.<br/>                 |
| [**SetFindCompressorCB**](ismartrenderengine-setfindcompressorcb.md) | Non implémenté.<br/>                                                          |
| [**SetGroupCompressor**](ismartrenderengine-setgroupcompressor.md)   | Spécifie un filtre de compression à utiliser lors du rendu du groupe spécifié.<br/> |



 

## <a name="remarks"></a>Notes

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

[Rendu d’un Project](rendering-a-project.md)
</dt> </dl>

 

 
