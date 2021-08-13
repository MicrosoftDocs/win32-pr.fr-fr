---
title: MpScanStart, fonction (MpClient. h)
description: Démarre une opération d’analyse.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- fonctionnalités d’environnement Windows hérités de la fonction MpScanStart
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34d56f6814ecdd13b2db4f698e8cc122d4d15e325bda17d82d56a5796d8590fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450239"
---
# <a name="mpscanstart-function"></a>MpScanStart fonction)

Démarre une opération d’analyse.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMpHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle de l’interface du gestionnaire de protection contre les programmes malveillants. Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*ScanType* \[ dans\]
</dt> <dd>

Type : **[ **MPSCAN \_**](mpscan-type.md)**

Spécifie le type d’analyse. Ce paramètre doit être l’un des membres du [**\_ type MPSCAN**](mpscan-type.md) enueration.

</dd> <dt>

*dwScanOptions* \[ dans\]
</dt> <dd>

Type : **DWORD**

Spécifie différentes options pour l’opération d’analyse.



| Valeur                                                                                                                                                                                                       | Signification                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <dt>**\_option MPSCAN \_ None**</dt> </dl>                               | Aucune option spécifique n’est demandée.<br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <dt>**\_option MPSCAN \_ Async**</dt> </dl>                            | L’opération d’analyse doit être asynchrone, où **MpScanStart** retourne immédiatement après l’initialisation réussie de l’analyse. (Par défaut, l’opération d’analyse est synchrone, ce qui signifie que **MpScanStart** ne retournera qu’une fois l’analyse terminée.)<br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <dt>**progression de l' \_ option MPSCAN \_**</dt> </dl>                   | L’appelant souhaite recevoir des informations sur la progression de l’analyse via un rappel.<br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <dt>**\_option MPSCAN \_ LOWPRIORITY**</dt> </dl>          | Effectuez l’analyse avec une priorité basse. (Par défaut, l’opération d’analyse est effectuée avec une priorité normale.)<br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <dt>**\_option MPSCAN \_ PACKEDEXES**</dt> </dl>             | Analyser les exécutables empaquetés pour détecter les menaces potentielles.<br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <dt>**\_Archives des options MPSCAN \_**</dt> </dl>                   | Analyser le contenu de l’Archive pour identifier les menaces potentielles. Les archives sont des fichiers avec des extensions telles que .zip, .cab ou. tar.<br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <dt>**\_heuristique des options MPSCAN \_**</dt> </dl>             | Activez l’analyse heuristique. Cela permet de rechercher les menaces dont le type de détection est défini sur heuristiques.<br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <dt>**\_option MPSCAN \_ REPORTFRIENDLY**</dt> </dl> | Signaler les éléments conviviaux dans une analyse des ressources. Cela est destiné à un usage interne uniquement.<br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <dt>**\_option MPSCAN \_ REPORTUNKNOWN**</dt> </dl>    | Signaler les éléments inconnus dans une analyse des ressources. Cela est destiné à un usage interne uniquement.<br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <dt>**\_option MPSCAN \_ noconsolide**</dt> </dl>    | Ne Consolidez pas les résultats de l’analyse avec la vue globale des menaces. Cela est utile pour un client (tel qu’un client de messagerie) qui souhaite contrôler le nettoyage de l’expérience utilisateur par lui-même plutôt que d’autoriser l’expérience utilisateur de nettoyage anti-programme malveillant par défaut. Cela est destiné à un usage interne uniquement.<br/> |



 

</dd> <dt>

*pScanResources* \[ dans, facultatif\]
</dt> <dd>

Type : **\_ ressources PMPSCAN**

Pointeur vers les informations sur les ressources d’analyse. Ce paramètre doit avoir la **valeur null** pour une analyse rapide. Il s’agit d’un paramètre facultatif pour une analyse complète. Pour une analyse de ressource, ce paramètre doit être spécifié avec au moins une structure d’informations sur les ressources. Pour analyser des ressources spécifiques, l’appelant doit disposer de l’autorisation de **\_ lecture générique** pour la ressource. Consultez [**\_ ressources MPSCAN**](mpscan-resources.md).

