---
description: Un fournisseur d’instances fournit des instances d’une ou de plusieurs classes données.
ms.assetid: d53c3399-cba8-4b5d-8da0-b5a23f94c0ae
ms.tgt_platform: multiple
title: Écriture d’un fournisseur d’instances
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bddfaa867624bd84cc975d32a8e7b747064d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536696"
---
# <a name="writing-an-instance-provider"></a>Écriture d’un fournisseur d’instances

Un fournisseur d’instances fournit des instances d’une ou de plusieurs classes données. Par exemple, un fournisseur d’instances peut fournir des informations sur un processeur ou un autre type de matériel. Étant donné que les objets gérés par un fournisseur d’instances ont tendance à changer régulièrement, tous les fournisseurs d’instances sont considérés comme des fournisseurs d’extraction ; autrement dit, un fournisseur qui récupère dynamiquement les informations relatives à un objet managé chaque fois que WMI effectue une demande d’informations. Le nom provient de l’idée que WMI « extrait » les informations du fournisseur pour le compte de la demande d’un client. À l’aide de la technologie pull, un fournisseur d’instances peut prendre en charge la récupération, l’énumération, la modification, la suppression et le traitement des requêtes d’une instance spécifique.

Les fournisseurs de haute performance peuvent augmenter l’efficacité d’un fournisseur d’instances ou accéder par programmation aux données qui apparaissent dans le moniteur système. Pour plus d’informations, consultez [création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md).

La procédure suivante décrit comment écrire un fournisseur d’instances.

**Pour écrire un fournisseur d’instances**

1.  [Inscrivez votre fournisseur auprès de WMI](registering-an-instance-provider.md).

    Les fournisseurs d’instances s’inscrivent auprès de WMI en créant une instance [**\_ \_ Win32Provider**](--win32provider.md) et une classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) .

2.  [Initialisez votre fournisseur](initializing-a-provider.md).

    WMI utilise [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) pour charger et initialiser un fournisseur. Il s’agit d’une tâche commune à tous les fournisseurs.

    > [!Note]  
    > Les fournisseurs d’instances sont fortement encouragés à utiliser le modèle de multithreading « both ».

     

3.  [Implémentez l’interface IWbemServices pour votre fournisseur](implementing-the-primary-interface-for-an-instance-provider.md).

    L’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) est l’interface principale d’un fournisseur d’instances.

4.  Ajoutez tout code supplémentaire nécessaire pour votre fournisseur.

    Lorsque vous concevez votre fournisseur, vous devrez probablement appeler des interfaces WMI. Pour plus d’informations, consultez [effectuer des appels à WMI](making-calls-to-wmi.md).

    Lorsque vous récupérez des informations pour un client, vous devrez peut-être accéder aux niveaux de sécurité de ce client. Pour plus d’informations, consultez [emprunt d’identité d’un client](impersonating-a-client.md).

5.  Si nécessaire, [implémentez l’interface hautes performances](improving-the-efficiency-of-an-instance-provider.md).

    L’interface hautes performances augmente la vitesse à laquelle le fournisseur peut réagir aux demandes de WMI.

6.  Si nécessaire, [implémentez la prise en charge des mises à jour d’instance partielle](supporting-partial-instance-operations.md).

    Comme son nom l’indique, une mise à jour de l’instance partielle est une technique qui permet de mettre à jour uniquement une partie d’une instance. Pour plus d’informations sur l’appel d’une instance partielle à partir d’un client, consultez [mise à jour d’une partie d’une instance](updating-part-of-an-instance.md) et [extraction d’une partie d’une instance WMI](retrieving-part-of-an-instance.md).

7.  Remplacez le fournisseur préexistant par votre nouveau code.

    Vous n’avez pas besoin d’effectuer cette étape si vous n’avez pas de fournisseur préexistant à copier. Pour plus d’informations, consultez [mise à jour d’un fournisseur](updating-a-provider.md).

 

 



