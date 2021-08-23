---
title: Types de données IMAPi (Imapi2. h)
description: Les spécifications du support optique et des appareils associés définissent des valeurs de plage pour les éléments tels que la description de la structure du DVD, la description des informations sur le disque et la taille de la page de fonctionnalité.
ms.assetid: 8797a8d0-5ce5-4b16-9d41-c22fa0d67dcf
keywords:
- ULONG_IMAPI2_DVD_STRUCTURE
- ULONG_IMAPI2_ADAPTER_DESCRIPTOR
- ULONG_IMAPI2_DEVICE_DESCRIPTOR
- ULONG_IMAPI2_DISC_INFORMATION
- ULONG_IMAPI2_TRACK_INFORMATION
- ULONG_IMAPI2_FEATURE_PAGE
- ULONG_IMAPI2_MODE_PAGE
- ULONG_IMAPI2_ALL_FEATURE_PAGES
- ULONG_IMAPI2_ALL_PROFILES
- ULONG_IMAPI2_ALL_MODE_PAGES
- ULONG_IMAPI2_NONZERO
- ULONG_IMAPI2_NOT_NEGATIVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f003c2e03ff3d21623111d3d43a83cddf43e31c64557cfce18b5a401cdcd5d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612009"
---
# <a name="imapi-data-types"></a>Types de données IMAPi

Les spécifications du support optique et des appareils associés définissent des valeurs de plage pour les éléments tels que la description de la structure du DVD, la description des informations sur le disque et la taille de la page de fonctionnalité. IMAPi définit les types d’entiers longs non signés suivants (ULONG) qui appliquent des limites de valeurs de plage. Ces types sont définis de façon stricte pour une validation IDL optimale des paramètres et comme une aide de documentation aux appelants concernant les limites supérieures pour certaines opérations de transfert de données disponibles.


```C++
typedef ULONG ULONG_IMAPI2_DVD_STRUCTURE;
typedef ULONG ULONG_IMAPI2_ADAPTER_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DEVICE_DESCRIPTOR;
typedef ULONG ULONG_IMAPI2_DISC_INFORMATION;
typedef ULONG ULONG_IMAPI2_TRACK_INFORMATION;
typedef ULONG ULONG_IMAPI2_FEATURE_PAGE;
typedef ULONG ULONG_IMAPI2_MODE_PAGE;
typedef ULONG ULONG_IMAPI2_ALL_FEATURE_PAGES;
typedef ULONG ULONG_IMAPI2_ALL_PROFILES;
typedef ULONG ULONG_IMAPI2_ALL_MODE_PAGES;
typedef ULONG ULONG_IMAPI2_NONZERO;
typedef ULONG ULONG_IMAPI2_NOT_NEGATIVE;
```