</dd> <dt>

*pCallbackInfo* \[ dans, facultatif\]
</dt> <dd>

Type : **PMPCALLBACK \_ info**

Pointeur vers les informations de rappel utilisées pour alimenter le client avec les modifications de l’état d’analyse (par exemple, Start et Complete) et les informations de progression. Les [**\_ données MPCALLBACK**](mpcallback-data.md) retournées dans la fonction de rappel signalent l’état d’analyse réel et les informations relatives à la progression. La liste suivante répertorie les rappels possibles :



| Valeur                                                                                                                                                                                                       | Signification                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <dt>**début de l' \_ analyse MPNOTIFY \_**</dt> </dl>                            | L’opération d’analyse a démarré.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <dt>**\_analyse MPNOTIFY \_ terminée**</dt> </dl>                   | L’opération d’analyse est terminée. Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <dt>**\_analyse MPNOTIFY \_ suspendue**</dt> </dl>                         | L’opération d’analyse est suspendue.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <dt>**\_analyse MPNOTIFY \_ reprise**</dt> </dl>                      | L’opération d’analyse a repris de la suspension.<br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <dt>**annulation de l' \_ analyse MPNOTIFY \_**</dt> </dl>                         | L’opération d’analyse a été annulée.<br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <dt>**progression de l' \_ analyse MPNOTIFY \_**</dt> </dl>                   | Analyser les informations de progression. Des informations supplémentaires (telles que les statistiques sur les ressources) sont disponibles via la structure de [**\_ données MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <dt>**\_erreur d’analyse MPNOTIFY \_**</dt> </dl>                            | Analyser les informations d’erreur pour une ressource spécifique. Les informations de ressource spécifiques sont disponibles via la structure de [**\_ données MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <dt>**\_analyse MPNOTIFY \_ infectée**</dt> </dl>                   | L’analyse a trouvé une ressource infectée. Notez que, dans la plupart des cas, cela entraînera une menace signalée à la fin de l’analyse. Parfois, il ne peut pas se matérialiser comme une menace en raison d’exclusions. Des informations supplémentaires sur les ressources infectées sont disponibles via la structure de [**\_ données MPSCAN**](mpscan-data.md) .<br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <dt>**MPNOTIFY \_ Scan \_ MEMORYSTART**</dt> </dl>          | La partie analyse rapide de la totalité de l’analyse a démarré.<br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <dt>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**</dt> </dl> | La partie analyse rapide de l’analyse complète est terminée.<br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**\_échec interne \_ MPNOTIFY**</dt> </dl>          | L’opération d’analyse a rencontré un échec générique. Le *HRESULT* dans [**les \_ données MPCALLBACK**](mpcallback-data.md) contient le code d’erreur spécifique.<br/>                                                                                                                                                                   |



 

</dd> <dt>

*phScanHandle* \[ à\]
</dt> <dd>

Type : **PMPHANDLE**

Handle d’analyse retourné qui identifie l’analyse actuellement lancée. Ce handle peut être utilisé dans les appels de fonction suivants, par exemple pour récupérer un résultat d’analyse. Le descripteur doit être fermé avec la fonction [**MpHandleClose**](mphandleclose.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si la fonction s’exécute correctement, la valeur de retour est **\_ OK**.

Si la fonction échoue, la valeur de retour est un code **HRESULT** en échec. L’appelant peut utiliser la fonction [**MpErrorMessageFormat**](mperrormessageformat.md) pour obtenir une description générique du message d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                    |
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

[**\_données MPCALLBACK**](mpcallback-data.md)
</dt> <dt>

[**\_données MPSCAN**](mpscan-data.md)
</dt> <dt>

[**\_ressources MPSCAN**](mpscan-resources.md)
</dt> <dt>

[**\_type MPSCAN**](mpscan-type.md)
</dt> </dl>

 

 





