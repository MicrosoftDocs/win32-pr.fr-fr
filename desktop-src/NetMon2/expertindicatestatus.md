---
description: La fonction ExpertIndicateStatus indique le pourcentage d’achèvement de l’analyse des experts du fichier de capture.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: ExpertIndicateStatus, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009344"
---
# <a name="expertindicatestatus-function"></a>ExpertIndicateStatus fonction)

La fonction **ExpertIndicateStatus** indique le pourcentage d’achèvement de l’analyse du fichier de capture par l’expert.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hExpertKey* \[ dans\]
</dt> <dd>

Identificateur d’expert unique. Moniteur réseau transmet *hExpertKey* à l’expert lorsqu’il appelle la fonction [Run](run.md) .

</dd> <dt>

*État* \[ dans\]
</dt> <dd>

État actuel de l’analyse. Spécifiez l’une des valeurs [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) suivantes.



| Valeur                                                                                                                                                                                 | Signification                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**EXPERTSTATUS \_ inactif**</dt> </dl> | L’expert n’a jamais démarré. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**début de EXPERTSTATUS \_**</dt> </dl> | L’expert démarre. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**EXPERTSTATUS \_ en cours d’exécution**</dt> </dl>    | L’expert s’exécute normalement. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**\_problème EXPERTSTATUS**</dt> </dl>    | Un problème spécifié dans le paramètre SubStatus A arrêté l’expert. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**EXPERTSTATUS \_ abandonné**</dt> </dl>    | Moniteur réseau arrêté l’expert. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**EXPERTSTATUS \_ terminé**</dt> </dl>             | L’expert a terminé l’analyse. <br/>                     |



 

</dd> <dt>

Sous- *État* \[ dans\]
</dt> <dd>

Extension ou clarification des informations fournies par le paramètre *Status* .

</dd> <dt>

*szText* \[ dans\]
</dt> <dd>

Indicateur d’État Text facultatif.

La valeur de ce paramètre peut être **null**.

</dd> <dt>

*PercentDone* \[ à\]
</dt> <dd>

Pourcentage des données de capture traitées par l’expert.

Lorsque l’expert termine l’analyse d’un fichier de capture, le système définit le pourcentage sur 100. Toute valeur supérieure à 99 sera ignorée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est NMERR \_ expert \_ Terminate ; l’expert doit immédiatement nettoyer et retourner sans terminer la capture.

## <a name="remarks"></a>Remarques

La fonction **ExpertIndicateStatus** peut uniquement être appelée par des experts qui implémentent la fonction [exécuter](run.md) ou [configurer](configure.md) l’exportation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
