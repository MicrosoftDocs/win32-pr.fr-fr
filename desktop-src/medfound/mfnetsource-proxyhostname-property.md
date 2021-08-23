---
description: Spécifie le nom d’hôte du serveur proxy.
ms.assetid: e53c86e9-c326-41c9-aa86-c80a750b9ce3
title: MFNETSOURCE_PROXYHOSTNAME, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82746763c937bdca388782cb0882b536c0b9e93b660e0f8e0a04426e5b48a61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663669"
---
# <a name="mfnetsource_proxyhostname-property"></a>MFNETSOURCE \_ propriété PROXYHOSTNAME

Spécifie le nom d’hôte du serveur proxy.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Chaîne de caractères larges (**WCHAR** \* )

\_LPWStr VT

**pwszVal**



## <a name="remarks"></a>Remarques

La constante **MFNETSOURCE \_ PROXYHOSTNAME** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer le localisateur de proxy par défaut lors de la création de l’objet localisateur de proxy. Pour définir la propriété, transmettez un pointeur **IPropertyStore** dans le paramètre *pProxyConfig* de la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . Cette propriété doit être définie par l’application lorsque le localisateur de proxy est configuré pour fonctionner en mode manuel.

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

 

 




