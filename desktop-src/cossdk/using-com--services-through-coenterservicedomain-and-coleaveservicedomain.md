---
description: Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain
ms.assetid: 763fb01e-5daf-4e9b-8ef1-9ae79c0a84cc
title: Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0977f92ed377a03487c768e42a5d14fdb710c115f4fa21e4149b125c2806e012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119380789"
---
# <a name="using-com-services-through-coenterservicedomain-and-coleaveservicedomain"></a>Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) et [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain) sont utilisés ensemble pour entourer une zone de code qui s’exécute dans son propre contexte et peut utiliser des services com+ sans nécessiter de composants com+. Les services COM+ utilisés dans ce contexte sont configurés via l’objet [**CServiceConfig**](cserviceconfig.md) qui est transmis à **CoEnterServiceDomain**. Le code entouré par **CoEnterServiceDomain** et **CoLeaveServiceDomain** se comporte comme s’il s’agissait d’une méthode appelée sur un objet créé dans ce contexte.

Une application de script peut utiliser cette paire de fonctions pour fournir une prise en charge au moment de l’exécution des services COM+ sans composants. Par exemple, une application de script peut être développée pour fournir des balises qui permettent aux créateurs de script d’entrer et de laisser un domaine de service au sein du script. Lorsque le moteur de script traite le script et rencontre les balises, il peut appeler [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) avec un objet [**CServiceConfig**](cserviceconfig.md) préconfiguré, exécuter le code nécessaire, puis appeler [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain).

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Non applicable.

## <a name="visual-basic"></a>Visual Basic

Non applicable.

## <a name="cc"></a>C/C++

Le fragment de code suivant illustre l’utilisation des services COM+ entre les appels à [**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain) et [**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain). La gestion des erreurs est omise par souci de concision. Ce fragment de code utilise l’objet [**CServiceConfig**](cserviceconfig.md) qui a été créé et configuré dans [Configuration des services com+ avec CServiceConfig](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
//   IID_IUnknown, (void**)&pUnknownCSC);

// Enter the Service Domain.
HRESULT hr = CoEnterServiceDomain(pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Do the work that uses COM+ services here.
//DoMyWork();

// Leave the Service Domain.
CoLeaveServiceDomain(NULL);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CoEnterServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)
</dt> <dt>

[**CoLeaveServiceDomain**](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)
</dt> <dt>

[Configuration des services COM+ avec CServiceConfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Utilisation des services COM+ via CoCreateActivity](using-com--services-through-cocreateactivity.md)
</dt> </dl>

 

 



