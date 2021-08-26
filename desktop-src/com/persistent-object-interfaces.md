---
title: Interfaces d’objets persistants (COM)
description: Un objet persistant implémente une ou plusieurs interfaces d’objets persistants.
ms.assetid: 8c8e44e4-f564-4af5-9a8a-ac6883862cae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ee1062c80a5c40d139965e0e3bebf96cbda534062322e218e2f5a7da586ff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120409"
---
# <a name="persistent-object-interfaces"></a>Interfaces d’objets persistants

Un objet persistant implémente une ou plusieurs *interfaces d’objets persistants*. Les clients utilisent des interfaces d’objets persistants pour indiquer à ces objets quand et où stocker leur état. Toutes les interfaces d’objets persistants sont dérivées de [**IPersist**](/windows/desktop/api/ObjIdl/nn-objidl-ipersist), donc tout objet qui implémente une interface d’objet persistant implémente également **IPersist**.

Les interfaces d’objets persistants suivantes sont actuellement définies :

-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)
-   [**IPersist**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)
-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage)
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)
-   [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))
-   [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))
-   [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))

Les implémenteurs choisissent les interfaces d’objets persistantes prises en charge par un objet en fonction de la façon dont l’objet doit être utilisé. En ne prenant pas en charge les interfaces d’objets persistantes, le responsable de l’implémentation dit en fait que l’état de cet objet ne peut pas être stocké de manière permanente. En prenant en charge une ou plusieurs interfaces d’objets persistants, l’implémenteur est en fait dit : « l’état de cet objet peut être stocké de manière permanente dans un ou plusieurs supports de magasin de données ».

Par exemple, le tableau suivant répertorie plusieurs types d’objets qui permettent la prise en charge de différentes interfaces d’objets persistants.



| Category                            | Interfaces d’objets persistantes généralement prises en charge                                                                                                                                                         |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Monikers<br/>                 | [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)<br/>                                                                                                                                                      |
| Objets OLE incorporables<br/>   | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |
| contrôles ActiveX ;<br/>         | [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), IPersistMemory, IPersistPropertyBag, [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))<br/> |
| objets de document ActiveX<br/> | [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ **IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile)<br/>                                                                                                              |



 

Les implémenteurs clients peuvent également choisir les interfaces d’objets persistants que le client peut utiliser. Les interfaces qu’un client utilise sont généralement déterminées par l’emplacement où le client peut stocker ses propres données. Un client qui ne peut stocker ses données que dans un fichier plat n’utilisera probablement que [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85))et IPersistPropertyBag. (**IPersistStreamInit** peut remplacer [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) dans la plupart des applications, car il contient cette définition et ajoute une méthode d’initialisation.) Un client qui peut enregistrer ses données dans un fichier de stockage structuré utilisera également [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Initialisation d’objets persistants](initializing-persistent-objects.md)
</dt> </dl>

 

