---
description: L’interface IWbemObjectSink crée une interface de récepteur qui peut recevoir tous les types de notifications dans le modèle de programmation WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Interface IWbemObjectSink (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6bfce21edca92c95276f382d16007f8b319b9f3b80fc5c3c721f7232ea0b4618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996539"
---
# <a name="iwbemobjectsink-interface"></a>Interface IWbemObjectSink

L’interface **IWbemObjectSink** crée une interface de récepteur qui peut recevoir tous les types de notifications dans le modèle de programmation WMI. Les clients doivent implémenter cette interface pour recevoir les résultats des [méthodes asynchrones](making-an-asynchronous-call-with-c--.md) de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)et des types spécifiques de notifications d’événements. Les fournisseurs utilisent, mais n’implémentent pas cette interface pour fournir des événements et des objets à WMI.

En règle générale, les fournisseurs appellent une implémentation qui leur est fournie par WMI. Dans ce cas, Call [**indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) pour fournir des objets au service WMI. Après cela, appelez [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) pour indiquer la fin de la séquence de notification. Vous pouvez également appeler **SetStatus** pour indiquer des erreurs lorsque le récepteur n’a aucun objet.

Lors de la programmation de clients asynchrones de WMI, l’utilisateur fournit l’implémentation. WMI appelle les méthodes pour remettre des objets et définir l’état du résultat.

> [!Note]  
> Si une application cliente passe la même interface de récepteur dans deux appels asynchrones différents qui se chevauchent, WMI ne garantit pas l’ordre du rappel. Les applications clientes qui effectuent des appels asynchrones qui se chevauchent doivent passer différents objets récepteur ou sérialiser leurs appels.

 

> [!Note]  
> Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser la fonction semi-synchrone au lieu de la communication asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

 

## <a name="members"></a>Membres

L’interface **IWbemObjectSink** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWbemObjectSink** possède ces méthodes.



| Méthode                                         | Description                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Indiquer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | Reçoit des objets de notification.<br/>                                                                               |
| [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | Appelée par les sources pour indiquer la fin d’une séquence de notification, ou pour envoyer d’autres codes d’État au récepteur.<br/> |



 

## <a name="remarks"></a>Remarques

Lors de l’implémentation d’un récepteur d’abonnement aux événements (**IWbemObjectSink** ou [**IWbemEventSink**](iwbemeventsink.md)), n’appelez pas WMI à partir des méthodes d' [**indication**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) ou [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) sur l’objet récepteur. Par exemple, l’appel de [**IWbemServices :: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) pour annuler le récepteur à partir d’une implémentation de [**indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) qu’il peut interférer avec l’État WMI. Pour annuler un abonnement à un événement, définissez un indicateur et appelez **IWbemServices :: CancelAsyncCall** à partir d’un autre thread ou objet. Pour les implémentations qui ne sont pas liées à un récepteur d’événements, telles que les récupérations d’objets, d’enum et de requêtes, vous pouvez rappeler dans WMI.

Les implémentations de récepteur doivent traiter la notification d’événement dans un délai de 100 ms car le thread WMI qui remet la notification d’événement ne peut pas effectuer d’autres tâches tant que le traitement de l’objet récepteur n’est pas terminé. Si la notification nécessite une grande quantité de traitement, le récepteur peut utiliser une file d’attente interne pour qu’un autre thread gère le traitement.

## <a name="examples"></a>Exemples

L’exemple de code suivant est une implémentation simple d’un récepteur d’objets. Cet exemple peut être utilisé avec [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) ou [**IWbemServices :: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) pour recevoir les instances retournées :


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                           |
| En-tête<br/>                   | <dl> <dt>Wbemcli. h (inclure Wbemidl. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Wbemuuid. lib</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl>                  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API COM pour WMI](com-api-for-wmi.md)
</dt> <dt>

[Exécution d’un appel asynchrone avec C++](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[Définition de la sécurité sur un appel asynchrone](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[Réception d’événements pendant la durée de votre application](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




