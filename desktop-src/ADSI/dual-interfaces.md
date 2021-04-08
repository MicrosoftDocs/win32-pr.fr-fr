---
title: Interfaces doubles (ADSI)
description: Utilisez les interfaces COM pour accéder aux propriétés et aux méthodes sur les objets ADSI du fournisseur.
ms.assetid: 6f3fd725-d660-4cc3-8de2-8ed7800b1141
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c858275098dd82362d229bc9e1cc35b544c55
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730188"
---
# <a name="dual-interfaces-adsi"></a>Interfaces doubles (ADSI)

Utilisez les interfaces COM pour accéder aux propriétés et aux méthodes sur les objets ADSI du fournisseur. Une propriété en lecture seule est mappée à une entrée d’interface de la forme **obtenir \_ <PropertyName>**. Une propriété en lecture/écriture mappe à deux entrées d’interface de la forme **obtenir \_ <PropertyName>** et **Placer \_ <PropertyName>**.

Toutes les méthodes sur une interface COM doivent :

-   Retourne une valeur HRESULT pour indiquer la réussite ou l’échec. Le type **HRESULT** est abordé dans la spécification com.
-   Lors des appels à **QueryInterface**, retournez **E \_ nointerface** pour les interfaces non implémentées.
-   Retournez **E \_ NOTIMPL** pour les méthodes non implémentées sur les interfaces implémentées autrement.
-   Renvoie **la \_ propriété E ADS \_ \_ non \_ prise en charge** pour les propriétés d’interface qui ne sont pas prises en charge.

Pour conserver la compatibilité avec les contrôleurs Automation, tous les paramètres et types de retour doivent se trouver dans le sous-ensemble défini par le type de données Automation VARIANT. Pour plus d’informations, consultez **Variant** et **VARIANTARG** dans le kit de développement logiciel (SDK) de la plateforme.

Un objet Active Directory fournisseur peut exposer des interfaces qui utilisent des types de données autres que ceux du sous-ensemble **Variant** . Toutefois, les contrôleurs Automation tels que les Visual Basic ne sont pas en mesure d’appeler ces interfaces. La plupart des interfaces de fournisseur ADSI sont dérivées de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) et peuvent être utilisées comme pointeurs d’interface **IDispatch** . Toutefois, les interfaces ADSI [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)et [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) ne sont pas dérivées de **IDispatch**.

 

 