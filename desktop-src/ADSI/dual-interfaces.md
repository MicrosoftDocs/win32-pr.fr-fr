---
title: Interfaces doubles (ADSI)
description: Utilisez les interfaces COM pour accéder aux propriétés et aux méthodes sur les objets ADSI du fournisseur.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d1cf89ef07e573be8f59805034ff8c567e75fd
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884058"
---
# <a name="dual-interfaces-adsi"></a>Interfaces doubles (ADSI)

Utilisez les interfaces COM pour accéder aux propriétés et aux méthodes sur les objets ADSI du fournisseur. Une propriété en lecture seule est mappée à une entrée d’interface de la forme **obtenir \_ &lt; &gt; PropertyName**. Une propriété en lecture/écriture mappe à deux entrées d’interface de la forme **obtenir \_ &lt; &gt; PropertyName** et **put \_ &lt; PropertyName &gt;**.

Toutes les méthodes sur une interface COM doivent :

-   Retourne une valeur HRESULT pour indiquer la réussite ou l’échec. Le type **HRESULT** est abordé dans la spécification com.
-   Lors des appels à **QueryInterface**, retournez **E \_ nointerface** pour les interfaces non implémentées.
-   Retournez **E \_ NOTIMPL** pour les méthodes non implémentées sur les interfaces implémentées autrement.
-   Renvoie **la \_ propriété E ADS \_ \_ non \_ prise en charge** pour les propriétés d’interface qui ne sont pas prises en charge.

Pour conserver la compatibilité avec les contrôleurs Automation, tous les paramètres et types de retour doivent se trouver dans le sous-ensemble défini par le type de données Automation VARIANT. Pour plus d’informations, consultez **Variant** et **VARIANTARG** dans le kit de développement logiciel (SDK) de la plateforme.

Un objet Active Directory fournisseur peut exposer des interfaces qui utilisent des types de données autres que ceux du sous-ensemble **Variant** . toutefois, les contrôleurs Automation tels que les Visual Basic ne sont pas en mesure d’appeler ces interfaces. La plupart des interfaces de fournisseur ADSI sont dérivées de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) et peuvent être utilisées comme pointeurs d’interface **IDispatch** . Toutefois, les interfaces ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)et [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ne sont pas dérivées de **IDispatch**.

 

 
