---
description: Demande à obtenir le contenu d’une texture en mosaïque sous la forme d’un. Fichier DDS (surface DirectDraw).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ITileRequest :: RequestTextureTileAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 20e67b9cd6d05e32488246306edb80d35fc8c6379fe4054f2cb1d7858f8e7402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119463"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>ITileRequest :: RequestTextureTileAsync, méthode

Demande à obtenir le contenu d’une texture en mosaïque sous la forme d’un. Fichier DDS (surface DirectDraw).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a>Paramètres

*1001*   
Événement spécifié pour faire correspondre le contenu de la mémoire tampon à (par exemple, une cible de rendu peut changer au fil du temps).

*textureFileptr*   
Adresse de l’objet de texture spécifié.

*tileSubresource*   
Sous-ressource spécifiée de la vignette.

*tileX*   
Position X de la mosaïque spécifiée.

*mosaïque*   
Position Y de la mosaïque spécifiée.

*tileZ*   
Position Z de la mosaïque spécifiée.

*ddsFilename*   
Chaîne COM qui contient le chemin d’accès du fichier. DDS dans lequel les résultats sont écrits.

*pRequestCallback*   
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

[**ITileRequest**](/windows/desktop/direct3dtools/itilerequest)

 

 
