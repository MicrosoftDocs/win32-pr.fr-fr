---
description: Obtient la version de communication à distance du moteur.
MS-HAID: vspixengine.IPixEngine6\_GetRemotingVersion\_RemotingVersion\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine6 :: GetRemotingVersion, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 065FC3A7-ECFB-4551-B4B0-CA0E6B8676F8
api_name:
- IPixEngine6.GetRemotingVersion
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d949397959ac35ee52dfb5d03d7da8eaf629610b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622915"
---
# <a name="span-idvspixengineipixengine6_getremotingversion_remotingversion_ptrspanipixengine6getremotingversion-method"></a><span id="vspixengine.ipixengine6_getremotingversion_remotingversion_ptr"></span>IPixEngine6 :: GetRemotingVersion, méthode

Obtient la version de communication à distance du moteur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRemotingVersion(
   RemotingVersion * pRemoteVersion
);
```

## <a name="parameters"></a>Paramètres

*pRemoteVersion*   
Version de communication à distance du moteur.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPixEngine6**](/windows/desktop/direct3dtools/ipixengine6)

 

 
