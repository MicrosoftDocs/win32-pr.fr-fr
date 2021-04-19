---
title: MpThreatOpen, fonction (MpClient. h)
description: Retourne un handle d’énumération à des fins de récupération des menaces.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpThreatOpen
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513784"
---
# <a name="mpthreatopen-function"></a>MpThreatOpen fonction)

Retourne un handle d’énumération à des fins de récupération des menaces. Cette fonction peut être utilisée pour ouvrir les menaces détectées par une analyse spécifique, toutes les menaces actives dans le système, l’historique de la désinfection des menaces ou toutes les menaces présentes dans la base de données de signature.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hScanHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Peut être un handle vers une opération d’analyse terminée, retourné par la fonction [**MpScanStart**](mpscanstart.md) . Ce paramètre peut également être défini sur le descripteur de l’interface du gestionnaire de protection contre les programmes malveillants renvoyé par [**MpManagerOpen**](mpmanageropen.md) pour énumérer toutes les menaces actives dans le système, l’historique de la désinfection des menaces ou les menaces provenant de la base de données de signatures.

</dd> <dt>

*ThreatSource* \[ dans\]
</dt> <dd>

Type : **MPTHREAT \_ source**

Utilisé pour contrôler la source de l’énumération des menaces. Les valeurs possibles pour ce paramètre sont les suivantes :



| Valeur                                                                                                                                                                                                 | Signification                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <dt>**analyse de la \_ source MPTHREAT \_**</dt> </dl>                   | Menaces associées au descripteur de numérisation spécifique.<br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <dt>**\_source MPTHREAT \_ active**</dt> </dl>             | Les menaces qui sont actuellement actives dans le système.<br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <dt>**historique de la \_ source MPTHREAT \_**</dt> </dl>          | Menaces qui sont traitées et conservées en tant qu’historique.<br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <dt>**mise en quarantaine de la \_ source MPTHREAT \_**</dt> </dl> | Menaces mises en quarantaine.<br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <dt>**\_signature source \_ MPTHREAT**</dt> </dl>    | Menaces pouvant être détectées avec la base de données de signature actuelle.<br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <dt>**État de la \_ source MPTHREAT \_**</dt> </dl>                | Menaces qui ont été traitées récemment. (« Récemment » est défini par un paramètre interne configurable.)<br/> |



 

</dd> <dt>

*ThreatType* \[ dans\]
</dt> <dd>

Type : **MPTHREAT \_**

Utilisé pour filtrer les menaces énumérées en fonction du type de détection. Les valeurs possibles pour ce paramètre sont les suivantes :



| Valeur                                                                                                                                                                                           | Signification                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <dt>**MPTHREAT \_ type \_ KNOWNBAD**</dt> </dl>       | La détection est effectuée sur la base d’une signature spécifique, d’une émulation ou d’une autre méthode de détection des menaces.<br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <dt>**TYPE de MPTHREAT \_ \_ suspect**</dt> </dl> | La détection est effectuée en fonction de l’analyse du comportement.<br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <dt>**\_type MPTHREAT \_ inconnu**</dt> </dl>          | La détection est effectuée en fonction de menaces inconnues (non classifiées).<br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <dt>**MPTHREAT \_ type \_ KNOWNGOOD**</dt> </dl>    | La détection est effectuée sur la base de menaces connues.<br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <dt>**MPTHREAT \_ type \_ NIS**</dt> </dl>                      | La détection est effectuée en fonction des menaces NIS.<br/>                                                       |



 

</dd> <dt>

*phThreatEnumHandle* \[ à\]
</dt> <dd>

Type : **PMPHANDLE**

Descripteur d’énumération des menaces retourné qui identifie le contexte de l’énumération. Ce descripteur peut être utilisé pour énumérer les informations sur les menaces à l’aide de [**MpThreatEnumerate**](mpthreatenumerate.md). Le descripteur doit être fermé avec la fonction [**MpHandleClose**](mphandleclose.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.

Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec. L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> </dl>

 

 





