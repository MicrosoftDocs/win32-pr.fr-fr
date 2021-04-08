---
title: Constantes WINBIO_ORIENTATION ( \_ types WINBIO. h)
description: Les constantes suivantes spécifient les orientations d’appareil photo possibles que le composant capteur spécifie comme étant obligatoires.
ms.assetid: E44A6F17-5F38-47C7-947B-FB6FB79B1217
topic_type:
- apiref
api_name:
- WINBIO_ORIENTATION_UNSPECIFIED
- WINBIO_ORIENTATION_LANDSCAPE
- WINBIO_ORIENTATION_PORTRAIT
- WINBIO_ORIENTATION_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e5c3a3150819eff6311c03b8cd279fad7dcf398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844382"
---
# <a name="winbio_orientation-constants"></a>\_Constantes d’orientation WINBIO

Les constantes suivantes spécifient les orientations d’appareil photo possibles que le composant capteur spécifie comme étant obligatoires.



| Constante/valeur                                                                                                                                                                                                                                                           | Description                                                         |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| <span id="WINBIO_ORIENTATION_UNSPECIFIED"></span><span id="winbio_orientation_unspecified"></span><dl> <dt>**WINBIO \_ ORIENTATION \_ non spécifiée**</dt> <dt>0</dt> </dl> | Une orientation obligatoire pour l’appareil photo n’est pas spécifiée.<br/> |
| <span id="WINBIO_ORIENTATION_LANDSCAPE"></span><span id="winbio_orientation_landscape"></span><dl> <dt>**WINBIO \_ ORIENTATION \_ paysage**</dt> <dt>1</dt> </dl>       | L’orientation paysage est requise pour l’appareil photo.<br/>    |
| <span id="WINBIO_ORIENTATION_PORTRAIT"></span><span id="winbio_orientation_portrait"></span><dl> <dt>**WINBIO \_ ORIENTATION \_ portrait**</dt> <dt>2</dt> </dl>          | L’orientation portrait est requise pour l’appareil photo.<br/>     |
| <span id="WINBIO_ORIENTATION_ANY"></span><span id="winbio_orientation_any"></span><dl> <dt>**WINBIO \_ ORIENTATION \_ any**</dt> <dt>3</dt> </dl>                         | Toute orientation est autorisée pour l’appareil photo.<br/>             |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                                                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>WinBio \_ types. h (inclure WinBio. h pour les applications clientes ou les \_ cartes WinBio. h pour les adaptateurs)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ \_ informations sur le capteur étendu WINBIO \_**](winbio-extended-sensor-info.md)
</dt> </dl>

 

 





