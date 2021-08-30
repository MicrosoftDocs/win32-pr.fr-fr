---
description: Fonction de rappel utilisée pour informer l’hôte que l’analyse hors connexion est terminée.
MS-HAID: vspixengine.IOfflineAnalysisCallback\_OfflineAnalysisComplete\_DWORD\_HRESULT\_BSTR
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisCallback :: OfflineAnalysisComplete, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36E10709-51DC-4657-B184-F1F807ABBBB4
api_name:
- IOfflineAnalysisCallback.OfflineAnalysisComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8829fbb94800a295f5e13ad2ec3c907c64fbfc93
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624145"
---
# <a name="span-idvspixengineiofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstrspaniofflineanalysiscallbackofflineanalysiscomplete-method"></a><span id="vspixengine.iofflineanalysiscallback_offlineanalysiscomplete_dword_hresult_bstr"></span>IOfflineAnalysisCallback :: OfflineAnalysisComplete, méthode

Fonction de rappel utilisée pour informer l’hôte que l’analyse hors connexion est terminée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OfflineAnalysisComplete(
   DWORD   cookie,
   HRESULT result,
   BSTR    outputFullFileName
);
```

## <a name="parameters"></a>Paramètres

*cookie*   
Cookie qui identifie de façon unique la demande qui a initié l’analyse hors connexion.

*venir*   
Indique si l’analyse hors connexion a réussi ou échoué. Si elle réussit, les résultats ont été écrits dans un fichier.

*outputFullFileName*   
Chaîne COM contianing le nom du fichier dans lequel les résultats de l’analyse hors connexion ont été écrits.

## <a name="return-value"></a>Valeur de retour

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IOfflineAnalysisCallback**](/windows/desktop/direct3dtools/iofflineanalysiscallback)

 

 
