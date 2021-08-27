---
description: Exécute une expérience.
MS-HAID: vspixengine.IPixEngine\_RunExperiment\_Experiment\_IRunExperimentCallback\_ptr\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_DWORD\_ExperimentTrigger\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IPixEngine :: RunExperiment, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A2EEC278-C074-44B3-94DC-E2D9DC770576
api_name:
- IPixEngine.RunExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 49ff62c3dfc379e5cc2b0741d70644c88509240b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621895"
---
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine :: RunExperiment, méthode

Exécute une expérience.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RunExperiment(
   Experiment               experiment,
   IRunExperimentCallback * pRequestCallback,
   INewFramesCallback*      callbacks,
   IFileIOCallback*         pFileIOCallback,
   DWORD                    triggersCount,
   ExperimentTrigger []     count4_triggersBuffer
);
```

## <a name="parameters"></a>Paramètres

*expérimenté*   
Décrit l’expérience à exécuter.

*pRequestCallback*   
Adresse d’une fonction utilisée pour informer l’hôte que le moteur a démarré l’expérimentation.

*rappels*   
Adresse d’une fonction utilisée pour informer l’hôte que de nouveaux frames ont été capturés.

*pFileIOCallback*   
Adresse d’une fonction utilisée pour notifier l’hôte des erreurs d’e/s de fichier lors de l’analyse.

*triggersCount*   
Nombre de déclencheurs dans l’expérience.

*count4 \_ triggersBuffer*   
Déclencheurs de capture.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IPixEngine**](/windows/desktop/direct3dtools/ipixengine)

 

 
