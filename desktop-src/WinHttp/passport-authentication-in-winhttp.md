---
description: les Services HTTP Microsoft Windows (WinHTTP) prennent entièrement en charge l’utilisation côté client du protocole d’authentification Microsoft Passport. Cette rubrique fournit une vue d’ensemble des transactions impliquées dans l’authentification Passport et explique comment les gérer.
ms.assetid: 395d7aef-4da0-4664-8328-7d31ce58fedd
title: Authentification Passport dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d6aff7f8924c307d4e21efb77bc57ebae2469e50361b57d12dce5b348555e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114301"
---
# <a name="passport-authentication-in-winhttp"></a>Authentification Passport dans WinHTTP

les Services HTTP Microsoft Windows (WinHTTP) prennent entièrement en charge l’utilisation côté client du protocole d’authentification Microsoft Passport. Cette rubrique fournit une vue d’ensemble des transactions impliquées dans l’authentification Passport et explique comment les gérer.

> [!Note]  
> Dans WinHTTP 5,1, l’authentification Passport est désactivée par défaut.

 

## <a name="passport-14"></a>Passport 1,4

Passport est un composant principal des services de bloc de Microsoft .NET. Elle permet aux entreprises de développer et d’offrir des services Web distribués dans un large éventail d’applications et permet à ses membres d’utiliser un nom et un mot de passe de connexion sur tous les sites Web participants.

WinHTTP assure la prise en charge de la plateforme pour Microsoft Passport 1,4 en implémentant le protocole côté client pour l’authentification Passport 1,4. il libère les applications des détails de l’interaction avec l’infrastructure Passport et des noms d’utilisateurs et mots de passe stockés dans Windows XP. Cette abstraction utilise Passport, et non pas du point de vue d’un développeur, que les schémas d’authentification traditionnels comme Basic ou Digest.

**Windows XP :** la clé de registre **HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Internet Paramètres \\ Passport \\ NumRegistrationRuns** identifie le nombre de fois où l’assistant authentification passport s’affiche lorsque l’authentification passport est requise. Si la valeur de cette clé est définie sur un nombre supérieur à 5, l’Assistant n’est pas affiché.

Les sections suivantes décrivent les transactions impliquées dans l’authentification Passport du point de vue d’une application cliente. Pour le développement Passport côté serveur, consultez la présentation de la documentation du kit de développement logiciel (SDK) Passport.

