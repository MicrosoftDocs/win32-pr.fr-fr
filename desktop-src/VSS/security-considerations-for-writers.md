---
description: L’infrastructure VSS exige que les processus d’écriture fonctionnent à la fois comme clients COM et comme serveurs.
ms.assetid: 59bb7a86-e874-45ce-abd6-cafd18802c4d
title: Considérations relatives à la sécurité pour les Writers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601b981613636a571c204acdfac78ada778bb19b16a3d2677c4e56ff3ee099cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767679"
---
# <a name="security-considerations-for-writers"></a>Considérations relatives à la sécurité pour les Writers

L’infrastructure VSS exige que les processus d’écriture fonctionnent à la fois comme clients COM et comme serveurs.

Lorsqu’ils agissent en tant que serveurs, les enregistreurs VSS exposent des interfaces COM (par exemple, les gestionnaires d’événements VSS tels que [**CVssWriter :: OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) [**) et**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata)reçoivent des appels com entrants à partir de processus VSS (tels que les demandeurs et le service VSS) ou des appels RPC à partir de processus externes à VSS. Par conséquent, un enregistreur VSS doit gérer en toute sécurité les clients COM qui sont en mesure d’effectuer des appels COM entrants dans son processus.

De même, les enregistreurs VSS peuvent également agir en tant que clients COM, en effectuant des appels COM sortants vers des rappels fournis par l’infrastructure VSS ou des appels RPC à des processus qui sont externes à VSS. Ces rappels fournis par une application de sauvegarde ou par le service VSS permettent à l’enregistreur d’effectuer des tâches telles que la mise à jour du document des composants de sauvegarde par le biais de l’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) . Par conséquent, les paramètres de sécurité VSS doivent permettre aux rédacteurs d’effectuer des appels COM sortants dans d’autres processus VSS.

Le mécanisme le plus simple pour gérer les problèmes de sécurité de l’enregistreur implique la sélection appropriée du compte d’utilisateur sous lequel il s’exécute. Un enregistreur doit généralement s’exécuter sous un utilisateur membre du groupe administrateurs ou opérateurs de sauvegarde, ou il doit être exécuté en tant que compte système local.

Par défaut, lorsqu’un enregistreur agit en tant que client COM, s’il ne s’exécute pas sous ces comptes, tout appel COM qu’il effectue est automatiquement rejeté avec **E \_ ACCESSDENIED** sans même avoir à accéder à l’implémentation de la méthode com.

## <a name="disabling-com-exception-handling"></a>Désactivation de la gestion des exceptions COM

Lors du développement d’un enregistreur, définissez l' \_ exception com COMGLB exception \_ ne \_ gérer l’indicateur global options pour désactiver la gestion des exceptions com. Il est important de le faire, car la gestion des exceptions COM peut masquer les erreurs irrécupérables dans une application VSS. L’erreur masquée peut rendre le processus dans un état instable et imprévisible, ce qui peut entraîner des altérations et des blocages. Pour plus d’informations sur cet indicateur, consultez [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-writer-default-com-access-check-permission"></a>Autorisation de vérification de l’accès COM par défaut du générateur de paramètres

Les rédacteurs doivent savoir que lorsque leurs processus agissent comme un serveur (par exemple, pour gérer les événements VSS), ils doivent autoriser les appels entrants d’autres participants VSS, tels que les demandeurs ou le service VSS.

Toutefois, par défaut, un processus autorise uniquement les clients COM qui s’exécutent sous la même session de connexion (auto-SID) ou s’exécutant sous le compte système local. Il s’agit d’un problème potentiel, car ces valeurs par défaut ne sont pas suffisantes pour prendre en charge l’infrastructure VSS. Par exemple, les demandeurs peuvent s’exécuter comme un compte d’utilisateur « opérateur de sauvegarde » qui n’est pas dans la même session de connexion que le processus d’écriture ou un compte système local.

Pour gérer ce type de problème, chaque processus serveur COM peut exercer un contrôle accru sur le fait qu’un client RPC ou COM est autorisé à exécuter une méthode COM que le serveur (un enregistreur dans ce cas) implémente à l’aide de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir une autorisation de vérification de l’accès com par défaut au niveau du processus.

Les Writers peuvent explicitement effectuer les opérations suivantes :

