---
description: Les \_ constantes LINEOPENOPTION répertorient les options disponibles pour l’ouverture d’une ligne.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Constantes LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541675"
---
# <a name="lineopenoption_-constants"></a>\_Constantes LINEOPENOPTION

Les **\_ constantes LINEOPENOPTION** répertorient les options disponibles pour l’ouverture d’une ligne.

<dl> <dt>

<span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_proxy LINEOPENOPTION**
</dt> <dd> <dl> <dt>



L’application est prête à gérer les demandes d’autres applications pour lesquelles la ligne est ouverte.


</dt> </dl> </dd> <dt>

<span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**
</dt> <dd> <dl> <dt>



L’application doit être informée des nouveaux appels créés sur le périphérique de ligne uniquement si ces appels apparaissent à l’adresse spécifiée dans le membre **dwAddressID** de la structure [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) désignée par le paramètre *lpCallParams* .


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Pour plus d’informations sur le fonctionnement de ces options, consultez [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




