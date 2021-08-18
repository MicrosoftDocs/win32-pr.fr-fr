---
description: Définit la configuration du flux pour la source du média WTV.
ms.assetid: 2181723A-C6E8-42BD-979C-5C26FE3986C4
title: MFPKEY_SBESourceMode, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c6b4fc0b248000f0540fd47fd7bbf8bba907994d1351144521bf162d330340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973368"
---
# <a name="mfpkey_sbesourcemode-property"></a>MFPKEY \_ propriété SBESourceMode

Définit la configuration du flux pour la source du média WTV.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**INT**

VT \_ int

**intVal**



## <a name="remarks"></a>Remarques

Utilisez cette propriété pour configurer la source du média WTV. Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

la source du média WTV lit Windows fichiers de l’émission TV (. WTV et. ms-drv) enregistrés.

Cette propriété doit avoir l’une des valeurs suivantes.

-   1 : mapper les flux audio disponibles à une sortie unique, en fonction de la valeur système locale. Ce mode est approprié pour la lecture. (valeur par défaut).
-   2. Tous les flux et sous-flux audio (tels que les flux de données et de légende) sont sélectionnés. Ce mode est approprié pour le remuxing ou le transcodage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
