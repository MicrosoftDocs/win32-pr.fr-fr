---
title: MpUpdateStart, fonction (MpClient. h)
description: Démarre une opération de mise à jour de signature.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- fonctionnalités d’environnement Windows hérités de la fonction MpUpdateStart
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a61cda213ecfbb23c9ef366fcce7b5c91e806f26f0f4ebe8b45dc596b63d1b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975889"
---
# <a name="mpupdatestart-function"></a>MpUpdateStart fonction)

Démarre une opération de mise à jour de signature.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMpHandle* \[ dans\]
</dt> <dd>

Type : **MPHANDLE**

Handle de l’interface du gestionnaire de protection contre les programmes malveillants. Ce descripteur est retourné par la fonction [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*dwUpdateOptions* \[ dans\]
</dt> <dd>

Type : **DWORD**

Spécifie l’option pour l’opération de mise à jour des signatures. Ce peut être l’une des valeurs suivantes :



| Valeur                                                                                                                                                                                              | Signification                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <dt>**\_option mise à jour \_ None**</dt> </dl>                | Aucune option spécifique n’est demandée.<br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <dt>**\_option mise à jour \_ Async**</dt> </dl>             | L’opération de mise à jour doit être asynchrone, où **MpUpdateStart** retourne immédiatement après l’initialisation réussie de la mise à jour de la signature. (Par défaut, l’opération de mise à jour est synchrone, ce qui signifie que **MpUpdateStart** retournera uniquement une fois la mise à jour de signature terminée.)<br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <dt>**progression de l' \_ option mise à jour \_**</dt> </dl>    | L’appelant souhaite recevoir des informations de progression de mise à jour de signature via un rappel.<br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <dt>**\_option mise à jour \_ http**</dt> </dl>                | La mise à jour de signature est effectuée en téléchargeant le package de signature complète à partir du site portail de sécurité Microsoft. Cela peut être utilisé comme option de secours si le client rencontre un problème de téléchargement de signature via Microsoft Update.<br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <dt>**\_option mise à jour \_ UNC**</dt> </dl>                   | Effectue une mise à jour de signature à l’aide du téléchargement direct à partir de partages UNC.<br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <dt>**\_option mise à jour \_ gérée**</dt> </dl>       | Effectue une mise à jour de signature à l’aide du service managé WSUS.<br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <dt>**\_option mise à jour \_ non gérée**</dt> </dl> | Effectue une mise à jour de signature à l’aide du service non managé MU/WU.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

*pCallbackInfo* \[ dans, facultatif\]
</dt> <dd>

Type : **PMPCALLBACK \_ info**

Pointeur vers les informations de rappel utilisées pour alimenter le client avec les modifications de l’état de mise à jour de signature (telles que le début et la fin) et les informations de progression. Les [**\_ données MPCALLBACK**](mpcallback-data.md) retournées dans la fonction de rappel signalent l’état de mise à jour réel et les informations relatives à la progression. La liste suivante répertorie les rappels possibles :



| Valeur                                                                                                                                                                                                                                | Signification                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ Start**</dt> </dl>                                      | L’opération de mise à jour a démarré.<br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ terminé**</dt> </dl>                             | Opération de mise à jour terminée.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <dt>**début de la \_ recherche MPNOTIFY SIGUPDATE \_ \_**</dt> </dl>                | Recherche des mises à jour démarrées.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <dt>**recherche de MPNOTIFY \_ SIGUPDATE \_ \_ terminée**</dt> </dl>       | Recherche des mises à jour terminées. Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <dt>**démarrage du téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>          | Téléchargement de la mise à jour démarré.<br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <dt>**progression du téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl> | Télécharger les informations de progression. Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <dt>**Téléchargement de MPNOTIFY \_ SIGUPDATE \_ \_ terminé**</dt> </dl> | Téléchargement pour la mise à jour terminée. Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <dt>**démarrage de l’installation de MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>             | L’installation de la mise à jour a démarré.<br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <dt>**progression de l’installation de MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>    | Informations de progression de l’installation. Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <dt>**installation de MPNOTIFY \_ SIGUPDATE \_ \_ terminée**</dt> </dl>    | Installation de la mise à jour terminée. Des informations supplémentaires sont disponibles via la structure de [**\_ données MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <dt>**\_requête MPNOTIFY \_ SIGUPDATE \_ traitée**</dt> </dl> | Le service anti-programme malveillant a traité une demande de mise à jour de signature. L’échec ou la réussite est indiqué par *HRESULT* dans les [**\_ données de MPCALLBACK**](mpcallback-data.md).<br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <dt>**redémarrage de MPNOTIFY \_ SIGUPDATE \_ \_ requis**</dt> </dl>       | Nécessite un redémarrage pour terminer l’opération de mise à jour. L’échec ou la réussite est indiqué par *HRESULT* dans les [**\_ données de MPCALLBACK**](mpcallback-data.md).<br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**\_échec interne \_ MPNOTIFY**</dt> </dl>                                   | L’opération de mise à jour de signature a rencontré un échec générique. Le *HRESULT* dans [**les \_ données MPCALLBACK**](mpcallback-data.md) contient le code d’erreur spécifique.<br/>    |



 

</dd> <dt>

*phUpdateHandle* \[ à\]
</dt> <dd>

Type : **PMPHANDLE**

Handle de mise à jour retourné qui identifie l’opération de mise à jour de signature actuellement lancée. Ce handle peut être utilisé dans les appels de fonction suivants, par exemple, pour contrôler l’opération de mise à jour de signature. Le descripteur doit être fermé avec la fonction [**MpHandleClose**](mphandleclose.md) .

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

[**\_données MPSIGUPDATE**](mpsigupdate-data.md)
</dt> </dl>

 

 





