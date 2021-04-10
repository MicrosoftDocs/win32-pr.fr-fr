---
description: Définit le niveau de protection HDCP pour la lecture des DVD, en suivant les règles du système de brouillage du contenu DVD (CSS).
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114378"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a>\_ \_ niveau de protection de l’ensemble OPM \_ selon le \_ \_ \_ \_ DVD CSS

Définit le niveau de protection HDCP pour la lecture des DVD, en suivant les règles du système de brouillage du contenu DVD (CSS).



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------------------------------|
| GUID de la commande | \_ \_ niveau de protection de l’ensemble OPM \_ selon le \_ \_ \_ \_ DVD CSS                                                |
| Données d’entrée   | Structure [**des \_ \_ paramètres de \_ niveau \_ de protection de l’ensemble OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) |



 

## <a name="remarks"></a>Notes

Cette commande permet de définir High-Bandwidth protection du contenu numérique (HDCP) lors de la diffusion de DVD standard. Contrairement à la commande de [**\_ \_ \_ niveau de protection Set de OPM**](opm-set-protection-level.md) , si HDCP ne peut pas être défini pour une raison quelconque, cette commande n’arrête pas la lecture. (Les règles CSS de DVD contiennent un « meilleur effort » pour les joueurs.) Dans le cas contraire, cette commande est identique à la commande de **\_ \_ \_ niveau de protection Set OPM** .

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

 

 




