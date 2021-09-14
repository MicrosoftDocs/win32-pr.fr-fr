---
description: Un fournisseur d’événements peut consacrer beaucoup de temps à la création d’événements.
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: Optimisation d’un fournisseur d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70eaabfbbd462b831059b10590d7959bdef05cbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008241"
---
# <a name="optimizing-an-event-provider"></a>Optimisation d’un fournisseur d’événements

Un fournisseur d’événements peut consacrer beaucoup de temps à la création d’événements. Si aucune application cliente n’utilise les événements créés, le fournisseur gaspille les ressources système. En outre, WMI passe une quantité considérable de ressources à analyser et à envoyer des requêtes complexes au fournisseur approprié. Pour éviter le gaspillage des ressources système et améliorer les performances de votre fournisseur d’événements, vous pouvez implémenter l’interface [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) . **IWbemEventProviderQuerySink** surveille les requêtes enregistrées par les applications clientes auprès de WMI à l’aide des méthodes [**newquery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) et [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) . En surveillant les requêtes des clients inscrits, votre fournisseur peut déterminer si des messages doivent être envoyés à WMI.

WMI appelle [**newquery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) sur un fournisseur d’événements lorsqu’un consommateur client inscrit une requête de filtre d’événement qui contient des références aux événements pris en charge par ce fournisseur d’événements. Ainsi, le fournisseur d’événements responsable des événements de modification d’instance pour la classe **EmailClass** peut être configuré pour générer des notifications uniquement pour l' **expéditeur**. Lorsque le fournisseur reçoit une requête demandant la notification des modifications apportées à la propriété **Subject** , le fournisseur peut commencer à générer ces notifications. Dans ce scénario, WMI n’est pas obligé d’ignorer les notifications qui modifient uniquement les **destinataires** du rapport.

De même, WMI appelle [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) sur un fournisseur d’événements lorsqu’un consommateur client annule l’inscription d’une requête de filtre d’événement qui contient des références aux événements pris en charge par le fournisseur d’événements. L’objectif de **CancelQuery** est que le fournisseur d’événements met à jour la liste des événements à envoyer.

> [!Note]  
> Si votre fournisseur prend en charge à la fois [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) et [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink), assurez-vous que votre implémentation de la méthode **IUnknown :: QueryInterface** retourne des pointeurs vers les deux interfaces.

 

 

 



