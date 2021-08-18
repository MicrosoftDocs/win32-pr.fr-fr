---
description: Fonction de rappel utilisée pour notifier l’hôte quand une charge de texture est terminée.
MS-HAID: vspixengine.IPixEngine5Callbacks\_LoadTextureFromFileComplete\_UINT\_PixEngineTextureDescriptor\_UINT\_PixEngineTextureSliceIndex\_arr\_PixEngineTextureSliceDescriptor\_arr\_UINT\_int\_arr\_PixEngineHistogram\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5Callbacks :: LoadTextureFromFileComplete, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e9a9530fb9ada600d818494565765655c2c8cfb3bca938d8b9dff9d240aa6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985969"
---
# <a name="span-idvspixengineipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptrspanipixengine5callbacksloadtexturefromfilecomplete-method"></a><span id="vspixengine.ipixengine5callbacks_loadtexturefromfilecomplete_uint_pixenginetexturedescriptor_uint_pixenginetexturesliceindex_arr_pixenginetextureslicedescriptor_arr_uint_int_arr_pixenginehistogram_ptr"></span>IPixEngine5Callbacks :: LoadTextureFromFileComplete, méthode

Fonction de rappel utilisée pour notifier l’hôte quand une charge de texture est terminée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadTextureFromFileComplete(
   UINT                               textureId,
   PixEngineTextureDescriptor         textureDesc,
   UINT                               numSlices,
   PixEngineTextureSliceIndex []      count2_sliceIndicies,
   PixEngineTextureSliceDescriptor [] count2_sliceDescriptors,
   UINT                               numFormatOverrides,
   int []                             count5_formatOverrides,
   PixEngineHistogram*                histogram
);
```

## <a name="parameters"></a>Paramètres

*textureId*   
ID de la texture chargée.

*textureDesc*   
Descripteur de texture de la texture chargée.

*numSlices*   
Nombre de secteurs de la texture.

*count2 \_ sliceIndicies*   
Les indices de tranche associés à la texture.

*count2 \_ sliceDescriptors*   
Descripteurs pour chaque tranche.

*numFormatOverrides*   
Nombre de remplacements de format.

*count5 \_ formatOverrides*   
Le format remplace.

*histogramme*   
Adresse des données d’histogramme pour la texture chargée.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPixEngine5Callbacks**](/windows/desktop/direct3dtools/ipixengine5callbacks)

 

 
