---
description: Valeurs HRESULT personnalisées pour l’interface de capture Graphics Diagnostics.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Énumération HRESULT
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c8b84b19be8de91f8f45ca5f6e8765035e75ebf67cade80a2d94faaf95ce2676
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981689"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span id="vspixengine.hresult"></span>Énumération HRESULT

Valeurs HRESULT personnalisées pour l’interface de capture Graphics Diagnostics.

## <a name="syntax"></a>Syntaxe


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ OK**  
HRESULT commun qui indique que l’opération a réussi comme prévu.

<span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ faux**  
HRESULT commun qui indique que l’opération a réussi, mais d’une manière différente de celle attendue.

<span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_fichier d’erreur pix \_ \_ \_ introuvable**  
HRESULT personnalisé qui est \_ \_ introuvable dans le fichier d’erreur renvoie \_ .

<span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**erreur PIX- \_ \_ environnement incorrect \_**  
HRESULT personnalisé qui renvoie l’erreur de l' \_ environnement est incorrect \_ .

<span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_ \_ format incorrect de l’erreur pix \_**  
HRESULT personnalisé qui renvoie le \_ format incorrect de l’erreur \_ .

<span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**\_violation de \_ partage d’erreurs pix \_**  
HRESULT personnalisé qui renvoie une violation de partage d’erreur \_ \_ .

<span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**\_disque d’erreur pix \_ \_ plein**  
HRESULT personnalisé qui renvoie le disque d’erreur \_ \_ saturé.

<span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**\_erreur pix \_ - \_ données supplémentaires**  
HRESULT personnalisé qui renvoie une erreur \_ plus de \_ données.

<span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_stratégie de \_ \_ Kits de débogage manquants dans \_ pix E \_**  
HRESULT personnalisé qui indique que la stratégie de kits de débogage est manquante.

<span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX \_ E \_ version non valide \_**  
HRESULT personnalisé qui indique qu’une version non valide est utilisée.

<span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ utilisant \_ DCOMP**  
HRESULT personnalisé qui indique que DirectComposition est en cours d’utilisation (la capture de DirectComposition n’est pas prise en charge.)

<span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ à l’aide de \_ DIRECTWRITE**  
HRESULT personnalisé qui indique que DirectWrite est en cours d’utilisation (la capture de DirectWrite n’est pas prise en charge.)

<span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ utilisant \_ d3d9**  
HRESULT personnalisé qui indique que le Direct3D9 est en cours d’utilisation (la capture de Direct3D9 n’est pas prise en charge dans Windows 10.)

<span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX \_ E \_ Impossible de \_ créer un \_ nuanceur**  
HRESULT personnalisé qui indique qu’un nuanceur spécifié ne peut pas être créé.

<span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ utilisant \_ D2D**  
HRESULT personnalisé qui indique que Direct2D est en cours d’utilisation (la capture de Direct2D n’est pas prise en charge.)

<span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**PIX \_ E \_ aucune \_ trame**  
HRESULT personnalisé qui indique qu’aucun frame n’a été capturé.

<span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ désactiver \_ Spy**  

<span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ sur \_ win7**  
HRESULT personnalisé qui indique qu’une Windows 8 vsglog ne peut pas être lue sur Windows 7.

<span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_trace du \_ \_ nuanceur de nuance pix E \_**  
HRESULT personnalisé qui indique qu’une erreur s’est produite lors de la création de la trace du nuanceur.

<span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**PIX \_ E \_ aucune \_ \_ visualisation des données cs \_**  
HRESULT personnalisé qui indique qu’il n’existe aucune visualisation des données de nuanceur de calcul.

<span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**\_SDK pix E \_ incompatibilité \_**  
HRESULT personnalisé qui indique qu’il existe une incompatibilité avec le kit de développement logiciel (SDK) actuel.

<span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**le \_ \_ Kit de \_ \_ développement logiciel (SDK) pix est possible**  
HRESULT personnalisé qui indique qu’il existe une discordance possible avec le kit de développement logiciel (SDK) actuel.

<span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIX \_ E \_ Pixel non détectable \_**  
HRESULT personnalisé qui indique qu’il existe un pixel non détectable.

