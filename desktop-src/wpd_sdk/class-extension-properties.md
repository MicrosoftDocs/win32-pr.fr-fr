---
description: Windows Les appareils mobiles prennent en charge les propriétés d’extension de classe suivantes.
ms.assetid: 9b8983ba-5824-495d-868f-fd22b98e1954
title: Propriétés de l’extension de classe (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Class
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c7215a383aec582f576cb64a6781068034bb7fa8df03b5a404368482f1c1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843403"
---
# <a name="class-extension-properties"></a>Propriétés d’extension de classe

Windows Les appareils mobiles prennent en charge les propriétés d’extension de classe suivantes.



| Propriété                                                                      | VarType         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_options d’extension de classe wpd \_ \_ \_ types de contenu pris en charge \_ \_**                 | **VT \_ inconnu** | Valeur qui spécifie la liste (sur-ensemble) des types de contenu pris en charge par le pilote (semblable à l’appel des fonctionnalités de commande WPD, \_ \_ \_ obtenir \_ les types de contenu pris en charge \_ sur la \_ **\_ catégorie fonctionnelle wpd \_ \_ All**).                                                                                                                                                                                                                                                                                                                                             |
| **les \_ options d’extension de classe wpd n' \_ inscrivent pas l' \_ \_ \_ \_ interface d' \_ appareil wpd \_**    | **VT \_ bool**    | Valeur qui spécifie si l’appelant souhaite que la bibliothèque d’extensions de classe WPD enregistre l’interface de classe de périphérique WPD. Si cette valeur est true, l’appelant est responsable de l’inscription.<br/> Si cette valeur est false, cela signifie que l’appelant s’attend à ce que la bibliothèque d’extensions de classe effectue l’inscription.<br/>La plupart des pilotes doivent autoriser la bibliothèque d’extensions de classe à effectuer l’inscription, sauf si l’inscription de l’interface de classe de périphérique WPD par la bibliothèque d’extensions de classe peut entraîner des effets négatifs. |
| **OPTIONS d’extension de classe WPD inscrire l’interface de l' \_ \_ \_ \_ \_ \_ appareil privé wpd \_ \_** | **VT \_ bool**    | Indique que l’appelant souhaite que la bibliothèque d’extensions de classe WPD enregistre l’interface de classe d’appareil WPD privée. Cela n’est pas recommandé pour la plupart des pilotes. Elle doit être utilisée uniquement dans les cas où l’inscription de l’interface de classe d’appareil WPD par la bibliothèque d’extensions de classe entraîne des effets négatifs. Cette option est généralement utilisée conjointement avec les **options d’extension de classe wpd ne pas \_ inscrire l' \_ \_ \_ \_ \_ \_ \_ interface d’appareil wpd** définie à **true**                                                                                          |
| **OPTIONS d’extension de classe WPD valeurs d’identification de l' \_ \_ \_ \_ appareil \_ \_**            | **VT \_ inconnu** | Il s’agit d’un [IPortableDeviceValues](iportabledevicevalues.md) qui contient les valeurs d’identification de l’appareil (modèle d’appareil **wpd \_ \_**, **\_ \_ modèle d’appareil wpd**, **\_ \_ \_ version du microprogramme d’appareil wpd** et **\_ \_ \_ \_ ID unique fonctionnel de l’appareil wpd**). Inclure avec d’autres options d’extension de classe lors de l’initialisation                                                                                                                                                                                                                               |
| **OPTIONS d’extension de classe WPD- \_ \_ \_ \_ \_ bande passante de transport**                      | **VT \_ UI4**     | Indique la bande passante maximale théorique du transport en kilobits par seconde.                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **OPTIONS d’extension de classe WPD valeurs d’identification de l' \_ \_ \_ \_ appareil \_ \_**            | **VT \_ inconnu** | Il s’agit d’un [IPortableDeviceValues](iportabledevicevalues.md) qui contient les valeurs d’identification de l’appareil (modèle d’appareil **wpd \_ \_**, **\_ \_ modèle d’appareil wpd**, **\_ \_ \_ version du microprogramme d’appareil wpd** et **\_ \_ \_ \_ ID unique fonctionnel de l’appareil wpd**). Incluez ceci avec d’autres options d’extension de classe lors de l’initialisation.                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




