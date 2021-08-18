---
description: Spécifie si le localisateur de proxy doit utiliser un serveur proxy pour les adresses locales.
ms.assetid: 384343f5-5919-44da-b8ea-0c994b4743a8
title: MFNETSOURCE_PROXYBYPASSFORLOCAL, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1de60371ac71e570b9c11abcbc255e20efe1793884ebb0746834d32a34353006
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954789"
---
# <a name="mfnetsource_proxybypassforlocal-property"></a>MFNETSOURCE \_ propriété PROXYBYPASSFORLOCAL

Spécifie si le localisateur de proxy doit utiliser un serveur proxy pour les adresses locales.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Boolean (**long**)

VT \_

**lVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ PROXYBYPASSFORLOCAL** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer le localisateur de proxy lors de la création de l’objet localisateur de proxy. Pour définir la propriété, transmettez un pointeur **IPropertyStore** dans le paramètre *pProxyConfig* de la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . La valeur doit être égale à 0 si le serveur proxy doit être utilisé pour les adresses locales. Sinon, une valeur différente de zéro configure le localisateur de proxy par défaut pour ignorer le serveur proxy pour les adresses locales.

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
</dt> <dt>

[Prise en charge du proxy pour les sources réseau](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




