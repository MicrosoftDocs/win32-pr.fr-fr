---
description: La \_ propriété AudioEngine \_ OEMFormat spécifie le format par défaut de l’appareil utilisé pour le rendu ou la capture d’un flux. Les valeurs sont remplies par le fabricant d’ordinateurs OEM dans un fichier. inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114845"
---
# <a name="pkey_audioengine_oemformat"></a>\_AudioEngine \_ OEMFormat

La \_ propriété AudioEngine \_ OEMFormat spécifie le format par défaut de l’appareil utilisé pour le rendu ou la capture d’un flux. Les valeurs sont remplies par le fabricant d’ordinateurs OEM dans un fichier. inf.

Le membre **VT** de la structure **PROPVARIANT** est défini sur l' \_ objet BLOB VT.

Le membre **BLOB** de la structure **PROPVARIANT** est une structure de type **BLOB** qui contient deux membres. BLOB de membre **. cbSize** est une **valeur DWORD** qui spécifie le nombre d’octets dans la description de format. BLOB de membre **. pBlobData** pointe vers une structure **WAVEFORMATEX** qui contient la description de format. pour plus d’informations sur les objets BLOB, consultez la documentation SDK Windows. pour plus d’informations sur **WAVEFORMATEX**, consultez la documentation Windows DDK.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