-   [Requête initiale](#initial-request)
-   [Serveur de connexion Passport](#passport-login-server)
-   [Demande authentifiée](#authenticated-request)

### <a name="initial-request"></a>Requête initiale

Lorsqu’un client demande une ressource sur un serveur qui requiert l’authentification Passport, le serveur vérifie la présence de [*tickets*](glossary.md)dans la demande. Si un *ticket* valide est envoyé avec la demande, le serveur répond avec la ressource demandée. Si le *ticket* n’existe pas sur le client, le serveur répond avec un code d’État 302. La réponse comprend l’en-tête Challenge, « WWW-Authenticate : Passport 1.4 ». Les clients qui n’utilisent pas Passport peuvent suivre la redirection vers le serveur de connexion Passport. Les clients plus avancés contactent généralement le contact Passport pour déterminer l’emplacement du serveur de connexion Passport.

> [!Note]  
> Le point central du réseau Microsoft Passport est la *connexion Passport,* qui facilite la synchronisation des sites des participants Passport pour s’assurer que chaque site dispose des informations les plus récentes sur la configuration du réseau et d’autres problèmes. Chaque composant Passport (gestionnaire Passport, serveurs de connexion, serveurs de mise à jour, etc.) communique régulièrement avec la connexion pour récupérer les informations dont il a besoin pour localiser et communiquer correctement avec les autres composants du réseau Passport. Ces informations sont récupérées sous la forme d’un document XML appelé document de configuration de composant ou CCD.

 

L’illustration suivante montre la demande initiale à une filiale Passport.

![image affiche la demande initiale à une filiale Passport.](images/art-passport1.png)

### <a name="passport-login-server"></a>Serveur de connexion Passport

Un serveur de connexion Passport gère toutes les demandes de [*tickets*](glossary.md) pour toutes les ressources d’une *autorité de domaine* Passport. Avant qu’une demande puisse être authentifiée à l’aide de Passport, l’application cliente doit contacter le serveur de connexion pour obtenir les *tickets* appropriés.

Lorsqu’un client demande des [*tickets*](glossary.md) à partir d’un serveur de connexion Passport, le serveur de connexion répond généralement avec un code d’état 401 pour indiquer que les informations d’identification de l’utilisateur doivent être fournies. Lorsque ces informations d’identification sont fournies, le serveur de connexion répond avec les *tickets* requis pour accéder à la ressource spécifiée sur le serveur qui contient la ressource initialement demandée. Le serveur de connexion peut également rediriger le client vers un autre serveur qui peut fournir la ressource demandée.

![image montre une demande de ticket client à un serveur de connexion Passport.](images/art-passport2.png)

### <a name="authenticated-request"></a>Demande authentifiée

Lorsque le client a les [*tickets*](glossary.md) qui correspondent à un serveur donné, ces *tickets* sont inclus avec toutes les demandes adressées à ce serveur. Si les *tickets* n’ont pas été modifiés depuis qu’ils ont été récupérés à partir du serveur de connexion Passport et que les *tickets* sont valides pour le serveur de ressources, le serveur de ressources envoie une réponse qui comprend à la fois la ressource demandée et les cookies indiquant que l’utilisateur est authentifié pour les demandes ultérieures.

Les cookies supplémentaires dans la réponse sont destinés à accélérer le processus d’authentification. Les demandes supplémentaires dans la même session pour les ressources sur les serveurs dans la même autorité de domaine Passport incluent toutes ces cookies supplémentaires. Les informations d’identification n’ont pas besoin d’être envoyées à nouveau au serveur de connexion tant que les cookies n’ont pas expiré.

![image affiche une demande authentifiée auprès du serveur de connexion Passport.](images/art-passport3.png)

## <a name="using-passport-in-winhttp"></a>Utilisation de Passport dans WinHTTP

L’authentification Passport dans WinHTTP est très similaire à d’autres schémas d’authentification. Consultez [authentification dans WinHTTP](authentication-in-winhttp.md) pour obtenir une vue d’ensemble de l’authentification dans WinHTTP.

Dans WinHTTP 5,1, l’authentification Passport est désactivée par défaut et doit être explicitement activée avec [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avant son utilisation.

WinHTTP gère un grand nombre des détails de la transaction en interne pour l’authentification Passport. Pendant la demande initiale, le serveur répond avec un code d’État 302 lorsque l’authentification est nécessaire. Le code d’État 302 indique en fait une redirection et fait partie du protocole Passport pour la compatibilité descendante. WinHTTP masque le code d’État 302 et contacte le contact Passport, puis le serveur de connexion. L’application WinHTTP est informée du code d’état 401 envoyé par le serveur de connexion pour demander les informations d’identification de l’utilisateur. Toutefois, pour l’application, elle apparaît comme si l’état 401 provient du serveur à partir duquel la ressource a été demandée. De cette façon, l’application WinHTTP ignore les interactions avec d’autres serveurs, et elle peut gérer l’authentification Passport avec le même code qui gère d’autres schémas d’authentification.

En règle générale, une application WinHTTP répond à un code d’état 401 en fournissant les informations d’identification d’authentification. Lorsque les informations d’identification sont fournies avec [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) ou [**SetCredentials**](iwinhttprequest-setcredentials.md) pour l’authentification Passport, les informations d’identification sont envoyées au serveur de connexion, et non au serveur indiqué dans la demande.

Toutefois, lors de la réponse à un code d’État 407, une application WinHTTP doit utiliser [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pour fournir les informations d’identification du proxy, plutôt que [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials). Dans la mesure où **WinHttpSetOption** est un moyen moins sûr de fournir des informations d’identification, il doit normalement être évité.

Une fois récupérés, les [*tickets*](glossary.md) sont gérés en interne et sont automatiquement envoyés aux serveurs applicables dans les demandes ultérieures.

> [!Note]  
> WinHTTP vous permet de désactiver la redirection automatique en appelant la fonction [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) pour l' [**\_ option WinHTTP \_ désactiver \_**](option-flags.md) l’indicateur de fonctionnalité et en spécifiant la valeur [**WinHTTP \_ Désactiver les \_ redirections**](option-flags.md). La désactivation de la redirection n’interfère pas avec la redirection que WinHTTP gère en interne pour les transactions Passport.

 

WinHTTP peut terminer avec succès l’authentification Passport même si une application désactive la redirection automatique. Toutefois, une fois l’authentification Passport terminée, une redirection implicite doit se produire à partir de l’URL du serveur de connexion Passport vers l’URL d’origine. Cette redirection n’est pas déclenchée par une réponse HTTP 302, mais est implicite dans le protocole Passport.

WinHTTP gère cette redirection implicite. Si une application a désactivé la redirection automatique, WinHTTP exige que l’application donne une « autorisation » à la fonction WinHTTP à rediriger automatiquement dans ce cas particulier.

Pour que WinHTTP redirige vers l’URL d’origine après l’authentification, l’application doit inscrire une fonction de rappel à l’aide de [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback). WinHTTP peut ensuite notifier l’application avec un \_ rappel de REdirection de l’état de rappel WinHTTP \_ , ce \_ qui permet à l’application d’annuler la redirection. Une application n’a pas besoin de fournir des fonctionnalités dans la fonction de rappel ; l’inscription du rappel est suffisante pour permettre à WinHTTP de suivre cette redirection de cas spéciaux.

Le message d’échec de connexion WinHTTP de l’erreur \_ \_ \_ est généré si aucune fonction de rappel n’est définie par l’application.

### <a name="passport-cobranding"></a>Comarketing Passport

Contrairement aux schémas d’authentification traditionnels pris en charge par WinHTTP, Passport peut être largement [*développé.*](glossary.md) Lors de la réception d’un code d’état 401 qui indique un défi, une application peut récupérer le graphique et le texte de la *comarketing* . Récupérez une URL pour le graphique de *comarquage* en appelant [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) avec l' \_ option WinHTTP indicateur d’URL de \_ \_ comarketing Passport \_ . Récupérez le texte de la *comarque* en appelant [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) avec l' \_ option WinHTTP indicateur de \_ \_ texte comarque Passport \_ . Ces éléments peuvent être utilisés pour personnaliser une boîte de dialogue de collecte des informations d’identification.

### <a name="stored-user-names-and-passwords"></a>Noms d’utilisateur et mots de passe stockés

Windows XP a introduit le concept de noms d’utilisateurs et de mots de passe stockés. Si les informations d’identification Passport d’un utilisateur sont enregistrées via l' **Assistant Inscription Passport** ou la **boîte de dialogue informations d’identification** standard, elles sont enregistrées dans les noms d’utilisateur et mots de passe stockés. quand vous utilisez winhttp sur Windows XP ou version ultérieure, winhttp utilise automatiquement les informations d’identification dans les noms d’utilisateurs et les mots de passe stockés si les informations d’identification ne sont pas définies explicitement. Cela est similaire à la prise en charge des informations d’identification d’ouverture de session par défaut pour NTLM/Kerberos. Toutefois, l’utilisation des informations d’identification Passport par défaut n’est pas soumise aux paramètres de stratégie d’ouverture de session automatique.

### <a name="disabling-passport-authentication"></a>Désactivation de l’authentification Passport

Certaines applications peuvent nécessiter la possibilité de désactiver l’authentification Passport. Par exemple, lorsqu’une filiale Passport répond avec le code d’état initial 302, il peut être préférable de suivre la redirection indiquée et d’afficher la page d’authentification Passport HTML plutôt que d’autoriser WinHTTP à gérer l’authentification en interne. L’authentification Passport est désactivée dans WinHTTP en appelant la fonction [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l’option WinHTTP \_ configurer l' \_ \_ \_ authentification Passport et en passant la valeur WinHTTP \_ désactiver l' \_ \_ authentification Passport. Vous pouvez ensuite la réactiver avec WINHTTP \_ activer \_ l' \_ authentification Passport.

L’authentification Passport ne peut pas être désactivée lors de l’utilisation de l’objet [**WinHttpRequest**](winhttprequest.md) .

Comme indiqué plus haut dans cette section, l’authentification Passport est désactivée par défaut dans WinHTTP 5,1 et doit être explicitement activée avec [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avant son utilisation.

## <a name="passport-configuration-overrides-used-for-testing"></a>Remplacements de la configuration Passport utilisés pour le test

WinHTTP s’appuie sur les informations de configuration qu’il télécharge à partir du serveur de transfert Passport pour prendre en charge l’authentification Passport 1,4. Par défaut, ce serveur sécurisé (SSL) est nexus.passport.com et la ressource de configuration est RDR/pprdr. asp, qui est appelée configuration de Passport « en direct ». Le format des informations est un en-tête HTTP personnalisé « PassportURLs », suivi de paires attribut-valeur séparées par des virgules.

Par exemple, « https://nexus.passport.com/rdr/pprdr.asp » retourne les informations de configuration suivantes :

``` syntax
PassportURLs: DARealm=Passport.net,
DALogin=login.passport.com/login2.asp,
DAReg=https://register.passport.com/defaultwiz.asp,
Properties=https://memberservices.passport.com/ppsecure/MSRV_EditProfile.asp,
Privacy=https://www.passport.com/consumer/privacypolicy.asp,
GeneralRedir=https://nexusrdr.passport.com/redir.asp,
Help=https://memberservices.passport.com/UI/MSRV_UI_Help.asp,
ConfigVersion=2
\r\n
```

Les parties qui sont pertinentes pour WinHTTP sont DARealm, DALogin et ConfigVersion. Pour des raisons de performances, elles sont mises en cache pendant la durée de vie d’une session WinHTTP. Ces trois valeurs peuvent être remplacées par les applications qui sont requises pour fonctionner avec une autre infrastructure Passport autre que la configuration de production « en direct » en modifiant les paramètres de registre appropriés sous

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
LoginServerRealm (REG_SZ)    For example: abc.net
LoginServerUrl (REG_SZ)      For example: https://private-login.passport.com/login2.asp
ConfigVersion (REG_DWORD)    For example: 10
```

Si LoginServerUrl est présent dans le registre, WinHTTP ne contacte pas le serveur de communication pour d’autres valeurs de configuration. Dans ce cas, LoginServerRealm et ConfigVersion doivent également être définis dans le registre pour corriger les valeurs.

Une application peut, à des fins de test, être requise pour télécharger la configuration de Passport à partir d’un serveur de transfert privé. Pour ce faire, vous pouvez substituer deux valeurs de Registre sous

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Internet Settings
                  WinHttp
                     Passport Test
```

``` syntax
NexusHost (REG_SZ)    e.g. private-nexus.passport.com
NexusObj(REG_SZ)      e.g. config/passport.asp
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification dans WinHTTP](authentication-in-winhttp.md)
</dt> </dl>

 

 



