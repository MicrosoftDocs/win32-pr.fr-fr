---
description: Stocke le pointeur IUnknown de la classe qui implémente l’interface IMFSSLCertificateManager.
ms.assetid: 13e05bda-96c2-4095-a266-74185760f33a
title: MFNETSOURCE_SSLCERTIFICATE_MANAGER, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf6e21962e3d521e8c5781d59b2e0fe6fed04aa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516195"
---
# <a name="mfnetsource_sslcertificate_manager-property"></a>\_Propriété MFNETSOURCE SSLCERTIFICATE \_ Manager

Stocke le pointeur **IUnknown** de la classe qui implémente l’interface [**IMFSSLCertificateManager**](/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager) . L’implémentation cliente fournit des méthodes pour récupérer le certificat SSL client lorsqu’il est demandé par le serveur.



Type de données

Type de PROPVARIANT (VT)

Membre PROPVARIANT

**IUnknown, pointeur**

VT \_ inconnu

**punkVal**



## <a name="remarks"></a>Notes

La constante **MFNETSOURCE \_ SSLCERTIFICATE \_ Manager** définit le GUID de la clé de propriété. L’identificateur de propriété (PID) est égal à zéro. Pour définir cette propriété sur la source réseau, transmettez un pointeur **IPropertyStore** au programme de résolution source. Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




