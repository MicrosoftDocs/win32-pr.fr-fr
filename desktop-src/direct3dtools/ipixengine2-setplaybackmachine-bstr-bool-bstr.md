---
description: Définit l’ordinateur de lecture actuel pour le journal des graphiques spécifié.
MS-HAID: vspixengine.IPixEngine2\_SetPlaybackMachine\_BSTR\_BOOL\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine2 :: SetPlaybackMachine, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 181EE044-1FC4-484B-AE63-C33BC627C3B7
api_name:
- IPixEngine2.SetPlaybackMachine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c1c4ca173b9ccef80d6f9d89f1829f7170459e90
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628175"
---
# <a name="span-idvspixengineipixengine2_setplaybackmachine_bstr_bool_bstrspanipixengine2setplaybackmachine-method"></a><span id="vspixengine.ipixengine2_setplaybackmachine_bstr_bool_bstr"></span>IPixEngine2 :: SetPlaybackMachine, méthode

Définit l’ordinateur de lecture actuel pour le journal des graphiques spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetPlaybackMachine(
   BSTR logFile,
   BOOL bUseAuthentication,
   BSTR machine
);
```

## <a name="parameters"></a>Paramètres

*Relog*   
Chaîne COM contianing le nom du journal de graphisme.

*bUseAuthentication*   
true pour utiliser l’authentification ; Sinon, false.

*usinage*   
Chaîne COM contenant le nom de l’ordinateur de lecture.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
