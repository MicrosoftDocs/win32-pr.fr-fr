---
description: Transmet de manière asynchrone des ressources au moteur, telles que des chaînes pour les messages d’erreur.
MS-HAID: vspixengine.IPixEngine7\_InitEngineAsync\_ResourcePair\_arr\_UINT\_IVersionCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine7 :: InitEngineAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 10138B39-88D2-4586-BD51-C618722EFFA0
api_name:
- IPixEngine7.InitEngineAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7d477fe54622631f1729f05e39f6d2682a7b422b7508c033a7a342b04c6918d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985939"
---
# <a name="span-idvspixengineipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dwordspanipixengine7initengineasync-method"></a><span id="vspixengine.ipixengine7_initengineasync_resourcepair_arr_uint_iversioncallback_ptr_dword_dword"></span>IPixEngine7 :: InitEngineAsync, méthode

Transmet de manière asynchrone des ressources au moteur, telles que des chaînes pour les messages d’erreur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT InitEngineAsync(
   ResourcePair []   count1_resources,
   UINT              count,
   IVersionCallback* versionCallback,
   DWORD             requestCookie,
   DWORD             progressIntervalMsecs
);
```

## <a name="parameters"></a>Paramètres

*\_ressources count1*   
Tableau de ressources.

*saut*   
Nombre de ressources dans les \_ ressources count1

*versionCallback*   
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

[**IPixEngine7**](/windows/desktop/direct3dtools/ipixengine7)

 

 
