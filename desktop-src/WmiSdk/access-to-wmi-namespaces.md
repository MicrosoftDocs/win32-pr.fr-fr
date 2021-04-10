---
description: WMI utilise un descripteur de sécurité Windows standard pour contrôler l’accès aux espaces de noms WMI.
ms.assetid: 5cf9886c-04fa-480e-889f-b64a6a70d053
ms.tgt_platform: multiple
title: Accès aux espaces de noms WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eaebe5370e97dcb42ddcf79018015ceff9147f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952869"
---
# <a name="access-to-wmi-namespaces"></a>Accès aux espaces de noms WMI

WMI utilise un *descripteur de sécurité* Windows standard pour contrôler l’accès aux espaces de noms WMI. Quand vous vous connectez à WMI, par le biais du moniker « winmgmts » WMI ou d’un appel à [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) ou [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), vous vous connectez à un espace de noms spécifique.

Les informations suivantes sont présentées dans cette rubrique :

-   [Sécurité de l’espace de noms WMI](#wmi-namespace-security)
-   [Audit de l’espace de noms WMI](#wmi-namespace-auditing)
-   [Types d’événements d’espace de noms](#types-of-namespace-events)
-   [Paramètres d’accès à l’espace de noms](#namespace-access-settings)
-   [Autorisations par défaut sur les espaces de noms WMI](#default-permissions-on-wmi-namespaces)
-   [Rubriques connexes](#related-topics)

## <a name="wmi-namespace-security"></a>Sécurité de l’espace de noms WMI

WMI gère la sécurité des espaces de noms en comparant le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) de l’utilisateur qui se connecte à l’espace de noms avec le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) de l’espace de noms. Pour plus d’informations sur la sécurité Windows, consultez [accès aux objets sécurisables WMI](access-to-wmi-securable-objects.md).

Sachez que, à partir de Windows Vista, le [contrôle de compte d’utilisateur (UAC, User Account Control)](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) affecte l’accès aux données WMI et ce qui peut être configuré avec le [*contrôle WMI*](gloss-w.md). Pour plus d’informations, consultez [autorisations par défaut sur les espaces de noms WMI](#default-permissions-on-wmi-namespaces) et [le contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).

L’accès aux espaces de noms WMI est également affecté lorsque la connexion provient d’un ordinateur distant. Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md), [sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md)et [connexion via le pare-feu Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Les fournisseurs doivent s’appuyer sur le paramètre d’emprunt d’identité de la connexion pour déterminer si le script ou l’application cliente doit recevoir des données. Pour plus d’informations sur les scripts et les applications clientes, consultez Définition de la [sécurité des processus d’application cliente](setting-client-application-process-security.md). Pour plus d’informations sur l’emprunt d’identité du [*fournisseur*](gloss-p.md) , consultez [développement d’un fournisseur WMI](developing-a-wmi-provider.md).

## <a name="wmi-namespace-auditing"></a>Audit de l’espace de noms WMI

WMI utilise les [*listes de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) de l’espace de noms pour auditer l’activité de l’espace de noms. Pour activer l’audit des espaces de noms WMI, utilisez l’onglet **sécurité** du [*contrôle WMI*](gloss-w.md) pour modifier les paramètres d’audit de l’espace de noms.

L’audit n’est pas activé lors de l’installation du système d’exploitation. Pour activer l’audit, cliquez sur l’onglet **audit** dans la fenêtre **sécurité** standard. Vous pouvez ensuite ajouter une entrée d’audit.

Stratégie de groupe de l’ordinateur local doit être défini pour autoriser l’audit. Vous pouvez activer l’audit en exécutant le composant logiciel enfichable MMC gpedit. msc et en définissant **audit Object Access** sous **Configuration ordinateur** paramètres Windows paramètres de  >    >  **sécurité**  >  **stratégies locales**  >  **stratégie d’audit**.

Une entrée d’audit modifie la liste SACL de l’espace de noms. Lorsque vous ajoutez une entrée d’audit, il s’agit d’un utilisateur, d’un groupe, d’un ordinateur ou d’un principal de sécurité intégré. Après avoir ajouté l’entrée, vous pouvez définir les opérations d’accès qui entraînent des événements du journal de sécurité. Par exemple, pour les utilisateurs authentifiés de groupe, vous pouvez cliquer sur exécuter des méthodes. Ce paramètre génère des événements de journal de sécurité chaque fois qu’un membre du groupe utilisateurs authentifiés exécute une méthode dans cet espace de noms. L’ID d’événement pour les événements WMI est 4662.

Votre compte doit être dans le groupe administrateurs et s’exécuter sous un privilège élevé pour modifier les paramètres d’audit. Le compte administrateur intégré peut également modifier la sécurité ou l’audit d’un espace de noms. Pour plus d’informations sur l’exécution en mode élevé, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).

L’audit WMI génère des événements de réussite ou d’échec pour les tentatives d’accès aux espaces de noms WMI. Le service n’audite pas la réussite ou l’échec des opérations du fournisseur. Par exemple, lorsqu’un script se connecte à WMI et à un espace de noms, il peut échouer, car le compte sous lequel le script s’exécute n’a pas accès à cet espace de noms ou peut tenter une opération, telle que la modification de la liste DACL, qui n’est pas accordée.

Si vous exécutez sous un compte dans le groupe administrateurs, vous pouvez afficher les événements d’audit de l’espace de noms dans l’interface utilisateur **Observateur d’événements** .

## <a name="types-of-namespace-events"></a>Types d’événements d’espace de noms

WMI effectue le suivi des types d’événements suivants dans le journal des événements de sécurité :

-   Succès de l’audit

    L’opération doit réussir deux étapes pour une réussite d’audit. Tout d’abord, WMI accorde l’accès à l’application cliente ou au script en fonction du SID du client et de la liste DACL des espaces de noms. Deuxièmement, l’opération demandée correspond aux droits d’accès dans la liste SACL d’espaces de noms pour cet utilisateur ou ce groupe.

-   Échec de l’audit

    WMI refuse l’accès à l’espace de noms, mais l’opération demandée correspond aux droits d’accès dans la liste SACL d’espaces de noms pour cet utilisateur ou ce groupe.

## <a name="namespace-access-settings"></a>Paramètres d’accès à l’espace de noms

Vous pouvez afficher les droits d’accès à l’espace de noms pour différents comptes sur le contrôle WMI. Ces constantes sont décrites dans [**constantes de droits d’accès à l’espace de noms**](namespace-access-rights-constants.md). Vous pouvez modifier l’accès à un espace de noms WMI à l’aide du contrôle WMI ou par programme. Pour plus d’informations, consultez [modification de la sécurité d’accès sur des objets sécurisables](changing-access-security-on-securable-objects.md).

Les audits WMI changent dans toutes les autorisations d’accès répertoriées dans la liste suivante, à l’exception de l’autorisation Remote Enable. Les modifications sont enregistrées en tant que succès ou échec de l’audit correspondant à l’autorisation Modifier la sécurité.

<dl> <dt>

<span id="Execute_Methods"></span><span id="execute_methods"></span><span id="EXECUTE_METHODS"></span>Méthodes Execute
</dt> <dd>

Permet à l’utilisateur d’exécuter des méthodes définies sur des classes WMI. Correspond à la constante d’autorisation d’accès d' **\_ \_ exécution de la méthode WBEM** .

</dd> <dt>

<span id="Full_Write"></span><span id="full_write"></span><span id="FULL_WRITE"></span>Écriture complète
</dt> <dd>

Autorise l’accès complet en lecture, écriture et suppression aux classes WMI et aux instances de classe, statiques et dynamiques. Correspond à la constante d’autorisation d’accès au **\_ \_ REP Full Write \_ REP** .

</dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>Écriture partielle
</dt> <dd>

Autorise l’accès en écriture aux instances de classe WMI statiques. Correspond à la constante d’autorisation d’accès de la **\_ \_ \_ Représentation partielle WBEM** .

</dd> <dt>

<span id="Provider_Write"></span><span id="provider_write"></span><span id="PROVIDER_WRITE"></span>Écriture du fournisseur
</dt> <dd>

Autorise l’accès en écriture aux instances de classe WMI dynamiques. Correspond à la constante d’autorisation d’accès du **\_ \_ fournisseur d’écriture WBEM** .

</dd> <dt>

<span id="Enable_Account"></span><span id="enable_account"></span><span id="ENABLE_ACCOUNT"></span>Activer le compte
</dt> <dd>

Autorise l’accès en lecture aux instances de classe WMI. Correspond à la constante d’autorisation d’accès **WBEM \_ Enable** .

</dd> <dt>

<span id="Remote_Enable"></span><span id="remote_enable"></span><span id="REMOTE_ENABLE"></span>Activation à distance
</dt> <dd>

Autorise l’accès à l’espace de noms par les ordinateurs distants. Correspond à la constante d’autorisation d’accès **\_ à \_ distance WBEM** .

</dd> <dt>

<span id="Read_Security"></span><span id="read_security"></span><span id="READ_SECURITY"></span>Sécurité de lecture
</dt> <dd>

Autorise l’accès en lecture seule aux paramètres DACL. Correspond à la constante d’autorisation d’accès au **\_ contrôle de lecture** .

</dd> <dt>

<span id="Edit_Security"></span><span id="edit_security"></span><span id="EDIT_SECURITY"></span>Modifier la sécurité
</dt> <dd>

Autorise l’accès en écriture aux paramètres DACL. Correspond à la constante d’autorisation **Write \_ DAC** Access.

</dd> </dl>

## <a name="default-permissions-on-wmi-namespaces"></a>Autorisations par défaut sur les espaces de noms WMI

Les groupes de sécurité par défaut sont les suivants :

-   Utilisateurs authentifiés
-   SERVICE LOCAL
-   SERVICE RÉSEAU
-   Administrateurs (sur l’ordinateur local)

Les autorisations d’accès par défaut pour les utilisateurs authentifiés, le SERVICE LOCAL et le SERVICE réseau sont les suivantes :

-   Méthodes d’exécution
-   Écriture complète
-   Activer le compte

Les comptes du groupe administrateurs disposent de tous les droits nécessaires, y compris la modification des descripteurs de sécurité. Toutefois, en raison du contrôle de compte d’utilisateur (UAC), le contrôle WMI ou le script doit s’exécuter avec un niveau de sécurité élevé. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](user-account-control-and-wmi.md).

Parfois, un script ou une application doit activer un privilège d’administrateur, tel que **SeSecurityPrivilege**, pour effectuer une opération. Par exemple, un script peut exécuter la méthode [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) de la [**classe Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) sans **SeSecurityPrivilege** et obtenir les informations de sécurité dans la liste de contrôle d' [*accès discrétionnaire (DACL, Discretionary Access Control List)*](/windows/desktop/SecGloss/d-gly) du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)de l’objet Printer. Toutefois, les informations SACL ne sont pas renvoyées au script, sauf si le privilège **SeSecurityPrivilege** est disponible et activé pour le compte. Si le compte ne dispose pas du privilège disponible, il ne peut pas être activé. Pour plus d’informations, consultez [exécution d’opérations privilégiées](executing-privileged-operations.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de WMI](about-wmi.md)
</dt> </dl>

 

 