<span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX \_ E ne pas \_ \_ déboguer le \_ nuanceur \_ à l’aide de la \_ sémantique de \_ valeur système \_**  
HRESULT personnalisé qui indique que le Sahder ne peut pas être débogué à l’aide de la sémantique de valeur système.

<span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX \_ S \_ UPDATEAVAILABLE**  
HRESULT personnalisé qui indique qu’une mise à jour est disponible.

<span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**État de dxgi PIX- \_ \_ \_ aucune \_ redirection**  
HRESULT personnalisé qui renvoie DXGI \_ Status \_ no \_ redirection.

<span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**État de dxgi PIX- \_ \_ \_ aucun \_ \_ accès au bureau**  
HRESULT personnalisé qui renvoie DXGI \_ Status \_ no \_ Desktop \_ Access.

<span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ image de la source VIDPN Graphics de l’État dxgi pix \_ \_ \_ en cours d' \_ utilisation**  
HRESULT personnalisé qui renvoie la \_ \_ source VIDPN Graphics dxgi status \_ \_ \_ \_ use.

<span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**\_mode d' \_ État dxgi pix \_ \_ modifié**  
HRESULT personnalisé qui renvoie le \_ mode d’État dxgi \_ \_ modifié.

<span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ modification du mode d’État dxgi pix \_ \_ en \_ cours**  
HRESULT personnalisé qui renvoie le \_ \_ mode d’État dxgi \_ change \_ en \_ cours.

<span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_État dxgi \_ pix \_ UNOCCLUDED**  
HRESULT personnalisé qui renvoie DXGI \_ Status \_ UNOCCLUDED.

<span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**État de PIX \_ dxgi le \_ \_ DDA \_ est \_ encore \_ en cours de dessin**  
HRESULT personnalisé sur lequel renvoie DXGI \_ Status \_ \_ a \_ encore été \_ dessiné.

<span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**\_NOTIMPL pix \_**  
HRESULT personnalisé qui renvoie E \_ NOTIMPL.

<span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ nointerface**  
HRESULT personnalisé qui renvoie E \_ nointerface.

<span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_pointeur pix E \_**  
HRESULT personnalisé qui renvoie pointeur E \_ .

<span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**\_abandonner pix \_**  
HRESULT personnalisé qui renvoie E \_ Abort.

<span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**échec de PIX \_ E \_**  
Un HRESULT personnalisé qui renvoie E \_ échoue.

<span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E \_ inattendu**  
HRESULT personnalisé qui renvoie E \_ inattendu.

<span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**\_ACCESSDENIED pix \_**  
HRESULT personnalisé qui renvoie E \_ ACCESSDENIED.

<span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**\_handle pix E \_**  
HRESULT personnalisé qui renvoie E \_ .

<span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**\_OUTOFMEMORY pix \_**  
HRESULT personnalisé qui renvoie E \_ OUTOFMEMORY.

<span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**  
HRESULT personnalisé qui renvoie E \_ INVALIDARG.

<span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**\_disque d' \_ erreur Xbox pix \_ \_ plein**  
HRESULT personnalisé qui indique que le disque est plein.

<span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_adresse pix \_ WS \_ E \_ en cours d' \_ utilisation**  
HRESULT personnalisé qui indique que l’adresse est déjà utilisée.

<span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_stratégie des kits pix WS \_ E \_ manquant \_ \_**  
HRESULT personnalisé qui indique que l’adresse n’est pas disponible.

<span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**\_FAILEDTOLOADSOFTWAREMODULE pix \_**  
HRESULT personnalisé qui indique qu’un module logiciel nécessaire n’a pas pu se charger.

<span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**\_USEDSOFTWAREMODULETHATWASNTWARPORREF pix \_**  
HRESULT personnalisé qui indique que le module de logiciel utilisé n’était pas le pilote WARP ou REF.

<span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**\_CORRUPTEDFILE pix \_**  
HRESULT personnalisé qui indique que le fichier est endommagé.

<span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**\_FAILEDTOOPENFILE pix \_**  
HRESULT personnalisé qui indique que le fichier n’a pas pu s’ouvrir.

<span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**\_CALLFAILEDONPLAYBACK pix \_**  
HRESULT personnalisé qui indique qu’un appel a échoué lors de la lecture.

<span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**\_UNKNOWNUUID pix \_**  
HRESULT personnalisé qui indique qu’un UUID inconnu a été rencontré ; Cela ne doit jamais se produire.

