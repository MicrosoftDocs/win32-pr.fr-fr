---
description: Configuration des services COM+ avec CServiceConfig
ms.assetid: c44743a8-8b91-4e2a-9ba4-4cb6ae787999
title: Configuration des services COM+ avec CServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8bbc6c3131347f450340863db70fd9b3999730
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291823"
---
# <a name="configuring-com-services-with-cserviceconfig"></a>Configuration des services COM+ avec CServiceConfig

La classe [**CServiceConfig**](cserviceconfig.md) est utilisée pour configurer les services com+ qui peuvent être utilisés sans composants. Il agrège le marshaleur libre de threads, afin qu’il puisse être utilisé dans différents cloisonnements. Pour configurer un service individuel, vous devez appeler [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour l’interface associée au service, puis appeler des méthodes sur cette interface pour établir la configuration appropriée. Le tableau suivant décrit les interfaces qui sont implémentées par le biais de la classe **CServiceConfig** .



| Interface                                                                         | Description                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IServiceInheritanceConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceinheritanceconfig)<br/>         | Interface par défaut de la classe. Elle est utilisée pour initialiser rapidement un grand nombre des services COM+.<br/>                                                                                              |
| [**IServiceComTIIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicecomtiintrinsicsconfig)<br/> | Utilisé pour configurer les informations intrinsèques de l’COM Transaction Integrator (COMTI). COMTI permet aux développeurs d’intégrer des programmes de transaction basés sur des macroordinateurs à des applications basées sur des composants.<br/> |
| [**IServiceIISIntrinsicsConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iserviceiisintrinsicsconfig)<br/>     | utilisé pour configurer les informations intrinsèques du Internet Information Services (IIS).<br/>                                                                                                             |
| [**IServicePartitionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicepartitionconfig)<br/>             | Utilisé pour configurer le mode d’utilisation des partitions COM+ avec les services.<br/>                                                                                                                             |
| [**IServiceSxSConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesxsconfig)<br/>                         | Utilisé pour configurer des assemblys côte à côte.<br/>                                                                                                                                                    |
| [**IServiceSynchronizationConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicesynchronizationconfig)<br/> | Utilisé pour configurer les services de synchronisation COM+.<br/>                                                                                                                                              |
| [**IServiceThreadPoolConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicethreadpoolconfig)<br/>           | Utilisé pour configurer le pool de threads pour le service COM+. Le pool de threads ne peut être configuré que lors de l’utilisation de la fonction [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) .<br/>                          |
| [**IServiceTrackerConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetrackerconfig)<br/>                 | Utilisé pour configurer la propriété tracker. Tracker est un mécanisme de création de rapports utilisé par le code de surveillance pour surveiller le code en cours d’exécution.<br/>                                                         |
| [**IServiceTransactionConfig**](/windows/desktop/api/ComSvcs/nn-comsvcs-iservicetransactionconfig)<br/>         | Utilisé pour configurer le service de transactions COM+.<br/>                                                                                                                                               |



 

## <a name="component-services-administrative-tool"></a>Outil d’administration Services de composants

Non applicable.

## <a name="visual-basic"></a>Visual Basic

Non applicable.

## <a name="cc"></a>C/C++

Le fragment de code suivant illustre la création et la configuration d’un objet [**CServiceConfig**](cserviceconfig.md) pour utiliser des transactions com+.


```C++
// Create a CServiceConfig object.
HRESULT hr = CoCreateInstance(CLSID_CServiceConfig, NULL, CLSCTX_INPROC_SERVER, 
  IID_IUnknown, (void**)&pUnknownCSC);
if (FAILED(hr)) throw(hr);

// Query for the IServiceInheritanceConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceInheritanceConfig, 
  (void**)&pInheritanceConfig);
if (FAILED(hr)) throw(hr);

// Inherit the current context before using transactions.
hr = pInheritanceConfig->ContainingContextTreatment(CSC_Inherit);
if (FAILED(hr)) throw(hr);

// Query for the IServiceTransactionConfig interface.
hr = pUnknownCSC->QueryInterface(IID_IServiceTransactionConfig, 
  (void**)&pTransactionConfig);
if (FAILED(hr)) throw(hr);

// Configure transactions to always create a new one.
hr = pTransactionConfig->ConfigureTransaction(CSC_NewTransaction);
if (FAILED(hr)) throw(hr);

// Set the isolation level of the transactions to ReadCommitted.
hr = pTransactionConfig->IsolationLevel( 
  COMAdminTxIsolationLevelReadCommitted);
if (FAILED(hr)) throw(hr);

// Set the transaction time-out to 1 minute.
hr = pTransactionConfig->TransactionTimeout(60);
if (FAILED(hr)) throw(hr);

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CServiceConfig**](cserviceconfig.md)
</dt> <dt>

[Utilisation des services COM+ via CoCreateActivity](using-com--services-through-cocreateactivity.md)
</dt> <dt>

[Utilisation des services COM+ via CoEnterServiceDomain et CoLeaveServiceDomain](using-com--services-through-coenterservicedomain-and-coleaveservicedomain.md)
</dt> </dl>

 

