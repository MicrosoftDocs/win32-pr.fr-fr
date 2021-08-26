---
title: Utiliser OBJID \_ NATIVEOM pour exposer une interface native pour une fenêtre
description: Cette technique permet aux clients d’obtenir un objet personnalisé pour une fenêtre. Les serveurs peuvent l’utiliser pour exposer un pointeur vers un objet de document personnalisé pour une fenêtre.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed99db4641235ceee57688865710c19a41f0a517d70d4601d138150cb88dd470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098089"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a>Utiliser OBJID \_ NATIVEOM pour exposer une interface native pour une fenêtre

Cette technique permet aux clients d’obtenir un objet personnalisé pour une fenêtre. Les serveurs peuvent l’utiliser pour exposer un pointeur vers un objet de document personnalisé pour une fenêtre.

**Pour exposer une interface de modèle objet natif pour une fenêtre (serveurs)**

1.  Gérez le message [**WM \_ GETOBJECT**](wm-getobject.md) dans la procédure de fenêtre. Lorsque la valeur *lParam* est [**objID \_ NATIVEOM**](object-identifiers.md), retourne un pointeur d’interface vers l’objet personnalisé à l’aide de [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).
2.  Libérez votre pointeur d’interface après l’appel de [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), le cas échéant. Pour plus d’informations, consultez **LresultFromObject**.

Les clients peuvent obtenir un pointeur vers cet objet personnalisé.

**Pour obtenir un pointeur pour un objet personnalisé pour une fenêtre (clients)**

-   Appelez [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) et transmettez [**objID \_ NATIVEOM**](object-identifiers.md) en tant que second paramètre.

Notez les points suivants pour cette technique :

-   Cette technique est similaire au retour d’un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , à l’exception de l’ID d’objet utilisé et du fait que [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) retourne un objet personnalisé au lieu de **IAccessible**.
-   Les développeurs de serveurs peuvent avoir besoin de publier des informations qui permettent aux clients d’identifier le **HWND** de manière unique afin qu’il puisse le trouver avant d’appeler [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) sur son handle de fenêtre.
-   N’implémentez pas l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sur l’objet personnalisé qui est retourné. Dans ce cas, OLEACC le traite comme un **IAccessible** standard et peut empêcher l’utilisation des interfaces personnalisées.
-   Pour pouvoir être utilisé dans plusieurs processus, les interfaces sur l’objet retourné peuvent avoir besoin d’être inscrites auprès du modèle COM (Component Object Model).

cette technique est prise en charge par plusieurs composants de Microsoft Office. Pour plus d’informations, consultez [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

 

 




