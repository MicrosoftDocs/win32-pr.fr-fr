---
description: Contient un pointeur vers l’interface IMFNetProxyLocatorFactory.
ms.assetid: 455325c0-5116-4e81-9729-fab9c6a367c7
title: MFNETSOURCE_PROXYLOCATORFACTORY, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1199333e9eb343ab9d8f96864372b2dc385ab7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114595"
---
# <a name="mfnetsource_proxylocatorfactory-property"></a>MFNETSOURCE \_ propriété PROXYLOCATORFACTORY

Contient un pointeur vers l’interface [**IMFNetProxyLocatorFactory**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory) .



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**IUnknown** , pointeur

VT \_ inconnu

**punkVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ PROXYLOCATORFACTORY** définit le GUID de cette clé de propriété. L’identificateur de propriété (PID) est égal à zéro.

Les applications peuvent utiliser cette propriété pour fournir un localisateur de proxy personnalisé pour la source réseau. Pour définir la propriété, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

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

 

 




