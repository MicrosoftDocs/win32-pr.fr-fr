---
description: Obtient la valeur mérite d’un codec matériel.
ms.assetid: 51987a79-78bf-41b2-8349-8c2725dd89d6
title: OPM_GET_CODEC_INFO (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 988ffa9a962d9ed04b6a978da1534a6da4fa506e873d89d238bcbb2aa00fd865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847979"
---
# <a name="opm_get_codec_info"></a>\_informations sur l’extraction de \_ codec OPM \_

Obtient la valeur mérite d’un codec matériel.



| Condition requise | Valeur |
|--------------|-------------------------------------------------------------------------------------------|
| GUID de la demande | **\_informations sur l’extraction de \_ codec OPM \_**                                                                 |
| Données d’entrée   | Une structure de [**\_ \_ \_ \_ paramètres d’extraction de codec OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)   |
| Retourner les données  | Structure d’informations de l' [**\_ extraction de \_ codec \_ \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) |



 

## <a name="remarks"></a>Remarques

Bien que cette commande utilise l’interface de [sortie Protection Manager](output-protection-manager.md) (OPM), elle s’applique uniquement aux encodeurs et aux décodeurs matériels. Elle ne s’applique pas aux périphériques de sortie vidéo.

En règle générale, vous ne devez pas utiliser cette commande directement. Pour obtenir la valeur mérite d’un codec matériel, appelez la fonction [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) . Cette fonction effectue tous les appels OPM nécessaires à l’envoi de la commande d' **\_ extraction d' \_ \_ informations de codec OPM** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Demandes d’État OPM](opm-status-requests.md)
</dt> <dt>

[Gestionnaire de protection de sortie](output-protection-manager.md)
</dt> <dt>

[**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> </dl>

 

 




