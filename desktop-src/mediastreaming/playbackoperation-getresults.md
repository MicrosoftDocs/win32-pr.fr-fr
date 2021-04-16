---
title: PlaybackOperation. GetResults, méthode
description: Retourne les résultats d’une opération asynchrone démarrée par l’une des méthodes de lecture MediaRenderer.
ms.assetid: EAA5B342-51EF-449A-A7E2-FFBDBE07757C
keywords:
- Méthode GetResults API de diffusion multimédia en continu
- Méthode GetResults API de diffusion multimédia en continu, interface PlaybackOperation
- API de diffusion multimédia en continu de l’interface PlaybackOperation, méthode GetResults
topic_type:
- apiref
api_name:
- PlaybackOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f146876966cc4e003bd88ad295c9938e5240abfe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380547"
---
# <a name="playbackoperationgetresults-method"></a>PlaybackOperation. GetResults, méthode

Retourne les résultats d’une opération asynchrone démarrée par l’une des méthodes de lecture [**MediaRenderer**](mediarenderer.md) .

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*valeur* \[ out, retval\]
</dt> <dd>

Résultat de l'opération. La valeur 0 indique que l’opération est terminée. Les autres valeurs sont réservées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

La méthode **GetResults** est généralement appelée à partir du gestionnaire d’événements qui a été enregistré en définissant la propriété [**Completed**](playbackoperation-completed.md) .

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PlaybackOperation**](playbackoperation.md)
</dt> </dl>

 

 





