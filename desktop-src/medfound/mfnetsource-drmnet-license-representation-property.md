---
description: Stocke un tableau d’octets qui représente la licence DRM associée au flux d’octets.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753125"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a>\_Propriété de \_ représentation de licence MFNETSOURCE DRMNET \_

Stocke un tableau d’octets qui représente la licence DRM associée au flux d’octets.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Tableau d’octets (**BLOB**)

\_objet BLOB VT

**objet BLOB**



## <a name="remarks"></a>Notes

La **représentation de \_ \_ licence MFNETSOURCE \_ DRMNET** constante définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Cette propriété est en lecture seule. Pour récupérer la valeur de la propriété à partir du flux d’octets réseau, appelez **IPropertyStore :: GetValue** et transmettez la structure **PROPERTYKEY** dans le paramètre *Key* . Le membre **fmtid** de **PROPERTYKEY** doit avoir la valeur GUID de la propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




