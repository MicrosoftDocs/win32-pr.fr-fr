---
description: L’infrastructure VSS requiert que les demandeurs VSS, tels que les applications de sauvegarde, puissent fonctionner à la fois comme clients COM et comme serveur.
ms.assetid: b01145c6-76ba-4a81-bca6-59c4ca488dac
title: Considérations relatives à la sécurité pour les demandeurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e989793dbf5a5dd1fac3224cf6f06958564de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318981"
---
# <a name="security-considerations-for-requesters"></a>Considérations relatives à la sécurité pour les demandeurs

L’infrastructure VSS requiert que les demandeurs VSS, tels que les applications de sauvegarde, puissent fonctionner à la fois comme clients COM et comme serveur.

Lorsqu’il joue le rôle de serveur, un demandeur expose un ensemble d’interfaces de rappel COM qui peuvent être appelées à partir de processus externes (tels que des Writers ou le service VSS). Par conséquent, les demandeurs doivent gérer en toute sécurité les clients COM qui sont en mesure d’effectuer des appels COM entrants dans son processus.

De même, les demandeurs peuvent agir comme un client COM pour les API COM fournies par un enregistreur VSS ou par le service VSS. Les paramètres de sécurité spécifiques au demandeur doivent autoriser les appels COM sortants du demandeur à ces autres processus.

Le mécanisme le plus simple pour gérer les problèmes de sécurité d’un demandeur consiste à sélectionner correctement le compte d’utilisateur sous lequel il s’exécute.

Un demandeur doit généralement s’exécuter sous un utilisateur membre du groupe administrateurs ou opérateurs de sauvegarde, ou bien s’exécuter en tant que compte système local.

Par défaut, lorsqu’un demandeur agit comme un client COM, s’il ne s’exécute pas sous ces comptes, tout appel COM est automatiquement rejeté avec **E \_ ACCESSDENIED**, sans même avoir à accéder à l’implémentation de la méthode com.

## <a name="disabling-com-exception-handling"></a>Désactivation de la gestion des exceptions COM

Lors du développement d’un demandeur, définissez l’exception COM COMGLB \_ exception \_ ne \_ handle d’options globales pour désactiver la gestion des exceptions com. Il est important de le faire, car la gestion des exceptions COM peut masquer les erreurs irrécupérables dans une application VSS. L’erreur masquée peut rendre le processus dans un état instable et imprévisible, ce qui peut entraîner des altérations et des blocages. Pour plus d’informations sur cet indicateur, consultez [IGlobalOptions](/windows/win32/api/objidlbase/nn-objidlbase-iglobaloptions).

## <a name="setting-requester-default-com-access-check-permission"></a>Définition de l’autorisation de vérification de l’accès COM par défaut du demandeur

Les demandeurs doivent savoir que lorsque leur processus agit comme un serveur (par exemple, en autorisant les enregistreurs à modifier le document des composants de sauvegarde), ils doivent autoriser les appels entrants d’autres participants VSS, tels que les enregistreurs ou le service VSS.

Toutefois, par défaut, un processus Windows autorise uniquement les clients COM qui s’exécutent sous la même session de connexion (le SID SELF) ou s’exécutent sous le compte système local. Il s’agit d’un problème potentiel, car ces paramètres par défaut ne sont pas adaptés à l’infrastructure VSS. Par exemple, les enregistreurs peuvent s’exécuter en tant que compte d’utilisateur « opérateur de sauvegarde » qui n’est pas dans la même session de connexion que le processus du demandeur ou un compte système local.

Pour gérer ce type de problème, chaque processus serveur COM peut exercer un contrôle accru sur le fait qu’un client RPC ou COM est autorisé à exécuter une méthode COM implémentée par le serveur (demandeur dans ce cas) en utilisant [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) pour définir une autorisation de vérification de l’accès com par défaut au niveau du processus.

Les demandeurs peuvent explicitement effectuer les opérations suivantes :

