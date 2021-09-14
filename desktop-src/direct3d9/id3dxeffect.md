---
description: Utilisé pour définir et interroger des effets, et pour choisir des techniques. Un objet Effect peut contenir plusieurs techniques pour afficher le même effet.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Interface ID3DXEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 275376234739964940d70381a34331ff5b89f2dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916424"
---
# <a name="id3dxeffect-interface"></a>Interface ID3DXEffect

Utilisé pour définir et interroger des effets, et pour choisir des techniques. Un objet Effect peut contenir plusieurs techniques pour afficher le même effet.

## <a name="members"></a>Membres

L’interface **ID3DXEffect** hérite de [**ID3DXBaseEffect**](id3dxbaseeffect.md). **ID3DXEffect** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXEffect** possède ces méthodes.



| Méthode                                                                | Description                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)       | Appliquez les valeurs d’un bloc d’État à l’état du système d’effet actuel.<br/>                                                                                                                 |
| [**Début**](id3dxeffect--begin.md)                                   | Démarre une technique active.<br/>                                                                                                                                                           |
| [**BeginParameterBlock**](id3dxeffect--beginparameterblock.md)       | Démarrer la capture des modifications d’État dans un bloc de paramètres.<br/>                                                                                                                                   |
| [**BeginPass**](id3dxeffect--beginpass.md)                           | Commence une passe, dans la technique active.<br/>                                                                                                                                           |
| [**CloneEffect**](id3dxeffect--cloneeffect.md)                       | Crée une copie d’un effet.<br/>                                                                                                                                                          |
| [**CommitChanges**](id3dxeffect--commitchanges.md)                   | Propage les modifications d’État qui se produisent à l’intérieur d’une passe active à l’appareil avant le rendu.<br/>                                                                                           |
| [**DeleteParameterBlock**](id3dxeffect--deleteparameterblock.md)     | Supprimer un bloc de paramètres.<br/>                                                                                                                                                             |
| [**End**](id3dxeffect--end.md)                                       | Met fin à une technique active.<br/>                                                                                                                                                             |
| [**EndParameterBlock**](id3dxeffect--endparameterblock.md)           | Arrêter la capture des modifications d’état des paramètres d’effet.<br/>                                                                                                                                        |
| [**EndPass**](id3dxeffect--endpass.md)                               | Terminer une passe active.<br/>                                                                                                                                                                   |
| [**FindNextValidTechnique**](id3dxeffect--findnextvalidtechnique.md) | Recherche la technique suivante valide, en commençant par la technique qui suit la technique spécifiée.<br/>                                                                                       |
| [**GetCurrentTechnique**](id3dxeffect--getcurrenttechnique.md)       | Obtient la technique actuelle.<br/>                                                                                                                                                           |
| [**GetDevice**](id3dxeffect--getdevice.md)                           | Récupère l’appareil associé à l’effet.<br/>                                                                                                                                      |
| [**GetPool**](id3dxeffect--getpool.md)                               | Obtient un pointeur vers le pool de paramètres partagés.<br/>                                                                                                                                      |
| [**GetStateManager**](id3dxeffect--getstatemanager.md)               | Obtient le gestionnaire d’état des effets.<br/>                                                                                                                                                         |
| [**IsParameterUsed**](id3dxeffect--isparameterused.md)               | Détermine si un paramètre est utilisé par la technique.<br/>                                                                                                                                   |
| [**OnLostDevice**](id3dxeffect--onlostdevice.md)                     | Utilisez cette méthode pour libérer toutes les références aux ressources de la mémoire vidéo et supprimer tous les stateblocks. Cette méthode doit être appelée chaque fois qu’un appareil est perdu, ou avant de réinitialiser un appareil.<br/> |
| [**OnResetDevice**](id3dxeffect--onresetdevice.md)                   | Utilisez cette méthode pour acquérir à nouveau des ressources et enregistrer l’état initial.<br/>                                                                                                                       |
| [**SetRawValue**](id3dxeffect--setrawvalue.md)                       | Définissez une plage contiguë de constantes de nuanceur avec une copie de mémoire.<br/>                                                                                                                        |
| [**SetStateManager**](id3dxeffect--setstatemanager.md)               | Définissez le gestionnaire d’état des effets.<br/>                                                                                                                                                         |
| [**SetTechnique**](id3dxeffect--settechnique.md)                     | Définit la technique active.<br/>                                                                                                                                                            |
| [**ValidateTechnique**](id3dxeffect--validatetechnique.md)           | Valider une technique.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Notes

L’interface ID3DXEffect est obtenue en appelant [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)ou [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).

Le type LPD3DXEFFECT est défini en tant que pointeur vers cette interface.


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Interfaces d’effet](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> <dt>

[**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




