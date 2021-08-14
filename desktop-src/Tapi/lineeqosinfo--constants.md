---
description: Ces constantes sont utilisées par un TSP pour identifier le résultat d’une demande QoS (Quality of service).
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: Constantes LINEEQOSINFO_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c07a2d532e578b1f7df752cfd4930660d1d22dd4dd8406f0f8cc8bd61924bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761392"
---
# <a name="lineeqosinfo_-constants"></a>\_Constantes LINEEQOSINFO

Ces constantes sont utilisées par un TSP pour identifier le résultat d’une demande QoS (Quality of service).

<dl> <dt>

<span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO \_ NOQOS**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



QoS n’est pas disponible.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO \_ ADMISSIONFAILURE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



La demande QoS n’a pas pu être satisfaite.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO \_ POLICYFAILURE**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Le type de QoS demandé n’est pas pris en charge.


</dt> </dl> </dd> <dt>

<span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO \_ erreur générique**
</dt> <dd> <dl> <dt>

 0x00000004
</dt> <dt>



Erreur QoS non spécifiée.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




