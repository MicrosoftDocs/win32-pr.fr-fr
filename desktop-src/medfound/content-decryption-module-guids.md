---
description: Les GUID suivants prennent en charge les implémentations de module de déchiffrement de contenu (CDM).
title: GUID du module de déchiffrement du contenu (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525241"
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


 

 




