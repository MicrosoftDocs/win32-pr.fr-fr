---
description: Pour vous connecter à un ordinateur distant à l’aide de WMI, vérifiez que les paramètres DCOM et les paramètres de sécurité de l’espace de noms WMI corrects sont activés pour la connexion.
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: Sécurisation d’une connexion WMI à distance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8650ee47c549121a51e5d131055a84c176da944c6146f0532ffc86f1d2f9e4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739513"
---
# <a name="securing-a-remote-wmi-connection"></a>Sécurisation d’une connexion WMI à distance

Pour vous connecter à un ordinateur distant à l’aide de WMI, vérifiez que les paramètres DCOM et les paramètres de sécurité de l’espace de noms WMI corrects sont activés pour la connexion.

WMI possède les paramètres d’emprunt d’identité, d’authentification et de service d’authentification (NTLM ou Kerberos) par défaut requis par l’ordinateur cible dans une connexion à distance. Votre ordinateur local peut utiliser des valeurs par défaut différentes que le système cible n’accepte pas. Vous pouvez modifier ces paramètres dans l’appel de connexion.

Les sections suivantes sont présentées dans cette rubrique :

-   [emprunt d’identité et authentification DCOM Paramètres pour WMI](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [Définition de la sécurité DCOM pour autoriser un utilisateur à accéder à distance à un ordinateur](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [Autoriser les utilisateurs à accéder à un espace de noms WMI spécifique](#allowing-users-access-to-a-specific-wmi-namespace)
-   [Définition de la sécurité des espaces de noms pour exiger le chiffrement des données pour les connexions à distance](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [Rubriques connexes](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a>emprunt d’identité et authentification DCOM Paramètres pour WMI

WMI possède les paramètres d’emprunt d’identité DCOM par défaut, d’authentification et de service d’authentification (NTLM ou Kerberos) requis par le système distant. Votre système local peut utiliser des valeurs par défaut différentes de celles que le système distant cible n’accepte pas. Vous pouvez modifier ces paramètres dans l’appel de connexion. Pour plus d’informations, consultez Définition de la [sécurité des processus d’application cliente](setting-client-application-process-security.md). Toutefois, pour le service d’authentification, il est recommandé de spécifier **la \_ \_ \_ valeur par défaut RPC C Authn** et de permettre à DCOM de choisir le service approprié pour l’ordinateur cible.

Vous pouvez fournir des paramètres dans les paramètres pour les appels à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) en C++. Dans les scripts, vous pouvez établir des paramètres de sécurité dans les appels à [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), dans un objet [**SWbemSecurity**](swbemsecurity.md) ou dans la chaîne de [moniker](constructing-a-moniker-string.md) de script.

Pour obtenir la liste de toutes les constantes d’emprunt d’identité C++, consultez [définition du niveau de sécurité de processus par défaut à l’aide de C++](setting-the-default-process-security-level-using-c-.md). pour plus d’Visual Basic les constantes et les chaînes de script pour l’utilisation de la connexion moniker, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

Le tableau suivant répertorie les paramètres d’emprunt d’identité, d’authentification et de service d’authentification DCOM par défaut requis par l’ordinateur cible (ordinateur B) dans une connexion à distance. Pour plus d’informations, consultez Sécurisation d’une connexion WMI à distance.



| Système d’exploitation ordinateur B | Chaîne de script de niveau d’emprunt d’identité | Chaîne de script de niveau d’authentification | Service d’authentification |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| Windows Vista ou version ultérieure ;      | Impersonate                          | PKT                                   | Kerberos               |



 

les connexions à distance WMI sont affectées par [le contrôle de compte d’utilisateur (UAC)](/previous-versions/aa905108(v=msdn.10)) et [Windows pare-feu](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx). pour plus d’informations, consultez [connexion à WMI à distance à partir de Vista](connecting-to-wmi-remotely-starting-with-vista.md) et [connexion via Windows pare-feu](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

N’oubliez pas que la connexion à WMI sur l’ordinateur local a le niveau d’authentification par défaut **PktPrivacy**.

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a>Définition de la sécurité DCOM pour autoriser un utilisateur à accéder à distance à un ordinateur

La sécurité dans WMI est liée à la connexion à un espace de noms WMI. WMI utilise DCOM pour gérer les appels distants. L’échec de la connexion à un ordinateur distant est dû à une défaillance DCOM (erreur « accès DCOM refusé » décimal-2147024891 ou Hex 0x80070005). Pour plus d’informations sur la sécurité DCOM dans WMI pour les applications C++, consultez Définition de la [sécurité des processus d’application cliente](setting-client-application-process-security.md).

Vous pouvez configurer les paramètres DCOM pour WMI à l’aide de l’utilitaire de configuration DCOM (**DCOMCnfg.exe**) disponible dans **Outils d’administration** dans le **panneau** de configuration. Cet utilitaire expose les paramètres qui permettent à certains utilisateurs de se connecter à l’ordinateur à distance via DCOM. Les membres du groupe administrateurs sont autorisés à se connecter à distance à l’ordinateur par défaut. Avec cet utilitaire, vous pouvez définir la sécurité pour démarrer, accéder et configurer le service WMI.

La procédure suivante décrit comment accorder des autorisations de démarrage et d’activation à distance DCOM pour certains utilisateurs et groupes. Si l’ordinateur A se connecte à distance à l’ordinateur B, vous pouvez définir ces autorisations sur l’ordinateur B pour autoriser un utilisateur ou un groupe qui ne fait pas partie du groupe Administrateurs sur l’ordinateur B à exécuter les appels de démarrage et d’activation DCOM sur l’ordinateur B.

**Pour accorder des autorisations d’activation et de lancement à distance DCOM pour un utilisateur ou un groupe**

1.  Cliquez sur **Démarrer**, sur **exécuter**, tapez **DCOMCNFG**, puis cliquez sur **OK**.
2.  Dans la boîte de dialogue **services de composants** , développez **services de composants**, développez **ordinateurs**, puis cliquez avec le bouton droit sur **poste de travail** et cliquez sur **Propriétés**.
3.  Dans la boîte de dialogue Propriétés de la **poste de travail** , cliquez sur l’onglet **sécurité com** .
4.  Sous **Autorisations d'exécution et d'activation**, cliquez sur **Modifier les limites**.
5.  Dans la boîte de dialogue **autorisation d’exécution** , procédez comme suit si votre nom ou votre groupe n’apparaît pas dans la **Liste groupes ou noms d’utilisateurs**:

    1.  Dans la boîte de dialogue **autorisation d’exécution** , cliquez sur **Ajouter**.
    2.  Dans la boîte de dialogue **Sélectionner les utilisateurs, les ordinateurs ou les groupes** , ajoutez votre nom et le groupe dans la zone **Entrez les noms des objets à sélectionner** , puis cliquez sur **OK**.

6.  Dans la boîte de dialogue **autorisation d’exécution** , sélectionnez votre utilisateur et votre groupe dans la zone **noms de groupes ou d’utilisateurs** . Dans la **colonne autoriser** , **sous autorisations pour utilisateur**, sélectionnez **exécution à distance** et sélectionnez **activation à distance**, puis cliquez sur **OK**.

La procédure suivante décrit comment accorder des autorisations d’accès à distance DCOM pour certains utilisateurs et groupes. Si l’ordinateur A se connecte à distance à l’ordinateur B, vous pouvez définir ces autorisations sur l’ordinateur B pour autoriser un utilisateur ou un groupe qui ne fait pas partie du groupe Administrateurs sur l’ordinateur B à se connecter à l’ordinateur B.

**Pour accorder des autorisations d’accès à distance DCOM**

1.  Cliquez sur **Démarrer**, sur **exécuter**, tapez **DCOMCNFG**, puis cliquez sur **OK**.
2.  Dans la boîte de dialogue **services de composants** , développez **services de composants**, développez **ordinateurs**, puis cliquez avec le bouton droit sur **poste de travail** et cliquez sur **Propriétés**.
3.  Dans la boîte de dialogue Propriétés de la **poste de travail** , cliquez sur l’onglet **sécurité com** .
4.  Sous **Autorisations d'accès**, cliquez sur **Modifier les limites**.
5.  Dans la boîte de dialogue **autorisation d’accès** , sélectionnez nom **d’ouverture de session anonyme** dans la zone **noms de groupes ou d’utilisateurs** . Dans la colonne **autoriser** , sous **autorisations pour utilisateur**, sélectionnez **accès à distance**, puis cliquez sur **OK**.

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a>Autoriser les utilisateurs à accéder à un espace de noms WMI spécifique

Vous pouvez autoriser ou interdire l’accès des utilisateurs à un espace de noms WMI spécifique en définissant l’autorisation « accès à distance autorisé » dans le contrôle WMI pour un espace de noms. Si un utilisateur tente de se connecter à un espace de noms auquel il n’est pas autorisé à accéder, il recevra l’erreur 0x80041003. Par défaut, cette autorisation est activée uniquement pour les administrateurs. Un administrateur peut activer l’accès à distance à des espaces de noms WMI spécifiques pour un utilisateur qui n’est pas administrateur.

La procédure suivante définit les autorisations d’activation à distance pour un utilisateur non-administrateur.

**Pour définir les autorisations d’activation à distance**

1.  Connecter à l’ordinateur distant à l’aide du contrôle WMI.

    Pour plus d’informations sur le contrôle WMI, consultez Définition de la [sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).

2.  Dans l’onglet **sécurité** , sélectionnez l’espace de noms, puis cliquez sur **sécurité**.
3.  Localisez le compte approprié et cochez la case **activer à distance** dans la liste des **autorisations** .

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a>Définition de la sécurité des espaces de noms pour exiger le chiffrement des données pour les connexions à distance

Un administrateur ou un fichier MOF peut configurer un espace de noms WMI afin qu’aucune donnée ne soit retournée, à moins que vous n’utilisiez la confidentialité du paquet (niveau d’authentification ou **PktPrivacy** en tant que moniker du **niveau d' \_ \_ authentification \_ \_ \_ C RPC** ) dans une connexion à cet espace de noms. Cela permet de s’assurer que les données sont chiffrées lorsqu’elles traversent le réseau. Si vous essayez de définir un niveau d’authentification inférieur, vous obtiendrez un message d’accès refusé. Pour plus d’informations, consultez [la page exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).

L’exemple de code VBScript suivant montre comment se connecter à un espace de noms chiffré à l’aide de « pktPrivacy ».


```VB
strComputer = "RemoteComputer"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!\\" _
                              & strComputer & "\root\EncryptedNamespace")
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Délégation avec WMI](connecting-to-a-3rd-computer-delegation.md)
</dt> <dt>

[Création de processus à distance avec WMI](creating-processes-remotely.md)
</dt> <dt>

[Sécurisation des clients et des fournisseurs C++](securing-c---clients-and-providers.md)
</dt> <dt>

[Sécurisation des clients de script](securing-scripting-clients.md)
</dt> </dl>

 

 
