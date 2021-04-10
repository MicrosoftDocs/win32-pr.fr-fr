---
title: Constantes WINBIO_DB ( \_ types WINBIO. h)
description: Spécifiez la base de données à utiliser pour un pool système.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104368"
---
# <a name="winbio_db-constants"></a>\_Constantes WINBIO DB

Les constantes suivantes peuvent être utilisées lors de l’appel de [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) pour spécifier la base de données à utiliser pour un pool système.



| Constante                                                                                                                                                                         | Description                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**WINBIO \_ DB \_ par défaut**</dt> </dl>       | Chaque unité biométrique du pool de capteurs utilise la base de données par défaut spécifiée dans la configuration d’unité biométrique par défaut.<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**démarrage de WINBIO \_ DB \_**</dt> </dl> | Peut être utilisé pour les scénarios avant le démarrage de Windows. En règle générale, la base de données fait partie de la puce de capteur ou fait partie du BIOS et ne peut être utilisée que pour l’inscription et la suppression d’un modèle.<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**WINBIO \_ DB \_ ONCHIP**</dt> </dl>          | La base de données réside sur la puce du capteur.<br/>                                                                                                                                                  |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





