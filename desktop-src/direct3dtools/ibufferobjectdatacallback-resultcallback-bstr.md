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
ms.openlocfilehash: 3a1ece7d54ccc27a91f47cb6d5cad1c2ff5861a038c10ed42d83eceef67fb4a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406209"
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

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne **S_OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IBufferObjectDataCallback**](/windows/desktop/direct3dtools/ibufferobjectdatacallback)

 

 
