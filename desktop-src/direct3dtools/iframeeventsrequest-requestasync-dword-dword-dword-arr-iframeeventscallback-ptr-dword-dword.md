---
description: Demande asynchrone pour obtenir des informations spécifiées sur un frame spécifié unique.
MS-HAID: vspixengine.IFrameEventsRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IFrameEventsCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameEventsRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 821E7674-A960-46F6-A7AF-386298902ED6
api_name:
- IFrameEventsRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a001f6a29d17806271ca4f5d29dc80d6e36251bf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108830"
---
# <a name="span-idvspixengineiframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dwordspaniframeeventsrequestrequestasync-method"></a><span id="vspixengine.iframeeventsrequest_requestasync_dword_dword_dword_arr_iframeeventscallback_ptr_dword_dword"></span>IFrameEventsRequest :: RequestAsync, méthode

Demande asynchrone pour obtenir des informations spécifiées sur un frame spécifié unique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RequestAsync(
   DWORD                  frameNumber,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IFrameEventsCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a>Paramètres

*frameNumber*   
Frame spécifié.

*numColumns*   
Colonnes spécifiées (champs).

*\_colonnes count1*   
Adresse du rappel utilisée pour notifier l’hôte de résultats.

*requestCallback*   
Adresse du rappel utilisée pour notifier l’hôte de résultats.

*requestCookie*   
Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.

*progressIntervalMsecs*   
Non utilisé.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IFrameEventsRequest**](/windows/desktop/direct3dtools/iframeeventsrequest)

 

 
