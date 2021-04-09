---
description: Lorsqu’une application utilisateur demande des données à partir d’objets sur le système via un fournisseur WMI, l’emprunt d’identité signifie que le fournisseur présente des informations d’identification qui représentent le niveau de sécurité des clients plutôt que les fournisseurs.
ms.assetid: 6d54f234-45aa-445b-ad50-7d5a9946c134
ms.tgt_platform: multiple
title: Emprunt de l’identité d’un client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 162857d90c8bddb70d90eb2e10efbc08537299d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866889"
---
# <a name="impersonating-a-client"></a>Emprunt de l’identité d’un client

Lorsqu’une application utilisateur demande des données à partir d’objets sur le système par le biais d’un fournisseur WMI, l’emprunt d’identité signifie que le fournisseur présente des informations d’identification qui représentent le niveau de sécurité du client plutôt que le du fournisseur. L’emprunt d’identité empêche un client d’obtenir un accès non autorisé aux informations sur le système.

Les sections suivantes sont présentées dans cette rubrique :

-   [Inscription d’un fournisseur pour l’emprunt d’identité](#registering-a-provider-for-impersonation)
-   [Définition des niveaux d’emprunt d’identité dans un fournisseur](#setting-impersonation-levels-within-a-provider)
-   [Maintenance des niveaux de sécurité dans un fournisseur](#maintaining-security-levels-in-a-provider)
-   [Gestion des messages d’accès refusé dans un fournisseur](#handling-access-denied-messages-in-a-provider)
-   [Création de rapports sur des instances partielles](#reporting-partial-instances)
-   [Création de rapports d’énumérations partielles](#reporting-partial-enumerations)
-   [Débogage de votre code d’accès refusé](#debugging-your-access-denied-code)
-   [Rubriques connexes](#related-topics)

WMI s’exécute généralement en tant que service administratif à un niveau de sécurité élevé, à l’aide du contexte de sécurité LocalServer. L’utilisation d’un service administratif permet à WMI d’accéder aux informations privilégiées. Lors de l’appel d’un fournisseur pour plus d’informations, WMI transmet son identificateur de sécurité (SID) au fournisseur, ce qui permet au fournisseur d’accéder aux informations au même niveau de sécurité élevé.

Durant le processus de lancement de l’application WMI, le système d’exploitation Windows donne à l’application WMI le contexte de sécurité de l’utilisateur qui a commencé le processus. Le contexte de sécurité de l’utilisateur est généralement un niveau de sécurité inférieur à LocalServer. il est donc possible que l’utilisateur n’ait pas l’autorisation d’accéder à toutes les informations disponibles pour WMI. Lorsque l’application utilisateur demande des informations dynamiques, WMI transmet le SID de l’utilisateur au fournisseur correspondant. En cas d’écriture appropriée, le fournisseur tente d’accéder aux informations avec le SID de l’utilisateur, plutôt que le SID du fournisseur.

Pour que le fournisseur emprunte correctement l’identité de l’application cliente, l’application cliente et le fournisseur doivent répondre aux critères suivants :

-   L’application cliente doit appeler WMI avec un niveau de sécurité de connexion COM de la connexion **RPC \_ c \_ IMP \_ Level \_ Impersonate** ou **RPC \_ c \_ IMP \_ Level \_ Delegate**. Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).
-   Le fournisseur doit s’inscrire auprès de WMI en tant que fournisseur d’emprunt d’identité. Pour plus d’informations, consultez [inscription d’un fournisseur pour l’emprunt d’identité](#registering-a-provider-for-impersonation).
-   Le fournisseur doit basculer vers le niveau de sécurité de l’application cliente avant d’accéder aux informations privilégiées. Pour plus d’informations, consultez [définition de niveaux d’emprunt d’identité au sein d’un fournisseur](#setting-impersonation-levels-within-a-provider).
-   Le fournisseur doit gérer correctement les conditions d’erreur si l’accès à ces informations est refusé. Pour plus d’informations, consultez [gestion des messages d’accès refusé dans un fournisseur](#handling-access-denied-messages-in-a-provider).

## <a name="registering-a-provider-for-impersonation"></a>Inscription d’un fournisseur pour l’emprunt d’identité

WMI ne transmet le SID d’une application cliente qu’aux fournisseurs qui se sont inscrits en tant que fournisseurs d’emprunt d’identité. Pour permettre à un fournisseur d’effectuer l’emprunt d’identité, vous devez modifier le processus d’inscription du fournisseur.

La procédure suivante décrit comment inscrire un fournisseur pour l’emprunt d’identité. La procédure suppose que vous comprenez déjà le processus d’inscription. Pour plus d’informations sur le processus d’inscription, consultez [inscription d’un fournisseur](registering-a-provider.md).

**Pour inscrire un fournisseur pour l’emprunt d’identité**

1.  Affectez la valeur 1 à la propriété [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) de la classe [**\_ \_ Win32Provider**](--win32provider.md) qui représente votre fournisseur.

    La propriété [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) indique si le fournisseur prend en charge l’emprunt d’identité ou non. L’affectation de la valeur 0 à **ImpersonationLevel** indique que le fournisseur n’emprunte pas l’identité du client et effectue toutes les opérations demandées dans le même contexte utilisateur que WMI. L’affectation de la valeur 1 à **ImpersonationLevel** indique que le fournisseur utilise des appels d’emprunt d’identité pour vérifier les opérations effectuées pour le compte du client.

2.  Affectez la valeur **true** à la propriété **PerUserInitialization** de la même classe [**\_ \_ Win32Provider**](--win32provider.md) .

> [!Note]  
> Si vous inscrivez un fournisseur avec la propriété [**\_ \_ Win32Provider**](--win32provider.md) **InitializeAsAdminFirst** définie sur **true**, le fournisseur utilise le jeton de sécurité de thread de niveau administration uniquement pendant la phase d’initialisation. Lorsqu’un appel à [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) n’échoue pas, le fournisseur utilise le contexte de sécurité de WMI et non du client.

 

L’exemple de code suivant montre comment inscrire un fournisseur pour l’emprunt d’identité.

``` syntax
instance of __Win32Provider
{
    CLSID = "{FD4F53E0-65DC-11d1-AB64-00C04FD9159E}";
    ImpersonationLevel = 1;
    Name = "MS_NT_EVENTLOG_PROVIDER";
    PerUserInitialization = TRUE;
};
```

## <a name="setting-impersonation-levels-within-a-provider"></a>Définition des niveaux d’emprunt d’identité dans un fournisseur

Si vous inscrivez un fournisseur avec la propriété de classe [**\_ \_ Win32Provider**](--win32provider.md) [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md) définie sur 1, WMI appelle votre fournisseur pour emprunter l’identité de différents clients. Pour gérer ces appels, utilisez les fonctions com [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) et [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) dans votre implémentation de l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

La fonction [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) permet à un serveur d’emprunter l’identité du client qui a effectué l’appel. En plaçant un appel à **CoImpersonateClient** dans votre implémentation de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices), vous autorisez votre fournisseur à définir le jeton de thread du fournisseur pour qu’il corresponde au jeton de thread du client, et donc emprunter l’identité du client. Si vous n’appelez pas **CoImpersonateClient**, votre fournisseur exécute le code à un niveau de sécurité administrateur, ce qui crée une faille de sécurité potentielle. Si votre fournisseur doit temporairement agir en tant qu’administrateur ou effectuer la vérification d’accès manuellement, appelez [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself).

Contrairement à [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient), [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) est une fonction com qui gère les niveaux d’emprunt d’identité de thread. Dans ce cas, **CoRevertToSelf** remplace le niveau d’emprunt d’identité par le paramètre d’emprunt d’identité d’origine. En général, le fournisseur est initialement un administrateur et alterne entre **CoImpersonateClient** et **CoRevertToSelf** , selon qu’il s’agit d’un appel qui représente l’appelant ou ses propres appels. Il incombe au fournisseur de placer correctement ces appels afin de ne pas exposer de faille de sécurité à l’utilisateur final. Par exemple, le fournisseur doit uniquement appeler des fonctions Windows natives dans la séquence de code empruntée.

> [!Note]  
> L’objectif de [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) et [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself) est de définir la sécurité d’un fournisseur. Si vous déterminez que l’emprunt d’identité a échoué, vous devez retourner un code d’achèvement approprié à WMI via [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Pour plus d’informations, consultez [gestion des messages d’accès refusé dans un fournisseur](#handling-access-denied-messages-in-a-provider).

 

## <a name="maintaining-security-levels-in-a-provider"></a>Maintenance des niveaux de sécurité dans un fournisseur

Les fournisseurs ne peuvent pas appeler [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) une fois dans une implémentation de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) et supposent que les informations d’identification d’emprunt d’identité restent en place pendant la durée du fournisseur. Au lieu de cela, appelez **CoImpersonateClient** plusieurs fois au cours d’une implémentation pour empêcher WMI de modifier les informations d’identification.

La principale préoccupation pour la définition de l’emprunt d’identité pour un fournisseur est la réentrance. Dans ce contexte, la réentrance est lorsqu’un fournisseur effectue un appel à WMI pour obtenir des informations et attend jusqu’à ce que WMI rappelle le fournisseur. En résumé, le thread d’exécution quitte le code du fournisseur, uniquement pour entrer à nouveau le code à une date ultérieure. La réentrance fait partie de la conception de COM et n’est généralement pas un problème. Toutefois, lorsque le thread d’exécution entre dans WMI, le thread prend les niveaux d’emprunt d’identité de WMI. Lorsque le thread revient au fournisseur, vous devez réinitialiser les niveaux d’emprunt d’identité avec un autre appel à [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient).

Pour vous protéger contre les failles de sécurité de votre fournisseur, vous devez faire en sorte que les appels réentrants dans WMI s’effectuent uniquement lors de l’emprunt d’identité du client. Autrement dit, les appels à WMI doivent être effectués après l’appel de [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) et avant l’appel de [**CoRevertToSelf**](/windows/win32/api/combaseapi/nf-combaseapi-coreverttoself). Étant donné que **CoRevertToSelf** provoque l’utilisation de l’emprunt d’identité au niveau de l’utilisateur, le WMI est en cours d’exécution, généralement LocalSystem, les appels réentrants à WMI après l’appel de **CoRevertToSelf** peuvent permettre à l’utilisateur et à tous les fournisseurs appelés de bénéficier d’un plus grand nombre de fonctionnalités.

> [!Note]  
> Si vous appelez une fonction système ou une autre méthode d’interface, le maintien du contexte d’appel n’est pas garanti.

 

## <a name="handling-access-denied-messages-in-a-provider"></a>Gestion des messages d’accès refusé dans un fournisseur

La plupart des messages d’erreur d’accès refusé s’affichent lorsqu’un client demande une classe ou des informations auxquelles ils n’ont pas accès. Si le fournisseur renvoie un message d’erreur Accès refusé à WMI et que WMI le transmet au client, le client peut déduire que les informations existent. Dans certains cas, il peut s’agir d’une violation de la sécurité. Par conséquent, votre fournisseur ne doit pas propager le message au client. Au lieu de cela, l’ensemble de classes que le fournisseur aurait fourni ne doit pas être exposé. De même, un fournisseur d’instances dynamiques doit appeler la source de données sous-jacente pour déterminer comment traiter les messages d’accès refusé. Il incombe au fournisseur de répliquer cette philosophie dans l’environnement WMI. Pour plus d’informations, consultez Création de rapports sur des [instances partielles](#reporting-partial-instances) et [création de rapports d’énumérations partielles](#reporting-partial-enumerations).

Lorsque vous déterminez comment votre fournisseur doit gérer les messages d’accès refusé, vous devez écrire et déboguer votre code. Lors du débogage, il est souvent pratique de faire la distinction entre un refus en raison d’un faible emprunt d’identité et un refus en raison d’une erreur dans votre code. Vous pouvez utiliser un test simple dans votre code pour déterminer la différence. Pour plus d’informations, consultez [débogage de votre code d’accès refusé](#debugging-your-access-denied-code).

## <a name="reporting-partial-instances"></a>Création de rapports sur des instances partielles

Une occurrence courante d’un message de refus d’accès se produit lorsque WMI ne peut pas fournir toutes les informations pour remplir une instance. Par exemple, un client peut disposer de l’autorité nécessaire pour afficher un objet lecteur de disque dur, mais il n’a peut-être pas l’autorisation de voir la quantité d’espace disponible sur le disque dur. Votre fournisseur doit déterminer comment gérer toute situation dans laquelle le fournisseur ne peut pas remplir complètement une instance avec des propriétés en raison d’une violation d’accès.

WMI ne nécessite pas de réponse unique aux clients qui ont un accès partiel à une instance. Au lieu de cela, la version 1. x de WMI autorise le fournisseur à l’une des options suivantes :

-   Échec de la totalité de l’opération avec l' **\_ accès WBEM E \_ \_ refusé** et ne renvoyant aucune instance.

    Retourne un objet d’erreur avec **l' \_ accès WBEM E \_ \_ refusé** pour décrire la raison du refus.

-   Retourne toutes les propriétés disponibles et remplit les propriétés non disponibles avec la **valeur null**.

> [!Note]  
> Assurez-vous que le renvoi de l' **\_ accès WBEM E \_ \_ refusé** ne crée pas de faille de sécurité dans votre entreprise.

 

## <a name="reporting-partial-enumerations"></a>Création de rapports d’énumérations partielles

Une autre occurrence courante d’une violation d’accès se produit lorsque WMI ne peut pas retourner toute une énumération. Par exemple, un client peut avoir accès à l’affichage de tous les objets ordinateur du réseau local, mais il n’a peut-être pas l’accès pour afficher les objets ordinateur en dehors de son domaine. Votre fournisseur doit déterminer comment gérer toute situation dans laquelle une énumération ne peut pas être effectuée en raison d’une violation d’accès.

Comme avec un fournisseur d’instances, WMI ne requiert pas une seule réponse à une énumération partielle. Au lieu de cela, la version 1. x de WMI permet à un fournisseur d’obtenir l’une des options suivantes :

-   Retourne **WBEM \_ S \_ aucune \_ erreur** pour toutes les instances auxquelles le fournisseur peut accéder.

    Si vous utilisez cette option, l’utilisateur n’a pas conscience que certaines instances n’étaient pas disponibles. Un certain nombre de fournisseurs, tels que ceux qui utilisent des langage SQL (SQL) avec la sécurité au niveau des lignes, retournent des résultats partiels réussis en utilisant le niveau de sécurité de l’appelant pour définir le jeu de résultats.

-   Échec de la totalité de l’opération avec l' **\_ accès WBEM E \_ \_ refusé** et ne renvoyant aucune instance.

    Le fournisseur peut éventuellement inclure un objet d’erreur qui décrit la situation au client. Notez que certains fournisseurs peuvent accéder aux sources de données en série et peuvent ne pas rencontrer de refus jusqu’à la partie de l’énumération.

-   Retourne toutes les instances accessibles, mais retourne également le code d’État non erreur **\_ accès WBEM S \_ \_ refusé**.

    Le fournisseur doit noter le refus au cours de l’énumération et peut continuer à fournir des instances, en se terminant par le code d’état des erreurs. Le fournisseur peut également choisir de terminer l’énumération au premier refus. La justification de cette option est que les différents fournisseurs ont des paradigmes de récupération différents. Un fournisseur a peut-être déjà fourni des instances avant de découvrir une violation d’accès. Certains fournisseurs peuvent choisir de continuer à fournir d’autres instances et d’autres peuvent souhaiter se terminer.

En raison de la structure de COM, vous ne pouvez pas marshaler les informations pendant une erreur à l’exception d’un objet d’erreur. Par conséquent, vous ne pouvez pas retourner à la fois les informations et un code d’erreur. Si vous choisissez de retourner des informations, vous devez utiliser un code d’état de non-erreur.

## <a name="debugging-your-access-denied-code"></a>Débogage de votre code d’accès refusé

Certaines applications peuvent utiliser des niveaux d’emprunt d’identité inférieurs à l' **\_ emprunt d' \_ \_ \_ identité RPC C IMP**. Dans ce cas, la plupart des appels d’emprunt d’identité effectués par le fournisseur pour l’application cliente échouent. Pour concevoir et implémenter un fournisseur avec succès, vous devez garder cette idée à l’esprit.

Par défaut, le seul autre niveau d’emprunt d’identité qui peut accéder à un fournisseur est **RPC \_ C \_ IMP \_ Level \_ identifier**. Dans les cas où une application cliente utilise l' **\_ \_ \_ \_ identifiant RPC C IMP Level**, [**CoImpersonateClient**](/windows/win32/api/combaseapi/nf-combaseapi-coimpersonateclient) ne retourne pas de code d’erreur. Au lieu de cela, le fournisseur emprunte l’identité du client à des fins d’identification uniquement. Par conséquent, la plupart des méthodes Windows appelées par le fournisseur renverront un message d’accès refusé. Cela n’est pas sans conséquence dans la pratique, car les utilisateurs ne sont pas autorisés à faire quelque chose d’inapproprié. Toutefois, il peut être utile pendant le développement du fournisseur de savoir si le client a fait l’emprunt d’identité ou non.

Le code requiert les références suivantes et les \# instructions include pour être compilées correctement.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
```



L’exemple de code suivant montre comment déterminer si un fournisseur a correctement emprunté une application cliente.


```C++
DWORD dwImp = 0;
HANDLE hThreadTok;
DWORD dwBytesReturned;
BOOL bRes;

// You must call this before trying to open a thread token!
CoImpersonateClient();

bRes = OpenThreadToken(
    GetCurrentThread(),
    TOKEN_QUERY,
    TRUE,
    &hThreadTok
);

if (bRes == FALSE)
{
    printf("Unable to read thread token (%d)\n", GetLastError());
    return 0;
}

bRes = GetTokenInformation(
    hThreadTok,
    TokenImpersonationLevel, 
    &dwImp,
    sizeof(DWORD),
    &dwBytesReturned
);

if (!bRes)
{
    printf("Unable to read impersonation level\n");
    CloseHandle(hThreadTok);
    return 0;
}

switch (dwImp)
{
case SecurityAnonymous:
    printf("SecurityAnonymous\n");
    break;

case SecurityIdentification:
    printf("SecurityIdentification\n");
    break;

case SecurityImpersonation:
    printf("SecurityImpersonation\n");
    break;

case SecurityDelegation:
    printf("SecurityDelegation\n");
    break;

default:
    printf("Error. Unable to determine impersonation level\n");
    break;
}

CloseHandle(hThreadTok);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sécurisation de votre fournisseur](securing-your-provider.md)
</dt> </dl>

 

 