-   Autorisez l’accès de tous les processus à appeler le processus du demandeur.

    Cette option peut être adaptée à la grande majorité des demandeurs et est utilisée par d’autres serveurs COM. par exemple, tous les services Windows basés sur SVCHOST utilisent déjà cette option, comme tous les services COM+ par défaut.

    Autoriser tous les processus à effectuer des appels COM entrants n’est pas nécessairement une faille de sécurité. Un demandeur agissant comme un serveur COM, comme tous les autres serveurs COM, conserve toujours l’option permettant d’autoriser ses clients sur chaque méthode COM implémentée dans son processus.

    Notez que les rappels COM internes implémentés par VSS sont sécurisés par défaut.

    Pour permettre à tous les processus d’accéder à COM à un demandeur, vous pouvez passer un descripteur de sécurité **null** comme premier paramètre de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). (Notez que **CoInitializeSecurity** doit être appelé au plus une fois pour l’ensemble du processus. Pour plus d’informations sur les appels **CoInitializeSecurity** , consultez la documentation com ou MSDN.)

    L’exemple de code suivant montre comment un demandeur doit appeler [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) dans Windows 8 et windows server 2012 et versions ultérieures, afin d’être compatible avec VSS pour les partages de fichiers distants (VSS) :

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IMPERSONATE,   //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_STATIC,                   //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Lors de la définition explicite de la sécurité de niveau COM d’un demandeur avec [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), vous devez effectuer les opérations suivantes :

    -   Définissez le niveau d’authentification sur au moins l' **\_ \_ \_ \_ \_ intégrité PKT au niveau** de l’authentification RPC C. Pour une meilleure sécurité, envisagez d’utiliser la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C**.
    -   Définissez le niveau d’emprunt d’identité sur le niveau d’emprunt d' **\_ \_ \_ \_ identité RPC C IMP**.
    -   Définissez les fonctionnalités de sécurité de masquage sur **EOAC \_ statique**. Pour plus d’informations sur le masquage de la sécurité, consultez [masquage](../com/cloaking.md).

    L’exemple de code suivant montre comment un demandeur doit appeler [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) dans Windows 7 et windows Server 2008 R2 et versions antérieures (ou dans Windows 8 et windows server 2012 et versions ultérieures, si la compatibilité VSS n’est pas nécessaire) :

    ``` syntax
    // Initialize COM security.
       hr = CoInitializeSecurity(
            NULL,                          //  PSECURITY_DESCRIPTOR         pSecDesc,
            -1,                            //  LONG                         cAuthSvc,
            NULL,                          //  SOLE_AUTHENTICATION_SERVICE *asAuthSvc,
            NULL,                          //  void                        *pReserved1,
            RPC_C_AUTHN_LEVEL_PKT_PRIVACY, //  DWORD                        dwAuthnLevel,
            RPC_C_IMP_LEVEL_IDENTIFY,      //  DWORD                        dwImpLevel,
            NULL,                          //  void                        *pAuthList,
            EOAC_NONE,                     //  DWORD                        dwCapabilities,
            NULL                           //  void                        *pReserved3
            );
    ```

    Lors de la définition explicite de la sécurité de niveau COM d’un demandeur avec [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), vous devez effectuer les opérations suivantes :

    -   Définissez le niveau d’authentification au moins **au \_ niveau de \_ \_ \_ connexion RPC C Authn**. Pour une meilleure sécurité, envisagez d’utiliser la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC C**.
    -   Définissez le niveau d’emprunt d’identité sur **RPC \_ C \_ IMP \_ Level \_ identifier** , sauf si le processus du demandeur doit autoriser l’emprunt d’identité pour des appels RPC ou com spécifiques qui ne sont pas liés à VSS.

-   Autorisez uniquement l’accès aux processus spécifiés pour appeler le processus du demandeur.

    Un serveur COM (tel qu’un demandeur) qui appelle [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) avec un descripteur de sécurité non **null** comme premier paramètre peut utiliser le descripteur pour se configurer lui-même pour accepter les appels entrants uniquement des utilisateurs qui appartiennent à un ensemble spécifique de comptes.

    Un demandeur doit s’assurer que les clients COM s’exécutant sous des utilisateurs valides sont autorisés à appeler son processus. Un demandeur qui spécifie un descripteur de sécurité dans le premier paramètre doit autoriser les utilisateurs suivants à effectuer des appels entrants dans le processus du demandeur :

    -   Système Local
    -   Service local

        **Windows XP :** Cette valeur n’est pas prise en charge avant Windows Server 2003.

    -   Service réseau

        **Windows XP :** Cette valeur n’est pas prise en charge avant Windows Server 2003.

    -   Membres du groupe Administrateurs local
    -   Membres du groupe opérateurs de sauvegarde local
    -   Utilisateurs spéciaux spécifiés dans l’emplacement du Registre ci-dessous, avec « 1 » comme \_ valeur de Registre DWORD

## <a name="explicitly-controlling-user-account-access-to-a-requester"></a>Contrôle explicite de l’accès d’un compte d’utilisateur à un demandeur

Dans certains cas, la restriction de l’accès à un demandeur à des processus s’exécutant en tant que système local, ou sous les groupes Administrateurs locaux ou opérateurs de sauvegarde locaux, peut être trop restrictive.

Par exemple, il se peut que le processus d’un demandeur spécifié ne doive normalement pas être exécuté sous un compte d’administrateur ou d’opérateur de sauvegarde. Pour des raisons de sécurité, il est préférable de ne pas promouvoir artificiellement les privilèges de processus pour prendre en charge VSS.

Dans ces cas, vous devez modifier la clé de Registre HKEY VssAccessControl VSS du système de l' **\_ \_ ordinateur local** \\  \\  \\  \\  \\  pour indiquer à VSS qu’un utilisateur spécifié peut exécuter un demandeur VSS en toute sécurité.

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
                  MyDomain\MyUser = 2<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_DWORD</dd>
</dl>
```

Ce mécanisme peut également être utilisé pour empêcher explicitement un utilisateur autorisé à exécuter un demandeur VSS. L’exemple suivant permet de restreindre l’accès à partir du \\ compte « administrateur ThatDomain » :

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

L’administrateur ThatDomain de l’utilisateur \\ ne peut pas exécuter un demandeur VSS.

## <a name="performing-a-file-backup-of-the-system-state"></a>Exécution d’une sauvegarde de fichiers de l’état du système

Si un demandeur effectue une sauvegarde de l’état du système en sauvegardant des fichiers individuels au lieu d’utiliser une image de volume pour la sauvegarde, il doit appeler les fonctions [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) et [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) pour énumérer les liens physiques des fichiers qui se trouvent dans les répertoires suivants :

-   Windows \\ system32 \\ WDI \\ perftrack\\
-   Windows \\ WINSXS\\

Ces répertoires sont accessibles uniquement par les membres du groupe administrateurs. Pour cette raison, un tel demandeur doit s’exécuter sous le compte système ou un compte d’utilisateur membre du groupe administrateurs.

**Windows XP et Windows Server 2003 :** Les fonctions [**FindFirstFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findfirstfilenamew) et [**FindNextFileNameW**](/windows/win32/api/fileapi/nf-fileapi-findnextfilenamew) ne sont pas prises en charge jusqu’à Windows Vista et Windows Server 2008.

 

 
