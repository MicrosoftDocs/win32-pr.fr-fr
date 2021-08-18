---
title: GetMuteOperation. GetResults, méthode
description: Retourne les résultats de l’opération asynchrone démarrée par GetMuteAsync.
ms.assetid: 5B6DB1B3-54D4-486D-AA03-5FEEC92304B0
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface GetMuteOperation
- API de diffusion multimédia en continu de l’interface GetMuteOperation, méthode GetResults
topic_type:
- apiref
api_name:
- GetMuteOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 37b8356a677f5e752fdf4e4ec658cc4077a17fa76b6181097d5753d898eef89e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972408"
---
# <a name="getmuteoperationgetresults-method"></a>GetMuteOperation. GetResults, méthode

Retourne les résultats de l’opération asynchrone démarrée par [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetResults(
  [out, retval] boolean *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Valeur de silence. La valeur true indique que l’audio est actuellement en sourdine. La valeur false indique que l’audio n’est pas muet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

La méthode **GetResults** est généralement appelée à partir du gestionnaire d’événements qui a été enregistré en définissant la propriété [**Completed**](getmuteoperation-completed.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetMuteOperation**](getmuteoperation.md)
</dt> </dl>

 

