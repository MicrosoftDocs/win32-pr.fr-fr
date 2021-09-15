---
title: AppIDFlags
description: Jeu d’indicateurs qui contrôlent le comportement d’activation d’un serveur COM.
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- Valeur de Registre AppIDFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdad2b80625d6a60460d43f242d7897e0ae7eb40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524989"
---
# <a name="appidflags"></a>AppIDFlags

Jeu d’indicateurs qui contrôlent le comportement d’activation d’un serveur COM.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **Registre \_ DWORD** .



| Valeur de l’indicateur | Constante                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ activer \_ IUSERVER \_ indesktop          |
| 0x2        | APPIDREGFLAGS \_ \_ \_ \_ SD \_ et \_ Bind du processus de serveur sécurisé |
| 0x4        | APPIDREGFLAGS \_ problème d' \_ Activation \_ RPC à l' \_ \_ identification   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>APPIDREGFLAGS \_ activer \_ IUSERVER \_ Description de l’ordinateur de bureau

Si l’indicateur **APPIDREGFLAGS \_ Activate \_ IUSERVER \_ indesktop** est effacé dans **AppIDFlags** ou si **AppIDFlags** n’est pas présent, le client d’une session Terminal Server effectuant une demande d’activation pour un serveur COM [utilisateur interactif](interactive-user.md) , crée une liaison ou lance le serveur com dans le bureau « par défaut » de la session de la [fenêtre](/windows/desktop/winstation/window-stations) « winsta0 » de la session dans la demande d’activation. Par exemple, si le client exécute « winsta0 \\ Desktop1 » de la session 3, la demande d’activation pour la session 3 crée une liaison ou un lancement et une liaison avec le serveur com dans « winsta0 \\ default » de la session 3, même si une instance du serveur com est déjà en cours d’exécution dans « winsta0 \\ Desktop1 » de la session 3.

Si l’indicateur **APPIDREGFLAGS \_ Activate \_ IUSERVER \_** est défini dans la valeur **AppIDFlags** , com crée une liaison avec le processus serveur qui s’exécute sur le Bureau du client et la session dans la demande d’activation, ou le lance et le lie. Par exemple, si le client exécute « winsta0 \\ Desktop1 » dans la session 3, la demande d’activation pour la session 3 crée une liaison, ou lance et crée une liaison avec le serveur com dans « winsta0 \\ Desktop1 » dans la session 3, même si une instance du serveur com est déjà en cours d’exécution dans « winsta0 \\ default » dans la session 3.

Le client peut utiliser le [moniker de session](/windows/desktop/TermServ/session-monikers) pour spécifier une session différente de la session du client lorsqu’il effectue la demande d’activation.

L’indicateur **APPIDREGFLAGS \_ Activate \_ IUSERVER \_ indesktop** s’applique uniquement aux serveurs com configurés pour runas «[interactive User](interactive-user.md)».

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>\_Description du \_ processus de sécurisation du serveur APPIDREGFLAGS \_ \_ SD \_ et de la \_ liaison

Si l’indicateur de **\_ \_ \_ \_ \_ liaison SD et \_ Bind du processus de serveur APPIDREGFLAGS** est défini dans **AppIDFlags**, les serveurs com configurés pour runas « Activator » seront lancés avec un descripteur de sécurité de processus qui autorise le processus à [ \_ \_ accéder](/windows/desktop/ProcThread/process-security-and-access-rights) au SID LogonID du jeton de processus. En outre, le propriétaire du descripteur de sécurité sera défini sur le SID LogonID du jeton de processus.

Si l’indicateur de **\_ \_ \_ \_ \_ liaison SD et \_ Bind du processus de serveur APPIDREGFLAGS** est défini dans **AppIDFlags**, les serveurs com configurés pour runas « cet utilisateur » seront lancés avec un descripteur de sécurité de processus qui autorise le [processus \_ tout \_ accès](/windows/desktop/ProcThread/process-security-and-access-rights) dans le SID LogonID du jeton de processus. En outre, le propriétaire du descripteur de sécurité sera défini sur le SID LogonID du jeton de processus. En outre, le gestionnaire de contrôle des services COM (SCM) modifie le jeton du processus serveur COM comme suit :

-   Elle ajoute un SID APPID au jeton. Elle accorde l’accès complet au SID APPID dans la liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List) du jeton par défaut. dans Windows Vista et les versions ultérieures de Windows, il accorde l’autorisation de contrôle READ SID OwnerRights \_ dans la liste DACL par défaut du jeton. dans les versions antérieures Windows Vista de Windows, il définit le propriétaire du jeton sur le SID APPID.

