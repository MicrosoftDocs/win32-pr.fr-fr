---
description: La méthode GetGroupCompressor récupère le filtre de compression pour le groupe spécifié.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'ISmartRenderEngine :: GetGroupCompressor, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 65915039d26b3c8739441240419e61e0cbacf5a6f4212cbb1c8b456f55dfcbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817437"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a>ISmartRenderEngine :: GetGroupCompressor, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetGroupCompressor` méthode récupère le filtre de compression pour le groupe spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Groupe* 
</dt> <dd>

Index de base zéro du groupe.

</dd> <dt>

*pCompressor* 
</dt> <dd>

Reçoit un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre de compression. Elle reçoit la valeur **null** s’il n’existe aucun filtre de compression.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Utilisez cette méthode pour définir les propriétés du filtre de compression, telles que la fréquence d’images clés. Appelez cette méthode après avoir appelé [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md), mais avant de restituer le projet. Interrogez ensuite la broche de sortie du filtre de compression pour l’interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , qui contient des méthodes pour définir des paramètres de compression. Relâchez l’interface lorsque vous avez terminé. Si vous apportez des modifications ultérieures à la chronologie, appelez **ConnectFrontEnd**, puis appelez à nouveau **GetGroupCompressor** pour réinitialiser les paramètres de compression.

En cas de retour, si la valeur de \* *pCompressor* est non **null**, l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) a un nombre de références en suspens. Veillez à libérer l’interface lorsque vous avez fini de l’utiliser.

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

[**Interface ISmartRenderEngine**](ismartrenderengine.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




