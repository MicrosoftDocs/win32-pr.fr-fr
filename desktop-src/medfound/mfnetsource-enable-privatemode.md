---
description: Active le mode de téléchargement privé dans la source réseau.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: MFNETSOURCE_ENABLE_PRIVATEMODE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e2ff972aa42753bb92be33fd6bf893d0578f28bf0ad29889a1b5986ba1a77c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113539"
---
# <a name="mfnetsource_enable_privatemode-property"></a>MFNETSOURCE \_ activer la \_ propriété PRIVATEMODE

Active le mode de téléchargement privé dans la source réseau.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**Boolean**

VT \_

**lVal**



## <a name="remarks"></a>Remarques

Si cette propriété a la **valeur true**, le cache est effacé à la fin de la session.

La constante **MFNETSOURCE \_ CLIENTGUID** définit le GUID de la clé de propriété. L’identificateur de propriété (PID) est égal à zéro. Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




