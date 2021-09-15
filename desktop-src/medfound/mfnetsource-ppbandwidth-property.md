---
description: Spécifie la bande passante de paire de paquets et la bande passante d’exécution détectée par la source réseau.
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: MFNETSOURCE_PPBANDWIDTH, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530689"
---
# <a name="mfnetsource_ppbandwidth-property"></a>MFNETSOURCE \_ propriété PPBANDWIDTH

Spécifie la bande passante de paire de paquets et la bande passante d’exécution détectée par la source réseau. La valeur de la propriété est un tableau de deux valeurs :

-   Bande passante de paires de paquets, en bits par seconde.
-   Bande passante d’exécution, en bits par seconde.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Tableau de valeurs **ULong** (**CAUL**)

VT \_ Vector \| VT \_ UI4

**caul**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ PPBANDWIDTH** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Cette propriété est en lecture seule. Pour récupérer cette propriété, interrogez la source réseau de l’interface **IPropertyStore** et appelez **IPropertyStore :: GetValue**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Fonctionnalités de la source réseau](network-source-features.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




