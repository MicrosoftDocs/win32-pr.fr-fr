---
description: 'Les appels semi-synchrones sont les moyens recommandés pour appeler des méthodes WMI, telles que IWbemServices :: ExecMethod et des méthodes de fournisseur, telles que la méthode CHKDSK de la \_ classe disque logique Win32.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Appel semi-synchrone avec C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529614"
---
# <a name="making-a-semisynchronous-call-with-c"></a>Appel semi-synchrone avec C++

Les appels semi-synchrones sont les moyens recommandés pour appeler des méthodes WMI, telles que [**IWbemServices :: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) et des méthodes de fournisseur, telles que la [**méthode CHKDSK de la \_ classe disque logique Win32**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).

L’un des inconvénients du traitement synchrone est que le thread appelant est bloqué jusqu’à ce que l’appel se termine. Le blocage peut entraîner un retard dans le temps de traitement. En revanche, un appel asynchrone doit implémenter [**SWbemSink**](swbemsink.md) dans le script. En C++, le code asynchrone doit implémenter l’interface [**IWbemObjectSink**](iwbemobjectsink.md) , utiliser plusieurs threads et contrôler le flux d’informations vers l’appelant. Les jeux de résultats volumineux des requêtes, par exemple, peuvent prendre beaucoup de temps pour remettre et obliger l’appelant à consacrer des ressources système significatives pour gérer la remise.

Le traitement semi-synchrone résout les problèmes de blocage de thread et de remise non contrôlée en interrogeant un objet d’état spécial qui implémente l’interface [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) . Grâce à **IWbemCallResult**, vous pouvez améliorer la vitesse et l’efficacité des requêtes, des énumérations et des notifications d’événements.

La procédure suivante décrit comment effectuer un appel semi-synchrone avec l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

**Pour effectuer un appel semi-synchrone avec l’interface IWbemServices**

1.  Transformez votre appel en mode normal, mais avec l' **\_ indicateur WBEM \_ retourner \_ immédiatement** l’indicateur défini dans le paramètre *IFlags* .

    Vous pouvez combiner **\_ immédiatement l’indicateur WBEM \_ Return \_** avec d’autres indicateurs qui sont valides pour la méthode spécifique. Par exemple, utilisez l' **indicateur \_ WBEM \_ Forward \_ only uniquement** pour tous les appels qui retournent des énumérateurs. La définition de ces indicateurs en combinaison permet de gagner du temps et de l’espace et d’améliorer la réactivité.

2.  Interrogez vos résultats.

    Si vous appelez une méthode qui retourne un énumérateur, tel que [**IWbemServices :: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) ou [**IWbemServices :: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), vous pouvez interroger les énumérateurs avec les méthodes [**IEnumWbemClassObject :: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) ou [**IEnumWbemClassObject :: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) . L’appel de **IEnumWbemClassObject :: NextAsync** est non bloquant et est retourné immédiatement. En arrière-plan, WMI commence à remettre le nombre demandé d’objets en appelant [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate). WMI s’arrête et attend un autre appel **NextAsync** .

    Si vous appelez une méthode qui ne retourne pas d’énumérateur, telle que [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), vous devez définir le paramètre *ppCallResult* sur un pointeur valide. Utilisez [**IWbemCallResult :: GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) sur le pointeur retourné pour récupérer les **\_ S non \_ - \_ erreur WBEM**.

3.  Terminez votre appel.

    Pour un appel qui retourne un énumérateur, WMI appelle [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) pour signaler la fin de l’opération. Si vous n’avez pas besoin de la totalité du résultat, Libérez l’énumérateur en appelant la méthode [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . L’appel des résultats de la **mise** en service dans WMI annule la remise de tous les objets restants.

    Pour un appel qui n’utilise pas d’énumérateur, récupérez l’objet [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) via le paramètre *plStatus* de votre méthode.

L’exemple de code C++ dans cette rubrique requiert que les \# instructions include suivantes soient compilées correctement.


```C++
#include <comdef.h>
#include <wbemidl.h>
```



L’exemple de code suivant montre comment effectuer un appel semi-synchrone à [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

 
