---
description: Demandes d’exécution de l’analyse hors connexion avec la source, le manifeste, les paramètres et le frame spécifiés.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'IOfflineAnalysisRequest :: RequestOfflineAnalysisAsync, méthode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a8a36f65f2158d03650257cf13458d36330e7fd3184210d99c05200e1731231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981139"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>IOfflineAnalysisRequest :: RequestOfflineAnalysisAsync, méthode

Demandes d’exécution de l’analyse hors connexion avec la source, le manifeste, les paramètres et le frame spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a>Paramètres

*analysisSource*   
Spécifie où la source d’analyse provient de rapports mis en cache ou de la lecture.

*manifestXml*   
Chaîne COM contenant le nom du chemin d’accès du fichier manifeste XML.

*parametersXml*   
Chaîne COM contenant le nom du chemin d’accès du fichier de paramètres XML.

*cookie*   
Cookie qui identifie de façon unique la demande et qui peut être utilisé pour signaler qu’il doit être annulé.

*captureFullFileName*   
Chaîne COM contenant le nom de chemin d’accès absolu du fichier de capture (. vsglog).

*frameNumber*   
Frame spécifié.

*outputFullFileName*   
Chaîne COM contenant le nom de chemin d’accès absolu du fichier dans lequel la sortie est écrite.

*requestCallback*   
Adresse d’un rappel utilisé pour notifier l’hôte de résultats.

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Voir aussi

[**IOfflineAnalysisRequest**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
