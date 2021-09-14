---
title: Utilisation de l’annotation de serveur
description: Cette rubrique fournit des informations sur l’utilisation de l’annotation de serveur pour spécifier un objet de rappel.
ms.assetid: eeeebddc-2752-4d8f-b4fa-38ce156acc08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb545cd4dd016901d69f67d5ab5cab15dda08875
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221836"
---
# <a name="using-server-annotation"></a>Utilisation de l’annotation de serveur

Cette rubrique fournit des informations sur l’utilisation de l’annotation de serveur pour spécifier un objet de rappel.

**Pour substituer une propriété qui spécifie un objet de rappel**

1.  Obtient un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) vers l’élément accessible qui doit être annoté.
2.  Appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’élément accessible pour recevoir un pointeur d’interface [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) .
3.  Appelez [**IAccIdentity :: GetIdentityString ()**](/windows/desktop/api/Oleacc/nf-oleacc-iaccidentity-getidentitystring) sur le pointeur d’interface [**IAccIdentity**](/windows/desktop/api/oleacc/nn-oleacc-iaccidentity) pour obtenir une chaîne qui identifie de façon unique l’élément accessible qui doit être annoté.
4.  Utilisez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) pour créer l’objet [**IAccPropServices**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropservices) .
5.  Créez un objet COM (Component Object Model) qui implémente [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver).
6.  Appelez [**IAccPropServices :: SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver), en passant la chaîne d’identité, un GUID indiquant la propriété à substituer et un pointeur vers l’objet de rappel [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) .
7.  Libère les pointeurs d’interface et la mémoire libre.

Lorsqu’un client demande la propriété de l’élément accessible, l’objet de rappel sera appelé et renverra la valeur au client.

Comme lorsque vous spécifiez une valeur, les développeurs de serveurs peuvent également utiliser la méthode [**IAccPropServices :: ComposeHwndIdentityString**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-composehwndidentitystring) pour obtenir une chaîne d’identité ; ils peuvent utiliser la méthode [**IAccPropServices :: SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) et spécifier les paramètres *HWND*, *idObject* ou *idChild* au lieu d’une chaîne d’identité.

Lors de l’utilisation de [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver) ou [**SetHwndPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-sethwndpropserver) sur un objet conteneur, les développeurs de serveurs peuvent éventuellement spécifier que les informations de substitution doivent également s’appliquer à tous les éléments enfants de ce conteneur.

Les serveurs peuvent effacer explicitement l’annotation à tout moment à l’aide de [**IAccPropServices :: ClearProps**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-clearprops). Cela n’est généralement pas nécessaire, car le service d’annotation nettoie automatiquement et libère les informations d’annotation lorsque l’élément accessible annoté disparaît.

Vous trouverez ci-dessous une liste des propriétés qui peuvent être annotées à l’aide de cette procédure.

## <a name="properties-supported-when-specifying-a-callback"></a>Propriétés prises en charge lors de la spécification d’un rappel

Lorsque vous spécifiez un rappel, les propriétés suivantes peuvent être annotées. Actuellement, ces propriétés ne peuvent pas être annotées directement en spécifiant une valeur.



| Propriété                      | Type                                                             |
|-------------------------------|------------------------------------------------------------------|
| \_nom du compte propid \_             | VT \_ BSTR                                                         |
| \_Description du compte propid \_      | VT \_ BSTR                                                         |
| \_rôle de compte propid \_             | VT \_                                                           |
| \_État du compte propid \_            | VT \_                                                           |
| \_aide sur le compte propid \_             | VT \_ BSTR                                                         |
| \_KEYBOARDSHORTCUT de compte propid \_ | VT \_ BSTR                                                         |
| ID de l' \_ \_ DefaultAction ACC    | VT \_ BSTR                                                         |
| PROPID \_ compte \_ VALUEMAP         | VT \_ BSTR                                                         |
| \_ROLEMAP de compte propid \_          | VT \_ BSTR                                                         |
| \_STATEMAP de compte propid \_         | VT \_ BSTR                                                         |
| \_focus du compte propid \_            | \_distribution vt<br/> VT \_<br/>                        |
| \_sélection du compte propid \_        | \_distribution vt<br/> VT \_<br/> VT \_ inconnu<br/> |
| PROP \_ . \_ parent du compte           | \_distribution vt                                                     |
| point \_ d' \_ accès au compte propid \_          | \_distribution vt<br/> VT \_<br/>                        |
| décompte de \_ la fenêtre de \_ navigation \_        | \_distribution vt<br/> VT \_<br/>                        |
| décompte du point d’approp \_ \_ \_ gauche        | \_distribution vt<br/> VT \_<br/>                        |
| décompte du point d’approp \_ \_ \_ droit       | \_distribution vt<br/> VT \_<br/>                        |
| PROP \_ . \_ \_        | \_distribution vt<br/> VT \_<br/>                        |
| ID d’en-dessous du compte d’prop \_ \_ \_        | \_distribution vt<br/> VT \_<br/>                        |
| ID de la la firstChild du point PROPID \_ \_ \_  | \_distribution vt<br/> VT \_<br/>                        |
| ID de l' \_ \_ \_ LastChild du point propid   | \_distribution vt<br/> VT \_<br/>                        |



 

 

