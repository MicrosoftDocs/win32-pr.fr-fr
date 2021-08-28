---
description: Rappel qui avertit l’hôte d’informations de mémoire tampon écrites dans un fichier par la demande dans.
MS-HAID: vspixengine.IBufferObjectDataCallback\_ResultCallback\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IBufferObjectDataCallback :: ResultCallback, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C8083FDF-0A56-4777-8EFD-66F77AD195EA
api_name:
- IBufferObjectDataCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: eaf084402c1cc34bff83d3b50002fbdcf3d97fb1
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122623095"
---
# <a name="span-idvspixengineibufferobjectdatacallback_resultcallback_bstrspanibufferobjectdatacallbackresultcallback-method"></a><span id="vspixengine.ibufferobjectdatacallback_resultcallback_bstr"></span>IBufferObjectDataCallback :: ResultCallback, méthode

Rappel qui avertit l’hôte d’informations de mémoire tampon écrites dans un fichier par la demande dans.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT ResultCallback(
   BSTR File
);
```

## <a name="parameters"></a>Paramètres

*Fichier* Chaîne COM qui contient le nom du chemin d’accès du fichier dans lequel les résultats sont écrits.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne **S_OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IBufferObjectDataCallback**](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
