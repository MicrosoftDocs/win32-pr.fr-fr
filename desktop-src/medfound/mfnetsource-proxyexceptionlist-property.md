---
description: Spécifie une liste délimitée par des points-virgules de serveurs multimédias qui peuvent accepter des connexions à partir d’applications clientes sans utiliser de serveur proxy.
ms.assetid: 218883c5-9a26-4733-8308-1827cf1f2cd7
title: MFNETSOURCE_PROXYEXCEPTIONLIST, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e87c07068d31cdd5e9762dab14e2a61edbe9c8f90f8750acc1b23c851ad47c1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113489"
---
# <a name="mfnetsource_proxyexceptionlist-property"></a>MFNETSOURCE \_ propriété PROXYEXCEPTIONLIST

Spécifie une liste délimitée par des points-virgules de serveurs multimédias qui peuvent accepter des connexions à partir d’applications clientes sans utiliser de serveur proxy.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Chaîne de caractères larges (**WCHAR** \* )

\_LPWStr VT

**pwszVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ PROXYEXCEPTIONLIST** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer le localisateur de proxy lors de la création de l’objet localisateur de proxy. Pour définir la propriété, transmettez un pointeur **IPropertyStore** dans le paramètre *pProxyConfig* de la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . Le localisateur de proxy n’effectue pas la détection du proxy pour ces adresses.

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

 

 