Les considérations de sécurité suivantes doivent être prises en compte lors de l’utilisation de l’indicateur **\_ \_ \_ \_ SD \_ et \_ Bind du processus de serveur APPIDREGFLAGS sécurisé** :

-   L' **indicateur \_ \_ \_ \_ SD \_ et \_ Bind du processus de serveur sécurisé APPIDREGFLAGS** est destiné à être défini par les serveurs com qui sont lancés sous l’un des contextes de sécurité de service intégrés, à savoir les comptes NetworkService ou LocalService. Si les serveurs empruntent l’identité des clients privilégiés et que l’indicateur de **\_ \_ \_ \_ \_ liaison SD et \_ Bind du processus de serveur APPIDREGFLAGS** n’est pas défini, le code malveillant s’exécutant dans d’autres processus avec le même contexte de sécurité peut élever les privilèges en détournant les jetons d’emprunt d’identité des clients privilégiés à partir du processus serveur com.
-   Lorsque l’indicateur de **\_ \_ \_ \_ \_ liaison SD et \_ Bind du processus du serveur APPIDREGFLAGS** est défini, com renforce le descripteur de sécurité de l’objet processus dans le cas de serveurs com « Activator » runas. Pour ces serveurs, le client COM est supposé renforcer le jeton qu’il utilise pour l’activation COM.
-   Lorsque l’indicateur de **\_ \_ \_ \_ \_ liaison SD et \_ Bind du processus de serveur APPIDREGFLAGS sécurisé** est défini, com renforce le descripteur de sécurité de l’objet processus dans le cas des serveurs com « cet utilisateur » runas. Elle renforce également le jeton de processus du serveur COM puisque le SCM COM est l’entité qui crée le jeton.

l' **indicateur \_ \_ \_ \_ SD \_ et \_ BIND du processus de serveur sécurisé APPIDREGFLAGS** est pris en charge dans Windows XP, Windows server 2003, Windows Vista et Windows server 2008 uniquement lorsque le correctif MSRC8322 ([bulletin de sécurité MS09-012](https://support.microsoft.com/kb/959454)) est appliqué. il est pris en charge en mode natif dans Windows 7 et les versions ultérieures de Windows.

L' **indicateur \_ \_ \_ \_ SD \_ et \_ Bind du processus de serveur sécurisé APPIDREGFLAGS** s’applique uniquement aux serveurs com configurés pour runas « Activator » ou « cet utilisateur ». Elle ne s’applique pas aux serveurs COM qui sont des services NT.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>APPIDREGFLAGS \_ problème d' \_ Activation \_ RPC à la \_ Description de l' \_ identification

Si la **APPIDREGFLAGS d' \_ activation du problème d' \_ Activation \_ RPC \_ à \_** l’indicateur d’identification est définie dans **AppIDFlags**, le SCM com émettra des demandes d’activation d’objet au processus serveur com en utilisant un niveau d’emprunt d’identité de l’identification du [niveau d' \_ \_ IMP \_ \_ RPC C](impersonation-levels.md).

Si le **APPIDREGFLAGS d' \_ activation du problème \_ \_ RPC \_ à \_** l’indicateur d’identification n’est pas défini, le SCM com émettra des demandes d’activation d’objet aux processus du serveur com en utilisant un niveau d’emprunt d’identité de l' [emprunt d' \_ \_ \_ \_ identité RPC C IMP](impersonation-levels.md).

Les considérations de sécurité suivantes doivent être prises en compte lors de l’utilisation du **RPC d’activation du problème APPIDREGFLAGS à l’indicateur d' \_ \_ \_ \_ \_ identification** :

-   L’activation de l’indicateur **APPIDREGFLAGS \_ \_ Activation \_ RPC \_ à \_** l’indicateur d’identification est destinée à être utilisée par les serveurs com qui n’effectuent pas de travail pour le compte des clients dans les demandes d’activation d’objet. pour ces serveurs, le fait d’avoir le SCM COM émettre des demandes d’activation d’objet au [ \_ niveau RPC C \_ IMP \_ level \_ identifier](impersonation-levels.md) réduit le risque de jetons privilégiés avec SE niveau de [**nom d’emprunt d' \_ identité \_**](/windows/desktop/SecAuthZ/privilege-constants) figurant dans le processus.

l’ACTIVATION de l’indicateur **APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC \_ à \_** l’indicateur d’identification est prise en charge dans Windows 7 et les versions ultérieures de Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bureaux](/windows/desktop/winstation/desktops)
</dt> <dt>

[Niveaux d’emprunt d’identité](impersonation-levels.md)
</dt> <dt>

[Utilisateur interactif](interactive-user.md)
</dt> <dt>

[Monikers de session](/windows/desktop/TermServ/session-monikers)
</dt> <dt>

[Stations Windows](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 