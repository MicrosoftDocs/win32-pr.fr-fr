---
description: le fournisseur wdm (Windows Driver Model) accorde l’accès aux classes, aux instances, aux méthodes et aux événements des pilotes matériels conformes au modèle WDM.
ms.assetid: 2f9749ff-b318-4228-80fd-e3846dde21d2
title: Fournisseur WDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ba187680ec371f331aa6394c5a2408c23080259e6b275e74cee496dd5125cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794619"
---
# <a name="wdm-provider"></a>Fournisseur WDM

le fournisseur wdm (Windows Driver Model) accorde l’accès aux classes, aux instances, aux méthodes et aux événements des pilotes matériels conformes au modèle WDM. Les classes pour les pilotes de matériel résident dans l' \\ espace de noms WMI racine.

Les classes WDM sont définies principalement dans WMI. mof.

WDM est une interface de système d’exploitation par le biais de laquelle les composants matériels fournissent des informations et des notifications d’événements. Le fournisseur WDM est un fournisseur de classes, d’instances, d’événements et de méthodes qui permet aux applications de gestion d’accéder aux données et aux événements à partir des pilotes de périphérique compatibles WMI-pour-WDM. Les classes créées par le fournisseur WDM pour représenter des données de pilote de périphérique résident uniquement dans l' \\ espace de noms WMI racine. Cet espace de noms doit déjà exister avant que le fournisseur WDM ne traite les pilotes WDM installés.

Le fournisseur WDM enregistre des informations sur les opérations WDM dans le fichier WmiProv. log. Pour plus d’informations, consultez [fichiers journaux WMI](/windows/desktop/WmiSdk/wmi-log-files).

En tant que classe, instance, méthode et fournisseur d’événements, le fournisseur WDM implémente l’interface [**IWbemProviderInit**](/windows/desktop/api/wbemprov/nn-wbemprov-iwbemproviderinit) standard, ainsi que les méthodes [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) suivantes :

-   [**CreateClassEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync)
-   [**CreateInstanceEnumAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**GetObjectAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**ExecMethodAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecNotificationQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execnotificationqueryasync)
-   [**ExecQueryAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**PutInstanceAsync**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

Le fournisseur WDM prend en charge l’événement extrinsèque [**WmiEvent**](/windows/desktop/WmiCoreProv/wmievent) , qui NOTIFIe WMI en ce qui concerne les événements des pilotes basés sur WDM. Vous pouvez inscrire vos consommateurs d’événements pour les événements **WmiEvent** comme vous le feriez pour n’importe quel autre événement. Pour plus d’informations, consultez [réception d’un événement WMI](/windows/desktop/WmiSdk/receiving-a-wmi-event). Aucun événement de création de classe n’est déclenché lors du démarrage d’un pilote.

Le fournisseur WDM prend en charge la classe suivante :

-   [**WMIBinaryMofResource**](wmibinarymofresource.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fournisseurs WMI](/windows/desktop/WmiSdk/wmi-providers)
</dt> <dt>

[Accès aux données à partir des pilotes de périphérique](/windows/desktop/WmiSdk/accessing-data-from-device-drivers)
</dt> </dl>

 

 