<span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**\_NOTCAPTUREFILEORCORRUPTED pix \_**  
HRESULT personnalisé qui indique que le fichier n’est pas un fichier de capture ou est endommagé.

<span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**\_NEWERFILE pix \_**  

<span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**\_OLDERFILE pix \_**  

<span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**\_INVALIDMOMENT pix \_**  

<span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**lecteur PIX- \_ \_ pilote incorrect \_**  
HRESULT personnalisé qui indique que le pilote est incorrect.

<span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**\_erreur pix \_ Impossible \_ \_ d’accéder \_ à DEPTHSTENCIL dans le \_ processeur**  
HRESULT personnalisé qui indique que l’UC a tenté d’accéder à la mémoire tampon du stencil de profondeur, provoquant une erreur.

<span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**\_erreur pix \_ Impossible de résoudre la \_ texture à \_ échantillonnages \_**  
HRESULT personnalisé qui indique qu’il y a eu une tentative de résolution d’une texture à échantillonnage multiple, provoquant une erreur.

<span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_erreur dxgi de l' \_ \_ appel non valide \_**  
HRESULT personnalisé qui renvoie DXGI \_ erreur d' \_ appel non valide \_ .

<span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_erreur dxgi \_ pix \_ \_ introuvable**  
HRESULT personnalisé qui renvoie DXGI \_ erreur \_ \_ introuvable.

<span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_erreur dxgi \_ de \_ plus \_ données dans pix**  
HRESULT personnalisé qui renvoie DXGI \_ erreur \_ plus de \_ données.

<span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**\_erreur dxgi \_ pix \_ non prise en charge**  
HRESULT personnalisé qui ne \_ \_ prend pas en charge l’erreur renvoie DXGI.

<span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**\_périphérique d' \_ erreur pix dxgi \_ \_ supprimé**  
HRESULT personnalisé qui renvoie l' \_ appareil d’erreur dxgi \_ \_ supprimé.

<span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**\_périphérique d' \_ erreur pix dxgi \_ \_ bloqué**  
HRESULT personnalisé qui renvoie le \_ blocage du périphérique d’erreur dxgi \_ \_ .

<span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**\_erreur de \_ \_ \_ réinitialisation de l’appareil pix dxgi**  
HRESULT personnalisé qui renvoie la \_ \_ réinitialisation de l’appareil d’erreur dxgi \_ .

<span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**l' \_ erreur dxgi pix \_ \_ est \_ encore en cours de \_ dessin**  
Un HRESULT personnalisé qui renvoie l' \_ erreur dxgi était encore en cours de \_ \_ \_ dessin.

<span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**\_statistiques de \_ trame d’erreur dxgi pix \_ \_ \_ disjointes**  
HRESULT personnalisé qui renvoie les \_ statistiques de \_ trame d’erreur dxgi \_ \_ disjointes.

<span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ source VIDPN d’erreur Graphics dxgi \_ \_ \_ en cours d' \_ utilisation**  
HRESULT personnalisé qui renvoie la \_ \_ source VIDPN Graphics Error dxgi \_ \_ \_ en cours d' \_ utilisation.

<span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ erreur interne du pilote d’erreur \_ pix dxgi \_**  
HRESULT personnalisé qui renvoie DXGI erreur \_ interne du pilote d’erreur \_ \_ \_ .

<span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**erreur de dxgi PIX non \_ \_ \_ exclusive**  
HRESULT personnalisé qui renvoie DXGI \_ erreur non \_ exclusive.

<span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**\_erreur de dxgi pix \_ \_ non \_ \_ disponible actuellement**  
HRESULT personnalisé qui renvoie DXGI \_ erreur \_ non \_ disponible actuellement \_ .

<span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**\_Erreur du \_ client distant pix dxgi \_ \_ \_ déconnectée**  
HRESULT personnalisé qui renvoie DXGI \_ erreur \_ \_ \_ déconnectée du client distant.

<span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_erreur dxgi \_ à distance de pix \_ \_ OUTOFMEMORY**  
HRESULT personnalisé qui renvoie DXGI \_ Error \_ OUTOFMEMORY à distance \_ .

<span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ modification du mode d’erreur dxgi pix \_ \_ en \_ cours**  
HRESULT personnalisé qui renvoie le \_ \_ mode d’erreur dxgi \_ change \_ en \_ cours.

