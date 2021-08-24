---
description: Les applications WMI écrites en C++ peuvent effectuer des appels asynchrones à l’aide de nombreuses méthodes de l’interface COM IWbemServices.
ms.assetid: 5179969f-bc7d-4408-84ef-7b003950a59f
ms.tgt_platform: multiple
title: Exécution d’un appel asynchrone avec C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd988382399f3fc377476c486b363cf51db6c4d9ef559c787236e41bb74117a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131191"
---
# <a name="making-an-asynchronous-call-with-c"></a>Exécution d’un appel asynchrone avec C++

Les applications WMI écrites en C++ peuvent effectuer des appels asynchrones à l’aide de nombreuses méthodes de l’interface com [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . Toutefois, la procédure recommandée pour appeler une [*méthode WMI*](gloss-w.md) ou un [*fournisseur*](gloss-p.md) consiste à utiliser des appels semi-synchrones, car les appels semi-synchrones sont plus sûrs que les appels asynchrones. Pour plus d’informations, consultez [création d’un appel semi-synchrone avec C++](making-a-semisynchronous-call-with-c--.md) et [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

La procédure suivante décrit comment effectuer un appel asynchrone à l’aide du récepteur dans votre processus.

**Pour effectuer un appel asynchrone à l’aide de C++**

1.  Implémentez l’interface [**IWbemObjectSink**](iwbemobjectsink.md) .

    Toutes les applications qui effectuent des appels asynchrones doivent implémenter [**IWbemObjectSink**](iwbemobjectsink.md). Les consommateurs d’événements temporaires implémentent également **IWbemObjectSink** pour recevoir des notifications d’événements.

2.  Connectez-vous à l’espace de noms WMI cible.

    Les applications doivent toujours appeler la fonction COM [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) lors de la phase d’initialisation. Si ce n’est pas le cas avant d’effectuer un appel asynchrone, WMI libère le récepteur d’application sans terminer l’appel asynchrone. Pour plus d’informations, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).

3.  Définissez la sécurité de votre récepteur.

    Les appels asynchrones créent un grand nombre de problèmes de sécurité que vous devrez peut-être gérer, par exemple, en autorisant l’accès WMI à votre application. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

4.  Effectuez l’appel asynchrone.

    La méthode est retournée immédiatement avec l’absence de code de réussite des **\_ \_ \_ Erreurs WBEM** . L’application peut effectuer d’autres tâches en attendant que l’opération se termine. WMI renvoie à l’application en appelant des méthodes dans l’implémentation [**IWbemObjectSink**](iwbemobjectsink.md) de votre application.

5.  Si nécessaire, vérifiez régulièrement votre mise en œuvre des mises à jour.

    Les applications peuvent recevoir une notification d’état intermédiaire en définissant le paramètre *lFlags* dans l’appel asynchrone de l’état d’envoi de l' **\_ indicateur \_ \_ WBEM**. WMI signale l’état de votre appel en définissant le paramètre *lFlags* de [**IWbemObjectSink**](iwbemobjectsink.md) sur **WBEM \_ Status \_ Progress**.

6.  Si nécessaire, vous pouvez annuler l’appel avant que WMI termine le traitement en appelant la méthode [**IWbemServices :: CancelCallAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) .

    La méthode [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) annule le traitement asynchrone en libérant immédiatement le pointeur vers l’interface [**IWbemObjectSink**](iwbemobjectsink.md) et garantit que le pointeur est libéré avant que **CancelAsyncCall** retourne.

    Si vous utilisez un objet wrapper qui implémente l’interface **IUnsecured** pour héberger des [**IWbemObjectSink**](iwbemobjectsink.md), vous risquez de rencontrer des complications supplémentaires. Étant donné que l’application doit passer le même pointeur à [**CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) qui a été passé dans l’appel asynchrone d’origine, l’application doit conserver l’objet de wrapper jusqu’à ce qu’il soit clair que l’annulation n’est pas nécessaire. Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).

7.  Lorsque vous avez terminé, nettoyez les pointeurs et arrêtez l’application.

    WMI fournit l’appel d’état final par le biais de la méthode [**SetStatus**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus) .

    > [!Note]  
    > Après l’envoi de la dernière mise à jour d’État, WMI libère le récepteur d’objets en appelant la méthode **Release** pour la classe qui implémente l’interface [**IWbemObjectSink**](iwbemobjectsink.md) . Dans l’exemple précédent, il s’agit de la méthode **QuerySink :: Release** . Si vous souhaitez contrôler la durée de vie de l’objet récepteur, vous pouvez implémenter le récepteur avec un nombre de références initial de un (1).

     

    Si une application cliente passe la même interface de récepteur dans deux appels asynchrones différents qui se chevauchent, WMI ne garantit pas l’ordre du rappel. Une application cliente qui effectue des appels asynchrones qui se chevauchent doit passer différents objets récepteur ou sérialiser les appels.

L’exemple suivant requiert la référence et les \# instructions include suivantes.


```C++
#include <iostream>
using namespace std;
#pragma comment(lib, "wbemuuid.lib")
#include <wbemidl.h>
```



L’exemple suivant décrit comment créer une requête asynchrone à l’aide de la méthode [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) , mais ne crée pas de paramètres de sécurité ou ne libère pas l’objet [**IWbemObjectSink**](iwbemobjectsink.md) . Pour plus d’informations, consultez [définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md).


```C++
// Set input parameters to ExecQueryAsync.
BSTR QueryLang = SysAllocString(L"WQL");
BSTR Query = SysAllocString(L"SELECT * FROM MyClass");

// Create IWbemObjectSink object and set pointer.
QuerySink *pSink = new QuerySink;

IWbemServices* pSvc = 0;

// Call ExecQueryAsync.
HRESULT hRes = pSvc->ExecQueryAsync(QueryLang, 
                                    Query, 
                                    0, 
                                    NULL, 
                                    pSink);

// Check for errors.
if (hRes)
{
    printf("ExecQueryAsync failed with = 0x%X\n", hRes);
    SysFreeString(QueryLang);
    SysFreeString(Query);
    delete pSink;    
    return ERROR;
}
```



> [!Note]  
> Le code ci-dessus ne se compile pas sans erreur, car la classe **QuerySink** n’a pas été définie. Pour plus d’informations sur **QuerySink**, consultez [**IWbemObjectSink**](iwbemobjectsink.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

 
