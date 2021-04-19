---
description: La fonction CoCreateActivity est utilisée pour soumettre le travail en traitement par lots au système COM+. Il permet aux applications basées sur des scripts de prendre en charge une configuration de service COM+ à l’ensemble de l’application.
ms.assetid: af734507-516c-43f1-9c5e-c77cde1b8008
title: Utilisation des services COM+ via CoCreateActivity
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b3296756b91d0f8ea29b1d67c11c78c431cfcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515376"
---
# <a name="using-com-services-through-cocreateactivity"></a>Utilisation des services COM+ via CoCreateActivity

La fonction [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) est utilisée pour soumettre le travail en traitement par lots au système com+. Il permet aux applications basées sur des scripts de prendre en charge une configuration de service COM+ à l’ensemble de l’application.

Les services COM+ souhaités sont configurés via un objet [**CServiceConfig**](cserviceconfig.md) qui est transmis à la fonction. La fonction crée un objet d’activité et retourne l’interface [**IServiceActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceactivity) de cet objet. Le travail en traitement par lots peut être envoyé de manière synchrone ou asynchrone, à l’aide des méthodes [**SynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-synchronouscall) ou [**AsynchronousCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iserviceactivity-asynchronouscall) de **IServiceActivity**, respectivement. Un pointeur vers une interface [**IServiceCall**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecall) est passé à chacune de ces méthodes, et le travail en traitement par lots est implémenté par le développeur dans la méthode [**OnCall**](/windows/desktop/api/ComSvcs/nf-comsvcs-iservicecall-oncall) de l’interface **IServiceCall** .

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Non applicable.

## <a name="visual-basic"></a>Visual Basic

Non applicable.

## <a name="cc"></a>C/C++

Le fragment de code suivant illustre l’utilisation des services COM+ par le biais de [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity). La gestion des erreurs est omise par souci de concision. Ce fragment de code utilise l’objet [**CServiceConfig**](cserviceconfig.md) qui a été créé et configuré dans [Configuration des services com+ avec CServiceConfig](configuring-com--services-with-cserviceconfig.md).


```C++
// A CServiceConfig object was created as follows:
// hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER,
//   IID_IUnknown, (void**)&pUnknownCSC);

// Create the activity for our services.
HRESULT hr = CoCreateActivity(pUnknownCSC, IID_IServiceActivity, (void**)&pActivity);
if (FAILED(hr)) throw(hr);

// Do the batch work synchronously.
// The batch work is implemented in pServiceCall->OnCall().
hr = pActivity->SynchronousCall(pServiceCall);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)
</dt> <dt>

[Configuration des services COM+ avec CServiceConfig](configuring-com--services-with-cserviceconfig.md)
</dt> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

 



