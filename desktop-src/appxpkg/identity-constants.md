---
title: Constantes d’identité (AppModel. h)
description: Spécifie la longueur des chaînes pour les champs d’identité du package.
ms.assetid: C4F81822-B502-4360-AEA4-829F1AB926BF
topic_type:
- apiref
api_name:
- APPLICATION_USER_MODEL_ID_MAX_LENGTH
- APPLICATION_USER_MODEL_ID_MIN_LENGTH
- PACKAGE_ARCHITECTURE_MAX_LENGTH
- PACKAGE_ARCHITECTURE_MIN_LENGTH
- PACKAGE_FAMILY_NAME_MAX_LENGTH
- PACKAGE_FAMILY_NAME_MIN_LENGTH
- PACKAGE_FULL_NAME_MAX_LENGTH
- PACKAGE_FULL_NAME_MIN_LENGTH
- PACKAGE_NAME_MAX_LENGTH
- PACKAGE_NAME_MIN_LENGTH
- PACKAGE_PUBLISHERID_MAX_LENGTH
- PACKAGE_PUBLISHERID_MIN_LENGTH
- PACKAGE_PUBLISHER_MAX_LENGTH
- PACKAGE_PUBLISHER_MIN_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH
- PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH
- PACKAGE_RESOURCEID_MAX_LENGTH
- PACKAGE_RESOURCEID_MIN_LENGTH
- PACKAGE_VERSION_MAX_LENGTH
- PACKAGE_VERSION_MIN_LENGTH
api_location:
- AppModel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681a0aef767afe92cdb93eee3849df8ed6a5f080
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510741"
---
# <a name="identity-constants"></a>Constantes d’identité

Spécifie la longueur des chaînes pour les champs d’identité du package. La longueur est mesurée en caractères et peut ou non inclure de l’espace pour la marque de fin NULL.

> [!Note]  
> Les constantes se présente sous la forme : la longueur de l' **\_ \_ ID du modèle \_ \_ \* \_ utilisateur** de l’application et la **\_ \_ \_ \_ \* \_ longueur de l’ID d’application relative du package** incluent l’espace pour une marque de fin null, mais les constantes se présente sous la forme : la **\_ \* \_ longueur du package** n’inclut pas d’espace pour un terminateur null.

 