-   Autorisez l’accès de tous les processus à appeler le processus d’écriture.

    cette option peut être adaptée à de nombreux enregistreurs et est utilisée par d’autres serveurs COM. par exemple, tous les services Windows basés sur SVCHOST utilisent déjà cette option, comme tous les services COM+ par défaut.

    Autoriser tous les processus à effectuer des appels COM entrants n’est pas nécessairement une faille de sécurité. Un enregistreur agissant comme un serveur COM, comme tous les autres serveurs COM, conserve toujours la possibilité d’autoriser ses clients sur chaque méthode COM implémentée dans son processus.

    Pour permettre à tous les processus d’accéder à COM à un writer, vous pouvez passer un descripteur de sécurité **null** comme premier paramètre de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). (Notez que **CoInitializeSecurity** doit être appelé au plus une fois pour l’ensemble du processus. Pour plus d’informations sur la fonction **CoInitializeSecurity**, consultez la documentation com.)

    Voici un exemple de code qui comprend un appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity):

    ``` syntax
    // Initialize COM security.
    hr = CoInitializeSecurity(
           NULL,                          // PSECURITY_DESCRIPTOR          pSecDesc,
           -1,                            // LONG                          cAuthSvc,
           NULL,                          // SOLE_AUTHENTICATION_SERVICE  *asAuthSvc,
           NULL,                          // void                         *pReserved1,
           RPC_C_AUTHN_LEVEL_PKT_PRIVACY, // DWORD                         dwAuthnLevel,
           RPC_C_IMP_LEVEL_IDENTIFY,      // DWORD                         dwImpLevel,
           NULL,                          // void                         *pAuthList,
           EOAC_NONE,                     // DWORD                         dwCapabilities,
           NULL                           // void                         *pReserved3
        );
    ```

    Lors de la définition explicite de la sécurité de niveau COM d’un writer avec [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), vous devez effectuer les opérations suivantes :

    -   Définissez le niveau d’authentification au moins **au \_ niveau de \_ \_ \_ connexion RPC C Authn**.

        Pour une meilleure sécurité, envisagez d’utiliser la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C**.

    -   Définissez le niveau d’emprunt d’identité sur **RPC \_ C \_ IMP \_ Level \_ identifier** , sauf si le processus de l’enregistreur doit autoriser l’emprunt d’identité pour des appels RPC ou com spécifiques qui ne sont pas liés à VSS.

-   Autorise uniquement les processus spécifiés à accéder au processus d’écriture.

    Un serveur COM (tel qu’un enregistreur) qui appelle [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) avec un descripteur de sécurité non **null** peut utiliser le descripteur pour se configurer lui-même pour accepter des appels entrants uniquement à partir d’utilisateurs appartenant à un ensemble spécifique de comptes.

    Un enregistreur doit s’assurer que les clients COM s’exécutant sous des utilisateurs valides sont autorisés à appeler son processus. Un enregistreur qui spécifie un descripteur de sécurité dans le premier paramètre doit autoriser les utilisateurs suivants à effectuer des appels entrants dans le processus du demandeur :

    -   Système Local
    -   Membres du groupe Administrateurs local
    -   Membres du groupe opérateurs de sauvegarde local
    -   Compte sous lequel le writer s’exécute

## <a name="explicitly-controlling-user-account-access-to-a-writer"></a>Contrôle explicite de l’accès d’un compte d’utilisateur à un enregistreur

Dans certains cas, la restriction de l’accès à un enregistreur aux processus qui s’exécutent en tant que système local, ou sous les groupes locaux administrateurs locaux ou opérateurs de sauvegarde locaux, peut être trop restrictive.

Par exemple, un processus d’écriture (peut-être un enregistreur tiers non-système) peut ne pas avoir besoin d’être exécuté sous un compte d’administrateur ou d’opérateur de sauvegarde. Pour des raisons de sécurité, il est préférable de ne pas promouvoir artificiellement les privilèges du processus pour prendre en charge VSS.

Dans ce cas, vous devez modifier la clé de Registre HKEY VssAccessControl VSS de la clé de Registre **HKEY \_ local \_ machine** \\ **System** \\  \\  \\  \\  pour indiquer à VSS qu’un utilisateur spécifié peut exécuter un enregistreur VSS en toute sécurité.

Sous cette clé, vous devez créer une sous-clé portant le même nom que le compte auquel l’accès doit être accordé ou refusé. Cette sous-clé doit être définie sur l’une des valeurs indiquées dans le tableau suivant.

| Valeur | Signification                                             |
|-------|-----------------------------------------------------|
| 0     | Refusez à l’utilisateur l’accès à votre rédacteur et au demandeur.  |
| 1     | Accordez à l’utilisateur l’accès à votre rédacteur.               |
| 2     | Accordez à l’utilisateur l’accès à votre demandeur.            |
| 3     | Accordez à l’utilisateur l’accès à votre rédacteur et au demandeur. |



 

L’exemple suivant accorde l’accès au compte « MyDomain \\ myuser » :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  MyDomain\MyUser = 1<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Ce mécanisme peut également être utilisé pour empêcher explicitement un utilisateur autrement autorisé d’exécuter un enregistreur VSS. L’exemple suivant permet de restreindre l’accès à partir du \\ compte « administrateur ThatDomain » :

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            VSS
               VssAccessControl
                  ThatDomain\Administrator = 0<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

L’administrateur ThatDomain de l’utilisateur \\ ne peut pas exécuter un enregistreur VSS.

 

 