<span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_erreur de \_ \_ perte d’accès dxgi \_ pix**  
HRESULT personnalisé qui renvoie \_ l’erreur d' \_ accès dxgi \_ .

<span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_ \_ \_ \_ délai d’attente d’erreur dxgi pix**  
HRESULT personnalisé qui renvoie l' \_ \_ \_ expiration du délai d’attente d’erreur DXGI.

<span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**\_session d’erreur pix dxgi \_ \_ \_ déconnectée**  
HRESULT personnalisé qui \_ \_ déconnecte la session d’erreur dxgi renvoie \_ .

<span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**\_ \_ erreur de dxgi pix pour la \_ \_ \_ sortie \_ obsolète**  
Un HRESULT personnalisé qui renvoie l' \_ erreur dxgi \_ limite \_ à la \_ sortie \_ obsolète.

<span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**l' \_ erreur dxgi pix \_ \_ ne peut pas \_ protéger le \_ contenu**  
Un HRESULT personnalisé qui renvoie l' \_ erreur dxgi \_ ne peut pas \_ protéger du \_ contenu.

<span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_ \_ \_ accès à l’erreur pix dxgi \_ refusé**  
HRESULT personnalisé qui renvoie \_ \_ l’accès à l’erreur dxgi \_ .

<span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**un \_ nom d’erreur dxgi pix \_ \_ \_ \_ existe déjà**  
Un HRESULT personnalisé qui renvoie \_ nom d’erreur dxgi \_ \_ \_ existe déjà.

<span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_composant du \_ Kit de \_ développement logiciel (SDK) pix dxgi \_ \_ manquant**  
HRESULT personnalisé qui est manquant dans le composant renvoie DXGI \_ Error \_ SDK \_ \_ .

<span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**PIX \_ dxgi \_ DDI \_ Err \_ WASSTILLDRAWING**  
HRESULT personnalisé qui renvoie DXGI \_ DDI \_ Err \_ WASSTILLDRAWING.

<span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**\_erreur dxgi \_ DDI \_ pix \_ non prise en charge**  
HRESULT personnalisé que renvoie DXGI \_ DDI Err n’est \_ \_ pas pris en charge.

<span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_ \_ erreur DDI dxgi DDI non \_ \_ exclusive**  
HRESULT personnalisé qui renvoie DXGI \_ DDI \_ Err non \_ exclusif.

<span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**Erreur de D3D10 PIX- \_ nombre d’objets d' \_ \_ \_ \_ État uniques trop nombreux \_ \_**  
HRESULT personnalisé qui renvoie D3D10 d' \_ un \_ trop \_ grand nombre d' \_ \_ objets d’État uniques \_ .

<span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_Fichier d' \_ erreur D3D10 pix \_ \_ \_ introuvable**  
HRESULT personnalisé qui renvoie fichier d' \_ erreur \_ D3D10 \_ \_ introuvable.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**Erreur de d3d11 PIX- \_ nombre d’objets d' \_ \_ \_ \_ État uniques trop nombreux \_ \_**  
HRESULT personnalisé qui renvoie D3D11 d' \_ un \_ trop \_ grand nombre d' \_ \_ objets d’État uniques \_ .

<span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_Fichier d' \_ erreur d3d11 pix \_ \_ \_ introuvable**  
HRESULT personnalisé qui renvoie fichier d' \_ erreur \_ d3d11 \_ \_ introuvable.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**\_Erreur d3d11 pix- \_ nombre d' \_ \_ \_ \_ objets de vue uniques trop nombreux \_**  
HRESULT personnalisé qui renvoie D3D11 \_ erreur \_ trop \_ nombreux objets de \_ \_ vue uniques \_ .

<span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**\_Erreur de \_ mappage de contexte différé d3d11 de pix \_ \_ \_ \_ sans \_ ignorer la première \_ fois**  
HRESULT personnalisé qui renvoie le \_ mappage de \_ contexte différé \_ d’erreur d3d11 \_ \_ sans \_ l' \_ annulation initiale.

<span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**erreur PIX bloqués de l' \_ \_ \_ appel de dessin \_**  
HRESULT personnalisé qui indique qu’un appel de dessin a été entièrement bloqués, provoquant une erreur.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