| Type de données                                                                                                                                  | Description                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ULONG_IMAPI2_DVD_STRUCTURE"></span><span id="ulong_imapi2_dvd_structure"></span>**ULONG \_ imapi2 \_ , \_ structure de DVD**                | Plage : 0, 65535 (0, 0x0000FFFF)<br/> La structure du DVD est limitée à 64 Ko en raison d’un champ d’allocation de deux octets.<br/>                                                                                                                                                                                     |
| <span id="ULONG_IMAPI2_ADAPTER_DESCRIPTOR"></span><span id="ulong_imapi2_adapter_descriptor"></span>**\_Descripteur d’adaptateur imapi2 ulong \_ \_** | Plage : 0, 268435455 (0, 0x0FFFFFFF)<br/> La taille du descripteur de l’adaptateur n’est pas implicitement limitée.<br/>                                                                                                                                                                                                |
| <span id="ULONG_IMAPI2_DEVICE_DESCRIPTOR"></span><span id="ulong_imapi2_device_descriptor"></span>**\_Descripteur d’appareil imapi2 ulong \_ \_**    | Plage : 0, 268435455 (0, 0x0FFFFFFF)<br/> La taille du descripteur de périphérique n’est pas implicitement limitée.<br/>                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_DISC_INFORMATION"></span><span id="ulong_imapi2_disc_information"></span>**\_ \_ Informations sur le disque imapi2 ulong \_**       | Plage : 0, 65538 (0, 0x00010002)<br/> Les informations sur le disque sont limitées à 64 Ko plus 2 octets pour le champ taille.<br/>                                                                                                                                                                                         |
| <span id="ULONG_IMAPI2_TRACK_INFORMATION"></span><span id="ulong_imapi2_track_information"></span>**ULONG \_ imapi2 \_ suivre les \_ informations**    | Plage : 0, 65538 (0, 0x00010002)<br/> Les informations de suivi sont limitées à 64 Ko plus 2 octets pour le champ taille.<br/>                                                                                                                                                                                        |
| <span id="ULONG_IMAPI2_FEATURE_PAGE"></span><span id="ulong_imapi2_feature_page"></span>**ULONG \_ , \_ page de fonctionnalité imapi2 \_**                   | Plage : 0256 (0, 0x00000100)<br/> Une seule page de fonctionnalité est limitée à 256 octets.<br/>                                                                                                                                                                                                                 |
| <span id="ULONG_IMAPI2_MODE_PAGE"></span><span id="ulong_imapi2_mode_page"></span>**\_ \_ Page mode imapi2 \_ ULong**                            | Plage : 0257 (0, 0x00000101)<br/> Une page en mode unique est limitée à 257 octets.<br/>                                                                                                                                                                                                                    |
| <span id="ULONG_IMAPI2_ALL_FEATURE_PAGES"></span><span id="ulong_imapi2_all_feature_pages"></span>**ULONG \_ imapi2 \_ toutes \_ les \_ pages de fonctionnalités**   | Plage : 0, 65536 (0, 0x00010000)<br/> Le nombre de fonctionnalités est limité à un champ de 2 octets.<br/>                                                                                                                                                                                                       |
| <span id="ULONG_IMAPI2_ALL_PROFILES"></span><span id="ulong_imapi2_all_profiles"></span>**ULONG \_ imapi2 \_ tous les \_ profils**                   | Plage : 0, 63 (0, 0x0000003F)<br/> Le nombre de profils pour un appareil est le nombre de profils qui tiennent dans une seule fonctionnalité. Chaque profil occupe quatre octets. Une fonctionnalité unique peut contenir 252 octets de données supplémentaires, suffisants pour stocker un maximum de 63 profils.<br/>                                 |
| <span id="ULONG_IMAPI2_ALL_MODE_PAGES"></span><span id="ulong_imapi2_all_mode_pages"></span>**ULONG \_ imapi2 \_ toutes \_ les \_ pages en mode**            | Plage : 0, 32763 (0, 0x00007FFB)<br/> Nombre de pages de mode pour un appareil. Le nombre, via le MODE \_ SENSE10, est limité à un champ de 2 octets.<br/> L’en-tête de paramètre de mode est de 8 octets. Chaque page est d’au moins deux octets. Le nombre maximal de pages de mode est 32763 : (65535-8)/2 arrondi à la valeur inférieure.<br/> |
| <span id="ULONG_IMAPI2_NONZERO"></span><span id="ulong_imapi2_nonzero"></span>**ULONG \_ imapi2 \_ différent de zéro**                                   | Plage : 1, 2147483647 (1, 0x7FFFFFFF)<br/> Valeur différente de zéro générique qui peut être utilisée pour vérifier qu’une valeur n’est pas égale à zéro.<br/>                                                                                                                                                                              |
| <span id="ULONG_IMAPI2_NOT_NEGATIVE"></span><span id="ulong_imapi2_not_negative"></span>**ULONG \_ imapi2 \_ non \_ négatif**                   | Plage : 0, 2147483647 (0, 0x7FFFFFFF)<br/> Entier 32 bits avec une valeur non négative.<br/>                                                                                                                                                                                                              |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Imapi2. h</dt> </dl> |



 

 





