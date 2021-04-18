---
description: Définit le niveau de protection d’un mécanisme de protection de sortie.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522673"
---
# <a name="opm_set_protection_level"></a>niveau de protection de l' \_ ensemble OPM \_ \_

Définit le niveau de protection d’un mécanisme de protection de sortie.



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID de la commande | niveau de protection de l' \_ ensemble OPM \_ \_                                                                         |
| Données d’entrée   | Structure [**des \_ \_ paramètres de \_ niveau \_ de protection de l’ensemble OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Notes

Certains connecteurs peuvent prendre en charge plusieurs mécanismes de protection. Avec ce type de connecteur, vous pouvez appliquer plusieurs mécanismes de protection au même connecteur, avec des paramètres différents pour chacun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Commandes OPM](opm-commands.md)
</dt> </dl>

 

 




