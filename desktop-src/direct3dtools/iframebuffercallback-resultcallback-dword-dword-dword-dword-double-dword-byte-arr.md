---
description: Rappel qui avertit l’hôte des informations trame retournées par la requête associée.
MS-HAID: vspixengine.IFrameBufferCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_double\_DWORD\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IFrameBufferCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F0276125-2DA9-45BC-A295-BD67C21EE601
api_name:
- IFrameBufferCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2308ec5355da8f8fda7eeccf31d1cbe19e8a8247
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626675"
---
# <a name="span-idvspixengineiframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arrspaniframebuffercallbackresultcallback-method"></a><span id="vspixengine.iframebuffercallback_resultcallback_dword_dword_dword_dword_double_dword_byte_arr"></span>IFrameBufferCallback :: ResultCallback, méthode

Rappel qui avertit l’hôte des informations trame retournées par la requête associée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ResultCallback(
   DWORD   frameNumber,
   DWORD   width,
   DWORD   height,
   DWORD   renderTargetPtr,
   double  frameDuraction,
   DWORD   size,
   BYTE [] count5_buffer
);
```

## <a name="parameters"></a>Paramètres

*frameNumber*   
Numéro de frame.

*Largeur*   
Largeur du cadre.

*celle*   
Hauteur du cadre.

*renderTargetPtr*   
Cible de rendu d’où proviennent les résultats. Il s’agit toujours d’un emplacement spécifié par la demande de mémoire tampon de trame ou, s’il ne s’agit pas d’un appel de dessin, le premier RTV Bount à la source de sortie.

*frameDuraction*   
Non utilisé.

*corps*   
Taille de la mémoire tampon de sortie en octets.

*\_mémoire tampon count5*   
Contenu de la cible de rendu au \_ format R8G8B8A8 UNORM.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IFrameBufferCallback**](/windows/desktop/direct3dtools/iframebuffercallback)

 

 
