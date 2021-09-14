---
title: Constantes WINBIO_DATABASE_TYPE ( \_ types WINBIO. h)
description: Indicateurs qui peuvent être utilisés pour le membre Attributes de la \_ structure de schéma de stockage WINBIO \_ .
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095965"
---
# <a name="winbio_database_type-constants"></a>\_Constantes de type de base de données WINBIO \_

Les indicateurs suivants peuvent être utilisés pour le membre **attributes** de la structure de [**\_ \_ schéma de stockage WINBIO**](winbio-storage-schema.md) .



| Constante/valeur                                                                                                                                                                                                                                                                     | Description                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Masque de type de base de données**</dt> <dt>0x0000FFFF</dt> </dl>                | Représente un masque pour tous les \_ bits de type \_ .<br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <dt>**WINBIO \_ \_ \_ Fichier de type base de données**</dt> <dt>0x00000001</dt> </dl>                | La base de données est contenue dans un fichier.<br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <dt>**WINBIO \_ TYPE de base de données \_ \_ SGBD**</dt> <dt>0x00000002</dt> </dl>                | La base de données est gérée par un composant de système de gestion de base de données externe (SGBD), tel que Microsoft SQL Server.<br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <dt>**WINBIO \_ TYPE de base de données \_ \_ ONCHIP**</dt> <dt>0x00000003</dt> </dl>          | La base de données réside sur le capteur biométrique.<br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <dt>**WINBIO \_ TYPE de base de données \_ \_ Smartcard**</dt> <dt>0x00000004</dt> </dl> | La base de données réside sur une carte à puce.<br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <dt>**WINBIO \_ \_ \_ Masque d’indicateur de base de données**</dt> <dt>0xFFFF0000</dt> </dl>                | Représente un masque pour tous les \_ bits d’indicateur \_ .<br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <dt>**WINBIO \_ Indicateur de base de données 0x00010000 \_ \_ amovible**</dt> <dt></dt> </dl> | Le support de stockage contenant la base de données peut être physiquement supprimé de l’ordinateur.<br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <dt>**WINBIO \_ Indicateur de base de données 0x00020000 \_ \_ à distance**</dt> <dt></dt> </dl>          | La base de données se trouve sur un ordinateur distant.<br/>                                                                        |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (include WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> </dl>

 

 





