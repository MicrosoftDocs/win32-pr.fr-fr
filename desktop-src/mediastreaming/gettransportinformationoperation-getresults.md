---
title: GetTransportInformationOperation GetResults, méthode
description: Retourne les résultats de l’opération asynchrone démarrée par GetTransportInformationAsync.
ms.assetid: 8CC6641E-C1E6-4C64-90EC-4120ECB54135
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface GetTransportInformationOperation
- API de diffusion multimédia en continu de l’interface GetTransportInformationOperation, méthode GetResults
topic_type:
- apiref
api_name:
- GetTransportInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17f846a5824ed07bcaf849a540429eaabe46f3d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381899"
---
# <a name="gettransportinformationoperationgetresults-method"></a>GetTransportInformationOperation :: GetResults, méthode

Retourne les résultats de l’opération asynchrone démarrée par [**GetTransportInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-gettransportinformationasync).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetResults(
  [out, retval] TransportInformation *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Référence à une structure [**TransportInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-transportinformation) qui contient les résultats de l’opération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

La méthode **GetResults** est généralement appelée à partir du gestionnaire d’événements qui a été enregistré en définissant la propriété [**Completed**](gettransportinformationoperation-completed.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetTransportInformationOperation**](gettransportinformationoperation.md)
</dt> </dl>

 

