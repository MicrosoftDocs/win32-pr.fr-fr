---
description: Les \_ constantes LINEOPENOPTION répertorient les options disponibles pour l’ouverture d’une ligne.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Constantes LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0dc6a4780b366b2dce08110ecce40c7140ab1d0956d788dce5a67d5d0501b6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739249"
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

## <a name="remarks"></a>Remarques

Pour plus d’informations sur le fonctionnement de ces options, consultez [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




