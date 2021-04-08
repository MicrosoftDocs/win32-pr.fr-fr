---
title: GetPositionInformationOperation. GetResults, méthode
description: Retourne les résultats de l’opération asynchrone démarrée par GetPositionInformationAsync.
ms.assetid: 1DC7CD65-1F0F-44A5-9836-C77A5C23F91E
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface GetPositionInformationOperation
- API de diffusion multimédia en continu de l’interface GetPositionInformationOperation, méthode GetResults
topic_type:
- apiref
api_name:
- GetPositionInformationOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a0b4311c3be814a73ddb1e2a9b18d8e19aea9ee
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726757"
---
# <a name="getpositioninformationoperationgetresults-method"></a>GetPositionInformationOperation. GetResults, méthode

Retourne les résultats de l’opération asynchrone démarrée par [**GetPositionInformationAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getpositioninformationasync).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetResults(
  [out, retval] PositionInformation *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Référence à une structure [**PositionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-positioninformation) qui contient les résultats de l’opération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

La méthode **GetResults** est généralement appelée à partir du gestionnaire d’événements qui a été enregistré en définissant la propriété [**Completed**](getpositioninformationoperation-completed.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetPositionInformationOperation**](getpositioninformationoperation.md)
</dt> </dl>

 

