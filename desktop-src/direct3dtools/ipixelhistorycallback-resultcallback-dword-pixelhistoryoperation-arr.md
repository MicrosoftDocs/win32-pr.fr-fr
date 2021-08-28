---
description: Rappel qui avertit l’hôte des résultats de la requête de l’historique des pixels.
MS-HAID: vspixengine.IPixelHistoryCallback\_ResultCallback\_DWORD\_PixelHistoryOperation\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixelHistoryCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1F7D0EA5-402A-49C4-A83E-91596AE9536B
api_name:
- IPixelHistoryCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7c5af9e88bde60121e8cbc78863b631c4cd41305
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622365"
---
# <a name="span-idvspixengineipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arrspanipixelhistorycallbackresultcallback-method"></a><span id="vspixengine.ipixelhistorycallback_resultcallback_dword_pixelhistoryoperation_arr"></span>IPixelHistoryCallback :: ResultCallback, méthode

Rappel qui avertit l’hôte des résultats de la requête de l’historique des pixels.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResultCallback(
   DWORD                    count,
   PixelHistoryOperation [] count0_pixelHistoryOperation
);
```

## <a name="parameters"></a>Paramètres

*saut*   
Nombre de résultats.

*count0 \_ pixelHistoryOperation*   
Résultats

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPixelHistoryCallback**](/windows/desktop/direct3dtools/ipixelhistorycallback)

 

 
