---
title: Constantes de niveau d’emprunt d’identité (RpcDce. h)
description: Spécifie un niveau d’emprunt d’identité, qui indique la quantité d’autorité donnée au serveur lorsqu’il emprunte l’identité du client.
ms.assetid: ea5a3b46-b607-4192-a3cc-b2ec55ca94a6
topic_type:
- apiref
api_name:
- RPC_C_IMP_LEVEL_DEFAULT
- RPC_C_IMP_LEVEL_ANONYMOUS
- RPC_C_IMP_LEVEL_IDENTIFY
- RPC_C_IMP_LEVEL_IMPERSONATE
- RPC_C_IMP_LEVEL_DELEGATE
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbc4b4a74871eb111b778d798587e53027053fe57cc8cda837a3aafb7c24d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048487"
---
# <a name="impersonation-level-constants"></a>Constantes de niveau d’emprunt d’identité

Spécifie un niveau d’emprunt d’identité, qui indique la quantité d’autorité donnée au serveur lorsqu’il emprunte l’identité du client.



| Constante/valeur                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_IMP_LEVEL_DEFAULT"></span><span id="rpc_c_imp_level_default"></span><dl> <dt>**RPC \_ C \_ IMP \_ niveau \_ par défaut**</dt> <dt>0</dt> </dl>             | DCOM peut choisir le niveau d’emprunt d’identité à l’aide de son algorithme de négociation permanente de sécurité normal. Pour plus d’informations, consultez [négociation de sécurité globale](security-blanket-negotiation.md).<br/>                                                                                                                                                                                                                                                                           |
| <span id="RPC_C_IMP_LEVEL_ANONYMOUS"></span><span id="rpc_c_imp_level_anonymous"></span><dl> <dt>**RPC \_ C \_ IMP \_ niveau \_ anonymous**</dt> <dt>1</dt> </dl>       | Le client est anonyme au serveur. Le processus serveur peut emprunter l’identité du client, mais le jeton d’emprunt d’identité ne contient aucune information et ne peut pas être utilisé.<br/>                                                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_IMP_LEVEL_IDENTIFY"></span><span id="rpc_c_imp_level_identify"></span><dl> <dt>**RPC \_ C \_ IMP \_ niveau \_ identifier**</dt> <dt>2</dt> </dl>          | Le serveur peut obtenir l’identité du client. Le serveur peut emprunter l’identité du client pour la vérification de la liste de contrôle d’accès, mais il ne peut pas accéder aux objets système en tant que client. <br/>                                                                                                                                                                                                                                                                                                               |
| <span id="RPC_C_IMP_LEVEL_IMPERSONATE"></span><span id="rpc_c_imp_level_impersonate"></span><dl> <dt>**RPC \_ C \_ IMP \_ Level \_ emprunte**</dt> <dt>3</dt> </dl> | Le processus serveur peut emprunter l’identité du contexte de sécurité du client tout en agissant pour le compte du client. Ce niveau d’emprunt d’identité peut être utilisé pour accéder aux ressources locales telles que les fichiers. Lorsque vous empruntez l’identité à ce niveau, le jeton d’emprunt d’identité ne peut être transmis que sur une limite d’ordinateur. Le service d’authentification [Schannel](schannel.md) prend uniquement en charge ce niveau d’emprunt d’identité. <br/>                                                                      |
| <span id="RPC_C_IMP_LEVEL_DELEGATE"></span><span id="rpc_c_imp_level_delegate"></span><dl> <dt>**RPC \_ C \_ IMP \_ niveau \_ délégué**</dt> <dt>4</dt> </dl>          | Le processus serveur peut emprunter l’identité du contexte de sécurité du client tout en agissant pour le compte du client. Le processus serveur peut également effectuer des appels sortants à d’autres serveurs tout en agissant pour le compte du client, à l’aide du masquage. Le serveur peut utiliser le contexte de sécurité du client sur d’autres ordinateurs pour accéder aux ressources locales et distantes en tant que client. Lorsque vous empruntez l’identité à ce niveau, le jeton d’emprunt d’identité peut être transmis sur un nombre quelconque de limites de l’ordinateur.<br/> |



## <a name="remarks"></a>Remarques

[**GetUserName**](/windows/desktop/api/winbase/nf-winbase-getusernamea) échoue lors de l’emprunt d’identité au niveau de l’identité. La solution de contournement consiste à emprunter l’identité, à appeler [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken), à rétablir, à appeler [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation)et enfin à appeler [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). À l’aide de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), le client définit le niveau d’emprunt d’identité

À l’aide de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), le client définit le niveau d’emprunt d’identité et l’identité du proxy qui seront disponibles lorsqu’un serveur appelle [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient). L’identité que le serveur verra lorsque l’emprunt d’identité a lieu est décrite dans [masquage](cloaking.md). Notez que lorsque vous effectuez un appel en empruntant une identité, l’appelé reçoit normalement le jeton de processus de l’appelant, et non le jeton d’emprunt d’identité de l’appelant. Pour recevoir le jeton d’emprunt d’identité de l’appelant, l’appelant doit activer le masquage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>RpcDce. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Masquer](cloaking.md)
</dt> </dl>

 