| Constante/valeur                                                                                                                                                                                                                                                                                                   | Description                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_USER_MODEL_ID_MAX_LENGTH"></span><span id="application_user_model_id_max_length"></span><dl> <dt>**Application \_ ID du modèle utilisateur- \_ \_ \_ \_ longueur maximale**</dt> <dt>130</dt> </dl>                  | Longueur maximale de l’ID du modèle utilisateur de l’application. L’espace est inclus pour la marque de fin NULL.<br/>                             |
| <span id="APPLICATION_USER_MODEL_ID_MIN_LENGTH"></span><span id="application_user_model_id_min_length"></span><dl> <dt>**Application \_ ID du modèle utilisateur- \_ \_ \_ \_ longueur minimale**</dt> <dt>21</dt> </dl>                   | Longueur minimale de l’ID du modèle utilisateur de l’application. L’espace est inclus pour la marque de fin NULL.<br/>                             |
| <span id="PACKAGE_ARCHITECTURE_MAX_LENGTH"></span><span id="package_architecture_max_length"></span><dl> <dt>**Package \_ \_ \_ Longueur maximale**</dt> de l’architecture <dt>7</dt> </dl>                                     | Longueur maximale de l’architecture. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                          |
| <span id="PACKAGE_ARCHITECTURE_MIN_LENGTH"></span><span id="package_architecture_min_length"></span><dl> <dt>**Package \_ \_ \_ Longueur minimale**</dt> de l’architecture <dt>3</dt> </dl>                                     | Longueur minimale de l’architecture. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                          |
| <span id="PACKAGE_FAMILY_NAME_MAX_LENGTH"></span><span id="package_family_name_max_length"></span><dl> <dt>**Package \_ Nom de famille \_ \_ MAX \_ longueur**</dt> <dt>64</dt> </dl>                                      | Longueur maximale du nom de famille. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                           |
| <span id="PACKAGE_FAMILY_NAME_MIN_LENGTH"></span><span id="package_family_name_min_length"></span><dl> <dt>**Package \_ Nom de famille \_ \_ Min \_ Length**</dt> <dt>17</dt> </dl>                                      | Longueur minimale du nom de famille. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                           |
| <span id="PACKAGE_FULL_NAME_MAX_LENGTH"></span><span id="package_full_name_max_length"></span><dl> <dt>**Package \_ \_ \_ \_ Longueur maximale du nom complet**</dt> <dt>127</dt> </dl>                                           | Longueur maximale du nom complet. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                             |
| <span id="PACKAGE_FULL_NAME_MIN_LENGTH"></span><span id="package_full_name_min_length"></span><dl> <dt>**Package \_ \_ \_ \_ Longueur minimale de nom complet**</dt> <dt>30</dt> </dl>                                            | Longueur minimale du nom complet. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                             |
| <span id="PACKAGE_NAME_MAX_LENGTH"></span><span id="package_name_max_length"></span><dl> <dt>**Package \_ \_ \_ Longueur maximale du nom**</dt> <dt>50</dt> </dl>                                                            | Longueur maximale du nom. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                                  |
| <span id="PACKAGE_NAME_MIN_LENGTH"></span><span id="package_name_min_length"></span><dl> <dt>**Package \_ \_ \_ Longueur minimale de nom**</dt> <dt>3</dt> </dl>                                                             | Longueur minimale du nom. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                                  |
| <span id="PACKAGE_PUBLISHERID_MAX_LENGTH"></span><span id="package_publisherid_max_length"></span><dl> <dt>**Package \_ PUBLISHERID \_ \_ longueur max**</dt> . <dt>13</dt> </dl>                                       | Longueur maximale de l’ID de l’éditeur. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHERID_MIN_LENGTH"></span><span id="package_publisherid_min_length"></span><dl> <dt>**Package \_ PUBLISHERID \_ Min \_ longueur**</dt> <dt>13</dt> </dl>                                       | Longueur minimale de l’ID de l’éditeur. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                          |
| <span id="PACKAGE_PUBLISHER_MAX_LENGTH"></span><span id="package_publisher_max_length"></span><dl> <dt>**Package \_ \_ \_ Longueur max**</dt> . du serveur de publication <dt>8192</dt> </dl>                                           | Longueur maximale du serveur de publication. Par exemple, CN = serveur de *publication*. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                |
| <span id="PACKAGE_PUBLISHER_MIN_LENGTH"></span><span id="package_publisher_min_length"></span><dl> <dt>**Package \_ \_ \_ Longueur min**</dt> . du serveur de publication <dt>4</dt> </dl>                                              | Longueur minimale du serveur de publication. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                             |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MAX_LENGTH"></span><span id="package_relative_application_id_max_length"></span><dl> <dt>**Package \_ \_ \_ \_ \_ Longueur maximale de l’ID d’application relative**</dt> <dt>65</dt> </dl> | Longueur maximale de l’ID d’application relative du package. L’espace est inclus pour la marque de fin NULL.<br/>                       |
| <span id="PACKAGE_RELATIVE_APPLICATION_ID_MIN_LENGTH"></span><span id="package_relative_application_id_min_length"></span><dl> <dt>**Package \_ \_ \_ \_ \_ Longueur minimale de l’ID d’application relative**</dt> <dt>2</dt> </dl>  | Longueur minimale de l’ID d’application relative du package. L’espace est inclus pour la marque de fin NULL.<br/>                       |
| <span id="PACKAGE_RESOURCEID_MAX_LENGTH"></span><span id="package_resourceid_max_length"></span><dl> <dt>**Package \_ RESOURCEID \_ \_ longueur max**</dt> . <dt>30</dt> </dl>                                          | Longueur maximale de l’ID de ressource. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                           |
| <span id="PACKAGE_RESOURCEID_MIN_LENGTH"></span><span id="package_resourceid_min_length"></span><dl> <dt>**Package \_ RESOURCEID \_ Min \_ longueur**</dt> <dt>0</dt> </dl>                                           | Longueur minimale de l’ID de ressource. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                                           |
| <span id="PACKAGE_VERSION_MAX_LENGTH"></span><span id="package_version_max_length"></span><dl> <dt>**Package \_ \_ \_ Longueur maximale**</dt> de la version <dt>23</dt> </dl>                                                   | Longueur maximale de la version. Par exemple, *xxxxx*. *xxxxx*. *xxxxx*. *xxxxx*. Aucun espace n’est inclus pour la marque de fin NULL/<br/> |
| <span id="PACKAGE_VERSION_MIN_LENGTH"></span><span id="package_version_min_length"></span><dl> <dt>**Package \_ \_ \_ Longueur min**</dt> . de la version <dt>7</dt> </dl>                                                    | Longueur minimale de la version. Par exemple, *x*. *x*. *x*. *x*. Aucun espace n’est inclus pour la marque de fin NULL.<br/>                 |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>AppModel. h</dt> </dl> |



 

 





