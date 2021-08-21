---
description: Les consommateurs temporaires et permanents ont des méthodes différentes pour sécuriser la remise des événements.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Réception des événements en toute sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64db5b0289abd9a43caee6ddb3b68da94a9560b0ea8f591d95ee472cf900b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316526"
---
# <a name="receiving-events-securely"></a>Réception des événements en toute sécurité

Les consommateurs temporaires et permanents ont des méthodes différentes pour sécuriser la remise des événements.

Les sections suivantes sont présentées dans cette rubrique :

-   [Sécurisation des consommateurs temporaires](#securing-temporary-consumers)
-   [Sécurisation des consommateurs permanents](#securing-permanent-consumers)
-   [Sécurisation de l’abonnement permanent](#securing-the-permanent-subscription)
-   [Définition d’une Administrator-Only SD](#setting-an-administrator-only-sd)
-   [Emprunt de l’identité du fournisseur d’événements](#impersonating-the-event-provider-identity)
-   [Sid et abonnements permanents](#sids-and-permanent-subscriptions)
-   [Création d’abonnements permanents à l’aide de comptes de domaine](#creating-permanent-subscriptions-using-domain-accounts)
-   [Rubriques connexes](#related-topics)

## <a name="securing-temporary-consumers"></a>Sécurisation des consommateurs temporaires

Un [*consommateur temporaire*](gloss-t.md) s’exécute jusqu’à ce que le système soit redémarré ou que WMI soit arrêté, mais ne peut pas être démarré si un événement spécifique est déclenché. Par exemple, un appel à [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) crée un consommateur temporaire.

Les appels [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) ou [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) créent des consommateurs d’événements temporaires. Les consommateurs temporaires ne peuvent pas contrôler qui fournit des événements au [*récepteur*](gloss-s.md) d’événements qu’ils créent.

Les appels aux méthodes [**ExecNotificationQuery**](swbemservices-execnotificationquery.md) peuvent être effectués de façon synchrone, [*semisynchronously*](gloss-s.md)ou asynchrone. Par exemple, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) est une méthode synchrone qui peut être appelée semisynchronously, en fonction de la façon dont le paramètre *IFlags* est défini. [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) est un appel asynchrone.

N’oubliez pas que le rappel au récepteur pour les versions asynchrones de ces appels peut ne pas être retourné au même niveau d’authentification que l’appel effectué par le script. Par conséquent, il est recommandé d’utiliser des appels semi-synchrones au lieu d’appels asynchrones. Si vous avez besoin d’une communication asynchrone, consultez [appel d’une méthode](calling-a-method.md) et [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

Les abonnés de script ne peuvent pas vérifier les droits d’accès d’un fournisseur d’événements pour fournir des événements au récepteur créé par le script. Par conséquent, il est recommandé que les appels à [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) utilisent la forme semi-synchrone de l’appel et utilisent des paramètres de sécurité spécifiques. Pour plus d’informations, consultez [création d’un appel semi-synchrone avec VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="securing-permanent-consumers"></a>Sécurisation des consommateurs permanents

Un [*consommateur permanent*](gloss-p.md) dispose d’un abonnement permanent aux événements d’un fournisseur d’événements qui est conservé après le redémarrage du système d’exploitation. Un fournisseur d’événements qui prend en charge les consommateurs permanents est un [*fournisseur de consommateur d’événements*](gloss-e.md). Si le fournisseur d’événements n’est pas en cours d’exécution lorsqu’un événement se produit, WMI démarre le fournisseur lorsqu’il doit remettre des événements. WMI identifie le fournisseur de consommateurs auquel les événements doivent être remis, en fonction de l’instance [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , qui associe l’instance [**\_ \_ Win32Provider**](--win32provider.md) du fournisseur de consommateurs à une [*classe de consommateur logique*](gloss-l.md) définie par le fournisseur de consommateur. Pour plus d’informations sur le rôle des fournisseurs de consommateurs, consultez [écriture d’un fournisseur de consommateur d’événements](writing-an-event-consumer-provider.md).

Les consommateurs permanents peuvent contrôler qui leur envoie des événements et les fournisseurs d’événements peuvent contrôler les utilisateurs qui accèdent à leurs événements.

Les applications et les scripts clients créent des instances de la classe de consommateur logique dans le cadre d’un abonnement. La classe de consommateur logique définit les informations contenues dans l’événement, ce que le client peut faire avec l’événement et comment l’événement est remis.

Les [classes de consommateur standard](standard-consumer-classes.md) WMI fournissent des exemples du rôle des classes de consommateur logiques. Pour plus d’informations, consultez [surveillance et réponse aux événements avec des consommateurs standard](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="securing-the-permanent-subscription"></a>Sécurisation de l’abonnement permanent

Les abonnements permanents sont plus susceptibles de provoquer des problèmes de sécurité dans WMI et présentent donc les exigences de sécurité suivantes :

-   L’instance de consommateur logique, le [**\_ \_ EventFilter**](--eventfilter.md)et les instances [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) doivent avoir le même identificateur de sécurité (SID) individuel dans la propriété **CreatorSID** . Pour plus d’informations, consultez [conserver le même sid dans toutes les instances d’un abonnement permanent](#sids-and-permanent-subscriptions).
-   Le compte qui crée l’abonnement doit être un compte de domaine disposant de privilèges d’administrateur local ou du compte de groupe Administrateurs local. L’utilisation du SID du groupe administrateurs permet à l’abonnement de continuer à fonctionner sur l’ordinateur local, même s’il est déconnecté du réseau. L’utilisation d’un compte de domaine permet l’identification exacte de l’utilisateur.

    Toutefois, si l’ordinateur n’est pas connecté et que le compte de création est un compte de domaine, le consommateur échoue, car WMI ne peut pas vérifier l’identité du compte. Pour éviter l’échec de l’abonnement si l’ordinateur est déconnecté du réseau, utilisez le SID du groupe administrateurs pour un abonnement. Dans ce cas, vous devez vous assurer que le compte LocalSystem peut accéder aux données d’appartenance au groupe sur le domaine. Certains fournisseurs de consommateurs d’événements ont des exigences particulièrement élevées en matière de sécurité, car un abonnement non autorisé peut causer des dommages importants. Exemples : consommateurs standard, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) et [**CommandLineEventConsumer**](commandlineeventconsumer.md).

-   Vous pouvez configurer l’abonnement permanent pour accepter uniquement les événements provenant d’identités de fournisseur d’événements spécifiques. Définissez le descripteur de sécurité dans la propriété **EventAccess** de l’instance [**\_ \_ EventFilter**](--eventfilter.md) sur les identités du fournisseur d’événements. WMI compare l’identité du fournisseur d’événements au descripteur de sécurité pour déterminer si le fournisseur dispose de l’accès de **\_ \_ publication WBEM approprié** . Pour plus d’informations, consultez [constantes de sécurité WMI](wmi-security-constants.md).

    Si le filtre autorise l’accès à l’identité du fournisseur d’événements, il approuve également l’événement. Cela permet au consommateur qui a reçu l’événement de déclencher un événement délégué.

    **Remarque**  La valeur par défaut du descripteur de sécurité dans **EventAccess** est **null**, ce qui permet d’accéder à tout le monde. La limitation de l’accès à l’instance d’abonnement de [**\_ \_ EventFilter**](--eventfilter.md) est recommandée pour une meilleure sécurité des événements.

## <a name="setting-an-administrator-only-sd"></a>Définition d’une Administrator-Only SD

L’exemple de code C++ suivant crée un descripteur de sécurité administrateur uniquement sur l’instance [**\_ \_ EventFilter**](--eventfilter.md) . Cet exemple crée le descripteur de sécurité à l’aide du langage SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ). Pour plus d’informations sur l' **\_ \_ abonnement WBEM correct**, consultez [constantes de sécurité WMI](wmi-security-constants.md).


```C++
// Create SD that allows only administrators 
//    to send events to this filter. 
// The SDDL settings are O:BAG:BAD:(A;;0x80;;;BA)
// Set the EventAccess property in the 
//    IWbemClassObject of the __EventFilter instance. 
   long lMask = WBEM_RIGHT_PUBLISH;
     WCHAR wBuf[MAX_PATH];
     _ltow( lMask, wBuf, 16 );
 
HRESULT hRes = pEventFilterInstance->Put( L"EventAccess", 0,
    &_variant_t( L"O:BAG:BAD:(A;;0x80;;;BA)" ), NULL );
```



L’exemple de code précédent requiert la référence et les \# instructions include suivantes.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>Emprunt de l’identité du fournisseur d’événements

Un consommateur permanent peut avoir besoin d’emprunter l’identité du fournisseur d’événements pour traiter l’événement. Les consommateurs permanents peuvent emprunter l’identité du fournisseur d’événements uniquement lorsque les conditions suivantes sont réunies :

-   La propriété **MaintainSecurityContext** de l’instance de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) a la valeur **true**.
-   Un événement est remis dans le même contexte de sécurité que celui dans lequel se trouvait le fournisseur lorsqu’il a généré l’événement. Seul un consommateur implémenté en tant que DLL, un consommateur in-process, peut recevoir des événements dans le contexte de sécurité du fournisseur. Pour plus d’informations sur la sécurité des fournisseurs et des consommateurs in-process, consultez [hébergement et sécurité des fournisseurs](provider-hosting-and-security.md).
-   Le fournisseur d’événements s’exécute dans un processus qui autorise l’emprunt d’identité.

Le compte qui exécute le processus de consommateur doit avoir un accès en **\_ écriture complet** à l’espace de stockage WMI (également connu sous le nom de référentiel CIM). Dans l’abonnement, les instances [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)et [**\_ \_ EventFilter**](--eventfilter.md) doivent avoir la même valeur d’identificateur de sécurité (SID) dans la propriété **CreatorSID** . WMI stocke le SID dans **CreatorSID** pour chaque instance.

## <a name="sids-and-permanent-subscriptions"></a>Sid et abonnements permanents

Un abonnement permanent ne fonctionne pas lorsque la liaison, le consommateur et le filtre ne sont pas créés par le même utilisateur, ce qui signifie que les [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)et [**\_ \_ EventFilter**](--eventfilter.md) doivent avoir la même valeur d’identificateur de sécurité (SID) individuelle dans la propriété **CreatorSID** . Windows WMI (Management Instrumentation) stocke cette valeur.

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>Création d’abonnements permanents à l’aide de comptes de domaine

Plusieurs problèmes doivent être pris en compte lors de l’utilisation de comptes de domaine pour créer des abonnements permanents. Chaque abonnement permanent doit toujours fonctionner quand aucun utilisateur n’est connecté, ce qui signifie qu’il fonctionne sous le compte LocalSystem intégré.

Si un utilisateur de domaine est le créateur d’un abonnement permanent pour les consommateurs sensibles à la sécurité ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), WMI vérifie si la propriété **CreatorSID** de la classe [**\_ \_ EventFilter**](--eventfilter.md) , la classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) et les instances de consommateur appartiennent à un utilisateur membre du groupe Administrateurs local.

L’exemple de code suivant montre comment vous pouvez spécifier la propriété **CreatorSID** .

``` syntax
 instance of __EventFilter as $FILTER
    {
        // this is the Administrators SID in array of bytes format
        CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};    
        // Add filter code here ...
    }

    instance of ActiveScriptEventConsumer as $CONSUMER
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       // Add consumer code here ...
    }

    instance of __FilterToConsumerBinding
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       Consumer = $CONSUMER;
       Filter = $FILTER;
       // Add binding code here ...
    }
```

pour les situations inter-domaines, ajoutez des utilisateurs authentifiés au « Windows groupe d’accès d’autorisation ».

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurisation des événements WMI](securing-wmi-events.md)
</dt> <dt>

[Réception d’un événement WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
