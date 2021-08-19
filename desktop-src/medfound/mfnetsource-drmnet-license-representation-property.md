---
description: Stocke un tableau d’octets qui représente la licence DRM associée au flux d’octets.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2718ba8a13d8d0c00114449f1141be77db0d3f83930d3b3de2171719c3bdf2d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113549"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>\_Propriété de \_ représentation de licence MFNETSOURCE DRMNET \_

Stocke un tableau d’octets qui représente la licence DRM associée au flux d’octets.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Tableau d’octets (**BLOB**)

\_objet BLOB VT

**objet BLOB**



## <a name="remarks"></a>Remarques

La **représentation de \_ \_ licence MFNETSOURCE \_ DRMNET** constante définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Cette propriété est en lecture seule. Pour récupérer la valeur de la propriété à partir du flux d’octets réseau, appelez **IPropertyStore :: GetValue** et transmettez la structure **PROPERTYKEY** dans le paramètre *Key* . Le membre **fmtid** de **PROPERTYKEY** doit avoir la valeur GUID de la propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




