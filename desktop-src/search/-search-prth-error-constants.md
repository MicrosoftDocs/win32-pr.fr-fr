---
description: 'Messages d’erreur retournés par les gestionnaires de protocole :'
ms.assetid: b5e99ad1-1698-483c-8173-796af33085c4
title: Rechercher des messages d’erreur du gestionnaire de protocole (searchapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4473e3e235641e5b4bb5d86313b4154cd00ec029fe96d42d8964dab51f33780f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969728"
---
# <a name="search-protocol-handler-error-messages"></a>Rechercher les messages d’erreur du gestionnaire de protocole

Messages d’erreur retournés par les gestionnaires de protocole :



| Constante/valeur                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PRTH_E_ACCESS_DENIED"></span><span id="prth_e_access_denied"></span><dl> <dt>**PRTH \_ \_Accès \_ refusé**</dt> <dt>0x80041205L</dt> </dl>             | L’accès a été refusé. Si cela se produit pendant une analyse incrémentielle, le fichier est supprimé de la file d’attente d’URL du Rassembleur.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_IS_READ_NONE"></span><span id="prth_e_acl_is_read_none"></span><dl> <dt>**PRTH \_ L' \_ ACL \_ est \_ Read \_ None**</dt> <dt>0x80041211L</dt> </dl>  | L’élément ne sera pas indexé. Sa liste de contrôle d’accès ne permet pas de lire l’élément.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="PRTH_E_ACL_TOO_BIG"></span><span id="prth_e_acl_too_big"></span><dl> <dt>**PRTH \_ Liste de contrôle d’accès E/0x80041212L \_ \_ trop \_ volumineuse**</dt> <dt></dt> </dl>                  | Liste de contrôle d’accès dépassant 64 Ko. La recherche n’indexe pas l’élément.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_BAD_REQUEST"></span><span id="prth_e_bad_request"></span><dl> <dt>**PRTH \_ E 0x80041208L de \_ \_ requête incorrecte**</dt> <dt></dt> </dl>                   | La requête n’était pas valide en raison d’une erreur dans l’URL.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="PRTH_E_COMM_ERROR"></span><span id="prth_e_comm_error"></span><dl> <dt>**PRTH \_ \_ \_ Erreur comm**</dt> . <dt>0x80041200L</dt> </dl>                      | Indique une erreur de communication ou de serveur. Si le nombre de ces erreurs est trop important pour un serveur particulier, le rassembleur marque le serveur comme étant non disponible.<br/>                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_NOT_REDIRECTED"></span><span id="prth_e_not_redirected"></span><dl> <dt>**PRTH \_ E \_ non \_ Redirigé**</dt> <dt>0x80041207L</dt> </dl>          | L’URL redirigée n’existe pas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_E_OBJ_NOT_FOUND"></span><span id="prth_e_obj_not_found"></span><dl> <dt>**PRTH \_ \_Obj E \_ non \_ trouvé**</dt> <dt>0x80041201L</dt> </dl>            | Objet introuvable. Indique que le rassembleur doit supprimer le document de la file d’attente s’il est introuvable au cours d’une analyse incrémentielle.<br/>                                                                                                                                                                                                                                                                                          |
| <span id="PRTH_E_REQUEST_ERROR"></span><span id="prth_e_request_error"></span><dl> <dt>**PRTH \_ \_ \_ Erreur de requête E**</dt> <dt>0x80041202L</dt> </dl>             | Les options utilisées ne sont pas prises en charge.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="PRTH_E_SERVER_ERROR"></span><span id="prth_e_server_error"></span><dl> <dt>**PRTH \_ \_ \_ Erreur de serveur**</dt> <dt>0x80041206L</dt> </dl>                | Erreur de communication ou de serveur. Si le nombre de ces erreurs est trop important pour un serveur particulier, le rassembleur marque le serveur comme étant non disponible.<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PRTH_S_NOT_ALL_PARTS"></span><span id="prth_s_not_all_parts"></span><dl> <dt>**PRTH \_ \_Ne pas \_ tous les \_ composants**</dt> <dt>0x8004121BL</dt> </dl>            | Impossible d’accéder aux parties d’un élément.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="PRTH_S_NOT_MODIFIED"></span><span id="prth_s_not_modified"></span><dl> <dt>**PRTH \_ 0x00041203L \_ non \_ modifié**</dt> <dt></dt> </dl>                | Le contenu de l’élément n’a pas changé. Si cette erreur se produit pendant une analyse incrémentielle, le rassembleur ignore cet élément, car l’élément n’a pas été modifié.<br/>                                                                                                                                                                                                                                                                                   |
| <span id="PRTH_S_TRY_IMPERSONATING"></span><span id="prth_s_try_impersonating"></span><dl> <dt>**PRTH \_ \_Essayer d' \_ emprunter l’identité**</dt> de <dt>0x00041225L</dt> </dl> | L’élément doit être accessible en usurpant l’identité d’un utilisateur. Le gestionnaire de protocole est supposé implémenter [**IUrlAccessor3 :: GetImpersonationSidBlobs**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor3-getimpersonationsidblobs) afin que l’hôte de protocole de recherche puisse récupérer une liste de sid à utiliser pour l’emprunt d’identité et peut revenir à l’utilisation de [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2), en empruntant l’identité de l’un des utilisateurs autorisés lors de l’ouverture de l’élément. <br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec SP2, Windows les \[ applications de bureau Vista uniquement\]<br/>                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                            |
| En-tête<br/>                   | <dl> <dt>Searchapi. h</dt> </dl> |



 

 




