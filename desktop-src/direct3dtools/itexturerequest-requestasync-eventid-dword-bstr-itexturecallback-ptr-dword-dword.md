---
description: Demande d’obtenir le contenu d’une texture sous la forme d’un. Fichier DDS (surface DirectDraw).
MS-HAID: vspixengine.ITextureRequest\_RequestAsync\_EventID\_DWORD\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ITextureRequest :: RequestAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 89A9F230-D296-43CD-A2A6-747057750EED
api_name:
- ITextureRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 24634372b8d1da7a880b881f4cf78285f974cf0f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622725"
---
# <a name="span-idvspixengineitexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dwordspanitexturerequestrequestasync-method"></a><span id="vspixengine.itexturerequest_requestasync_eventid_dword_bstr_itexturecallback_ptr_dword_dword"></span>ITextureRequest :: RequestAsync, méthode

Demande d’obtenir le contenu d’une texture sous la forme d’un. Fichier DDS (surface DirectDraw).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RequestAsync(
   EventID            eventID,
   DWORD              textureFileptr,
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
Adresse de l’objet de texture.

*ddsFilename*   
Chaîne COM qui contient le chemin d’accès du fichier. DDS dans lequel les résultats sont écrits.

*pRequestCallback*   
Adresse du rappel utilisée pour notifier l’hôte de résultats.

*requestCookie*   
Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.

*progressIntervalMsecs*   
Non utilisé.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**ITextureRequest**](/windows/desktop/direct3dtools/itexturerequest)

 

 
