---
description: Spécifie si le localisateur de proxy par défaut doit forcer la détection automatique de proxy.
ms.assetid: ab547a92-94a2-482e-b7ac-aeb3fdfb6b91
title: MFNETSOURCE_PROXYRERUNAUTODETECTION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37021c7e96b135389f0dffa2f8c26b8067df2b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528227"
---
# <a name="mfnetsource_proxyrerunautodetection-property"></a>MFNETSOURCE \_ propriété PROXYRERUNAUTODETECTION

Spécifie si le localisateur de proxy par défaut doit forcer la détection automatique de proxy.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

Boolean (**long**)

VT \_

**lVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ PROXYSETTINGS** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour configurer le localisateur de proxy lors de la création de l’objet localisateur de proxy. Pour définir la propriété, transmettez un pointeur **IPropertyStore** dans le paramètre *pProxyConfig* de la fonction [**MFCreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateproxylocator) . En mode de détection automatique, le localisateur de proxy utilise le mécanisme de détection de proxy WinInet. Pour forcer la détection automatique, définissez la valeur sur 0.

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
</dt> <dt>

[Prise en charge du proxy pour les sources réseau](proxy-support-for-network-sources.md)
</dt> </dl>

 

 




