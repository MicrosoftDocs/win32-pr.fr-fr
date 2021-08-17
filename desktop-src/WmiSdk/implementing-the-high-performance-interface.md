---
description: Étant donné que WMI charge un fournisseur de haute performance dans le processus vers WMI ou une application cliente, vous devez concevoir votre fournisseur hautes performances en tant que serveur in-process.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implémentation de l’interface High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecec9a7b5e5399765adaa7a0e195825493d930ece46c30af3e788795fe08ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118108620"
---
# <a name="implementing-the-high-performance-interface"></a>Implémentation de l’interface High-Performance

Étant donné que WMI charge un fournisseur de haute performance dans le processus vers WMI ou une application cliente, vous devez concevoir votre fournisseur hautes performances en tant que serveur in-process. En outre, vous devez implémenter les méthodes de fournisseur de haute performance dans les interfaces [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) et [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) .

Vous devez implémenter un fournisseur de haute performance en tant que serveur in-process. L’une des fonctionnalités que vous devez prendre en compte lors de l’implémentation de la sécurité d’un serveur in-process est la manière dont le fournisseur identifie son propre emplacement. Lorsqu’il est chargé dans le processus de WMI, WMI instancie le fournisseur à l’aide d’un CLSID. Lorsqu’il est chargé en cours de traitement dans une application cliente, l’application cliente instancie le fournisseur avec la propriété **ClientLoadableCLSID** . En attribuant des valeurs différentes à un CLSID et à **ClientLoadableCLSID**, vous autorisez le fournisseur à déterminer s’il est chargé dans le processus vers WMI ou vers une application cliente. Si elle se trouve dans un processus WMI, le fournisseur doit effectuer l’emprunt d’identité du client nécessaire à l’aide de **ClientLoadableCLSID**. Si elle se trouve dans un processus client, le fournisseur hérite du jeton d’accès du thread sur lequel elle est appelée. Pour plus d’informations sur l’implémentation d’un serveur in-process, consultez la [section com](https://msdn.microsoft.com/library/aa139695.aspx) de MSDN.

En tant que serveur in-process, un fournisseur de haute performance utilise un objet actualisateur pour conserver les données à jour pour le client distant. Le tableau suivant répertorie les méthodes que vous devez implémenter pour un fournisseur à hautes performances.



| Méthode                                                                                              | Fonctionnalité                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IWbemHiPerfProvider :: QueryInstances**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | Requêtes                                           |
| [**IWbemHiPerfProvider :: GetObjects**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | Récupération d’objets                                  |
| [**IWbemHiPerfProvider :: CreateRefresher**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | Crée un actualisateur                               |
| [**IWbemHiPerfProvider :: CreateRefreshableObject**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | Crée un objet d’instance actualisable             |
| [**IWbemHiPerfProvider :: CreateRefreshableEnum**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | Crée un énumérateur actualisable                  |
| [**IWbemHiPerfProvider :: StopRefreshing**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | Arrête l’actualisation d’un objet énumérateur ou d’instance |
| [**IWbemRefresher :: Refresh**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | Crée un actualisateur                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



