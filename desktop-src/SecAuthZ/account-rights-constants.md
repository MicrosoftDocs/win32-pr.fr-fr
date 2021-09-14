---
description: Les droits de compte déterminent le type d’ouverture de session qu’un compte d’utilisateur peut effectuer. Un administrateur attribue des droits de compte à des comptes d’utilisateurs et de groupes. Les droits de compte de chaque utilisateur incluent ceux octroyés à l’utilisateur et aux groupes auxquels l’utilisateur appartient.
ms.assetid: 42139d33-2d56-4d29-998f-5512bb795d44
title: Constantes de droits de compte (Ntsecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b16b75af89773df969ec78b771986b0a73dfb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013743"
---
# <a name="account-rights-constants"></a>Constantes de droits de compte

Les droits de compte déterminent le type d’ouverture de session qu’un compte d’utilisateur peut effectuer. Un administrateur attribue des droits de compte à des comptes d’utilisateurs et de groupes. Les droits de compte de chaque utilisateur incluent ceux octroyés à l’utilisateur et aux groupes auxquels l’utilisateur appartient.

Un administrateur système peut utiliser les fonctions de l' [*autorité de sécurité locale*](/windows/desktop/SecGloss/l-gly) (LSA) pour travailler avec les droits de compte. Les fonctions [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) et [**LsaRemoveAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaremoveaccountrights) ajoutent ou suppriment des droits de compte d’un compte. La fonction [**LsaEnumerateAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountrights) énumère les droits de compte détenus par un compte spécifié. La fonction [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright) énumère les comptes qui contiennent un droit de compte spécifié.

Les constantes de compte suivantes permettent de contrôler la capacité d’ouverture de session d’un compte. Les fonctions [**LogonUser**](/windows/desktop/api/winbase/nf-winbase-logonusera) ou [**LsaLogonUser**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser) échouent si le compte en cours de connexion ne dispose pas des droits de compte requis pour le type d’ouverture de session en cours d’exécution.



| Constante/valeur                                                                                                                                                                                                                                                                                                                           | Description                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| <span id="SE_BATCH_LOGON_NAME"></span><span id="se_batch_logon_name"></span><dl> <dt>**se \_ Texte \_ du \_ nom d’ouverture de session par lot**</dt> <dt>(« SeBatchLogonRight »)</dt> </dl>                                                                         | Requis pour qu’un compte se connecte à l’aide du type d’ouverture de session par lot.<br/>                               |
| <span id="SE_DENY_BATCH_LOGON_NAME"></span><span id="se_deny_batch_logon_name"></span><dl> <dt>**se \_ REFUSER \_ le \_ \_ nom d’ouverture de session par lot**</dt> <dt>(« SeDenyBatchLogonRight »)</dt> </dl>                                                     | Refuse explicitement à un compte le droit d’ouvrir une session à l’aide du type de connexion par lot.<br/>                |
| <span id="SE_DENY_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_interactive_logon_name"></span><dl> <dt>**se \_ REFUSER le texte du \_ \_ \_ nom d’ouverture de session interactive**</dt> <dt>(« SeDenyInteractiveLogonRight »)</dt> </dl>                             | Refuse explicitement à un compte le droit d’ouvrir une session à l’aide du type d’ouverture de session interactive.<br/>          |
| <span id="SE_DENY_NETWORK_LOGON_NAME"></span><span id="se_deny_network_logon_name"></span><dl> <dt>**se \_ REFUSER \_ le \_ \_ nom d’ouverture de session réseau**</dt> <dt>(« SeDenyNetworkLogonRight »)</dt> </dl>                                             | Refuse explicitement à un compte le droit d’ouvrir une session à l’aide du type d’ouverture de session réseau.<br/>              |
| <span id="SE_DENY_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_deny_remote_interactive_logon_name"></span><dl> <dt>**se \_ REFUSER le texte du \_ \_ \_ \_ nom d’ouverture de session interactive à distance**</dt> <dt>(« SeDenyRemoteInteractiveLogonRight »)</dt> </dl> | Refuse explicitement à un compte le droit d’ouvrir une session à distance à l’aide du type d’ouverture de session interactive.<br/> |
| <span id="SE_DENY_SERVICE_LOGON_NAME"></span><span id="se_deny_service_logon_name"></span><dl> <dt>**se \_ REFUSER \_ le \_ \_ nom d’ouverture de session du service**</dt> <dt>(« SeDenyServiceLogonRight »)</dt> </dl>                                             | Refuse explicitement à un compte le droit d’ouvrir une session à l’aide du type d’ouverture de session du service.<br/>              |
| <span id="SE_INTERACTIVE_LOGON_NAME"></span><span id="se_interactive_logon_name"></span><dl> <dt>**se \_ Texte \_ du \_ nom d’ouverture de session interactive**</dt> <dt>(« SeInteractiveLogonRight »)</dt> </dl>                                                 | Requis pour qu’un compte se connecte à l’aide du type d’ouverture de session interactive.<br/>                         |
| <span id="SE_NETWORK_LOGON_NAME"></span><span id="se_network_logon_name"></span><dl> <dt>**se \_ Texte \_ du \_ nom d’ouverture de session réseau**</dt> <dt>(« SeNetworkLogonRight »)</dt> </dl>                                                                 | Requis pour qu’un compte se connecte à l’aide du type d’ouverture de session réseau.<br/>                             |
| <span id="SE_REMOTE_INTERACTIVE_LOGON_NAME"></span><span id="se_remote_interactive_logon_name"></span><dl> <dt>**se \_ Texte \_ du \_ \_ nom d’ouverture de session interactive à distance**</dt> <dt>(« SeRemoteInteractiveLogonRight »)</dt> </dl>                     | Requis pour qu’un compte se connecte à distance à l’aide du type d’ouverture de session interactive.<br/>                |
| <span id="SE_SERVICE_LOGON_NAME"></span><span id="se_service_logon_name"></span><dl> <dt>**se \_ Texte \_ du \_ nom d’ouverture de session du service**</dt> <dt>(« SeServiceLogonRight »)</dt> </dl>                                                                 | Requis pour qu’un compte se connecte à l’aide du type d’ouverture de session du service.<br/>                             |



## <a name="remarks"></a>Notes

les \_ droits de refus SE remplacent les droits de compte correspondants. un administrateur peut attribuer un SE \_ refuser le droit à un compte pour remplacer les droits d’ouverture de session qu’un compte peut avoir en raison d’une appartenance à un groupe. par exemple, vous pouvez attribuer le \_ \_ nom d’ouverture de session réseau SE \_ à tout le monde, mais attribuer le \_ \_ \_ nom d’ouverture de session réseau SE refuser \_ le droit aux administrateurs d’empêcher l’administration à distance des ordinateurs.

Toutes les fonctions LSA mentionnées dans la présentation ci-dessus prennent en charge les droits et [privilèges](privilege-constants.md)de compte. Toutefois, contrairement aux privilèges, les droits de compte ne sont pas pris en charge par les fonctions [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) et [**LookupPrivilegeName**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegenamea) . La fonction [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) obtiendra des informations sur les droits de compte si tokenGroups, et non TokenPrivileges, est spécifié comme valeur du paramètre *TokenInformationClass* .

Les constantes droites de compte précédentes sont définies en tant que chaînes dans Ntsecapi. h. par exemple, la SE \_ \_ constante de nom d’ouverture de session INTERACTIVE \_ est définie comme « SeInteractiveLogonRight ».

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Ntsecapi. h</dt> </dl> |



 

