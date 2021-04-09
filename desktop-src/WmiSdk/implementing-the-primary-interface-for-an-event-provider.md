---
description: Un fournisseur d’événements doit implémenter l’interface IWbemEventProvider pour générer des notifications d’événements.
ms.assetid: ae33c9f5-61f7-4488-a281-01d7f9c62c46
ms.tgt_platform: multiple
title: Implémentation de l’interface principale pour un fournisseur d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5621a2c6d0901a7925828149dd5c1480c2b11456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952467"
---
# <a name="implementing-the-primary-interface-for-an-event-provider"></a>Implémentation de l’interface principale pour un fournisseur d’événements

Un fournisseur d’événements doit implémenter l’interface [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) pour générer des notifications d’événements. WMI appelle la méthode [**IWbemEventProvider ::P rovideevents**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents) du fournisseur et transmet un pointeur vers l’objet récepteur, qui est une implémentation de l’interface [**IWbemObjectSink**](iwbemobjectsink.md) . Lorsque le fournisseur d’événements est prêt à générer une notification, le fournisseur appelle la méthode [**IWbemObjectSink :: indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

Un fournisseur d’événements doit placer les notifications générées par le biais de [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) dans les objets d’événement. Vous devez implémenter des objets d’événement en tant qu’entrées dans un tableau d’interfaces [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) représenté par le paramètre *ppObjArray* de la méthode d' [**indication**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) . Étant donné que les **IWbemClassObjects** sont des objets com, le fournisseur doit incrémenter le décompte de références pour le récepteur en appelant la méthode [**IWbemObjectSink :: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) . Les fournisseurs d’événements qui doivent fournir de nombreuses notifications (par exemple, les événements 400) doivent créer un objet d’événement unique pour chaque notification en générant une nouvelle instance ou en clonant une instance existante. WMI ne contient jamais un objet d’événement au-delà de la fin de l’appel d' **indication** , et n’a pas d’exigences spéciales pour le **AddRef** au-dessus et au-delà de la norme com.

Tenez compte des recommandations suivantes lors de l’implémentation d’un fournisseur d’événements :

-   N’apportez pas de modifications de classe lors de la maintenance d’un appel client.
-   N’émettez pas d’appels liés aux événements, tels qu’un appel qui modifie un filtre d’événement.
-   Traitez toutes les demandes que le service de gestion Windows émet, telles que [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery), avant de réexécuter un événement.

    Si vous ne traitez pas la requête, le déclenchement de l’événement peut empêcher l’événement d’être accepté.

-   N’appelez jamais [**IWbemObjectSink :: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) à partir d’un fournisseur.

 

 
