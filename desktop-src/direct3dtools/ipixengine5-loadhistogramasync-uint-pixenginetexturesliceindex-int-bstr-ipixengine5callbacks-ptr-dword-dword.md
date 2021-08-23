---
description: Demande asynchrone de chargement des données de l’histogramme.
MS-HAID: vspixengine.IPixEngine5\_LoadHistogramAsync\_UINT\_PixEngineTextureSliceIndex\_int\_BSTR\_IPixEngine5Callbacks\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine5 :: LoadHistogramAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A23CB3E0-B299-40FD-899E-9FE6E9177551
api_name:
- IPixEngine5.LoadHistogramAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eab7942f62f67d9023ced3cfde82974c3ee824eb83d2570023bde02fbc1cbab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986079"
---
# <a name="span-idvspixengineipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dwordspanipixengine5loadhistogramasync-method"></a><span id="vspixengine.ipixengine5_loadhistogramasync_uint_pixenginetexturesliceindex_int_bstr_ipixengine5callbacks_ptr_dword_dword"></span>IPixEngine5 :: LoadHistogramAsync, méthode

Demande asynchrone de chargement des données de l’histogramme.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadHistogramAsync(
   UINT                       textureId,
   PixEngineTextureSliceIndex sliceIndex,
   int                        formatOverride,
   BSTR                       histogramDataFileName,
   IPixEngine5Callbacks*      callbacks,
   DWORD                      requestCookie,
   DWORD                      progressIntervalMsecs
);
```

## <a name="parameters"></a>Paramètres

*textureId*   
ID de la texture pour laquelle charger les données de l’histogramme.

*sliceIndex*   
Index de la tranche pour laquelle charger les données de l’histogramme.

*formatOverride*   
Spécifie la substitution de format.

*histogramDataFileName*   
Chaîne COM contenant le nom du fichier de données de l’histogramme.

*rappels*   
Adresse d’un objet qui fournit l’interface de rappels IPixEngine5.

*requestCookie*   
Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.

*progressIntervalMsecs*   
Non utilisé.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPixEngine5**](/windows/desktop/direct3dtools/ipixengine5)

 

 
