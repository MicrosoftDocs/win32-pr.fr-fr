---
title: Constantes WINBIO_PROPERTY_TYPE (WinBio. h)
description: Spécifiez la source des informations de propriété dans la fonction WinBioGetProperty.
ms.assetid: 82C54092-032B-4F32-820E-A1D4BB81ECCE
topic_type:
- apiref
api_name:
- WINBIO_PROPERTY_TYPE_SESSION
- WINBIO_PROPERTY_TYPE_TEMPLATE
- WINBIO_PROPERTY_TYPE_UNIT
- WINBIO_PROPERTY_TYPE_ACCOUNT
api_location:
- Winbio.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7b7c17da736e117f099ec66dafc4ef2cfbba037f90a35f2522d7710cb3cef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909357"
---
# <a name="winbio_property_type-constants"></a>\_Constantes de type de propriété WINBIO \_

Les constantes de **\_ \_ type de propriété WINBIO** suivantes peuvent être utilisées pour spécifier la source des informations de propriété dans la fonction [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty) .

<dl> <dt>

<span id="WINBIO_PROPERTY_TYPE_SESSION"></span><span id="winbio_property_type_session"></span>**\_session de \_ type de propriété WINBIO \_**
</dt> <dd> <dl> <dt>



La propriété s’applique à une session biométrique spécifique.


</dt> </dl> </dd> <dt>

<span id="WINBIO_PROPERTY_TYPE_TEMPLATE"></span><span id="winbio_property_type_template"></span>**\_modèle de \_ type de propriété WINBIO \_**
</dt> <dd> <dl> <dt>



La propriété s’applique à un modèle biométrique spécifique.


</dt> </dl> </dd> <dt>

<span id="WINBIO_PROPERTY_TYPE_UNIT"></span><span id="winbio_property_type_unit"></span>**\_unité de \_ type de propriété WINBIO \_**
</dt> <dd> <dl> <dt>



La propriété s’applique à une unité biométrique spécifique.


</dt> </dl> </dd> <dt>

<span id="WINBIO_PROPERTY_TYPE_ACCOUNT"></span><span id="winbio_property_type_account"></span>**\_type de propriété WINBIO \_ \_ compte**
</dt> <dd> <dl> <dt>



La propriété s’applique à un compte d’utilisateur spécifique qui a une inscription biométrique. Cette valeur est prise en charge à partir de Windows 10.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>WinBio. h (inclure WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes d’application cliente](client-application-constants.md)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> </dl>

 

 





