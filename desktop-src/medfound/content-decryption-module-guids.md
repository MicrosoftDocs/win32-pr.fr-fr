---
description: Les GUID suivants prennent en charge les implémentations de module de déchiffrement de contenu (CDM).
title: GUID du module de déchiffrement du contenu (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: ef4016b731b492ed61c6aed859a905446de72c308e03a734aa3cc8f573645668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958779"
---
# <a name="content-decryption-module-cdm-guids"></a>GUID du module de déchiffrement du contenu (CDM)

Les GUID suivants prennent en charge les implémentations de module de déchiffrement de contenu (CDM).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

GUID de service utilisé pour obtenir des interfaces à partir d’une implémentation de [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , telle que l’interface [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) WinRT. Une implémentation de **IMFContentDecryptionModule** doit implémenter [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) et prendre en charge ce GUID de service.


## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi



- [Constantes Media Foundation](media-foundation-constants.md)
- [IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule
- [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




