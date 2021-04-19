---
description: Les éléments WIA (Windows Image Acquisition) 2,0 sont regroupés en catégories qui définissent la façon dont un IWiaItem2 doit être traité ou utilisé.
ms.assetid: 927f4957-aedf-4eef-8892-91cf9b56e1a2
title: GUID de catégorie d’élément WIA 2,0 (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CATEGORY_AUTO
- WIA_CATEGORY_FEEDER
- WIA_CATEGORY_FEEDER_BACK
- WIA_CATEGORY_FEEDER_FRONT
- WIA_CATEGORY_FILM
- WIA_CATEGORY_FINISHED_FILE
- WIA_CATEGORY_FLATBED
- WIA_CATEGORY_FOLDER
- WIA_CATEGORY_ROOT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: e2785d7d82e28641ebeefad730f02b3561a537a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544673"
---
# <a name="wia-20-item-category-guids"></a>GUID de catégorie d’élément WIA 2,0

Les éléments WIA (Windows Image Acquisition) 2,0 sont regroupés en catégories qui définissent la façon dont un [**IWiaItem2**](-wia-iwiaitem2.md) doit être traité ou utilisé. Par exemple, si l’élément représente un flux, l’application doit s’attendre à ce qu’il contienne les propriétés du chargeur de documents requis et fonctionne comme un chargeur de documents. Si l’élément représente un fichier fini, une application WIA 2,0 doit la traiter ainsi, en supposant que les données sont statiques et situées sur l’appareil. (Les règles pour chaque élément sont définies dans leurs documents de spécification individuels.) Chaque catégorie a une constante de type GUID.



| Constante                                                                                                                                                                                               | Description                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_CATEGORY_AUTO"></span><span id="wia_category_auto"></span><dl> <dt>**WIA \_ catégorie \_ auto**</dt> </dl>                             | Élément qui représente les paramètres de configuration automatique pour un périphérique de scanneur WIA 2,0 qui prend en charge l’analyse configurée automatiquement.<br/>                                   |
| <span id="WIA_CATEGORY_FEEDER"></span><span id="wia_category_feeder"></span><dl> <dt>**\_chargeur de catégorie WIA \_**</dt> </dl>                       | Élément de chargeur qui est une source de données programmable et qui respecte les règles standard et les jeux de propriétés requis pour prendre en charge les flux de documents.<br/>                             |
| <span id="WIA_CATEGORY_FEEDER_BACK"></span><span id="wia_category_feeder_back"></span><dl> <dt>**\_retour du \_ chargeur de catégorie WIA \_**</dt> </dl>       | Source de données programmable décrivant la source de données de l’arrière-plan d’un élément de chargeur de base duplex.<br/>                                                                       |
| <span id="WIA_CATEGORY_FEEDER_FRONT"></span><span id="wia_category_feeder_front"></span><dl> <dt>**\_chargeur de catégorie WIA \_ \_ avant**</dt> </dl>    | Source de données programmable décrivant la source de données frontale d’un élément de chargeur de base duplex.<br/>                                                                      |
| <span id="WIA_CATEGORY_FILM"></span><span id="wia_category_film"></span><dl> <dt>**\_film de catégorie WIA \_**</dt> </dl>                             | Élément de film qui est une source de données programmable et qui respecte les règles standard et les jeux de propriétés requis pour prendre en charge les unités de numérisation de film.<br/>                            |
| <span id="WIA_CATEGORY_FINISHED_FILE"></span><span id="wia_category_finished_file"></span><dl> <dt>**\_fichier de catégorie WIA \_ terminé \_**</dt> </dl> | Élément qui n’est pas une source de données programmable, ou élément qui fournit des données dans un format de fichier terminé, ou un élément de dossier qui contient les éléments de format de fichier terminés.<br/> |
| <span id="WIA_CATEGORY_FLATBED"></span><span id="wia_category_flatbed"></span><dl> <dt>**\_plateau de catégorie WIA \_**</dt> </dl>                    | Élément à plat qui est une source de données programmable et qui respecte les règles standard et les jeux de propriétés requis pour prendre en charge l’analyse du plateau à plat.<br/>                     |
| <span id="WIA_CATEGORY_FOLDER"></span><span id="wia_category_folder"></span><dl> <dt>**\_dossier de catégorie WIA \_**</dt> </dl>                       | Un élément de stockage de dossier (pas une source de données programmable) contenant d’autres éléments de dossier ou des fichiers finis, ou les deux.<br/>                                                     |
| <span id="WIA_CATEGORY_ROOT"></span><span id="wia_category_root"></span><dl> <dt>**\_racine de catégorie WIA \_**</dt> </dl>                             | Élément racine de l’appareil. <br/>                                                                                                                                      |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




