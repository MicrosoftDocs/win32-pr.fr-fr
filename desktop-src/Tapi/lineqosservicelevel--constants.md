---
description: Ces constantes sont utilisées par un TSP pour identifier le type de niveau de qualité de service (QoS) requis.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: Constantes LINEQOSSERVICELEVEL_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a74a4508b54a8b56e8e9cb359f966122c5c009f0e5ede0f1b8544cd1e46330c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003007"
---
# <a name="lineqosservicelevel_-constants"></a>\_Constantes LINEQOSSERVICELEVEL

Ces constantes sont utilisées par un TSP pour identifier le type de niveau de qualité de service (QoS) requis.

<dl> <dt>

<span id="LINEQOSSERVICELEVEL_NEEDED"></span><span id="lineqosservicelevel_needed"></span>**LINEQOSSERVICELEVEL \_ nécessaire**
</dt> <dd> <dl> <dt>

 0x00000001
</dt> <dt>



Le niveau de qualité de service demandé est obligatoire.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_IFAVAILABLE"></span><span id="lineqosservicelevel_ifavailable"></span>**LINEQOSSERVICELEVEL \_ IFAVAILABLE**
</dt> <dd> <dl> <dt>

 0x00000002
</dt> <dt>



Niveau de qualité de service requis, s’il est disponible.


</dt> </dl> </dd> <dt>

<span id="LINEQOSSERVICELEVEL_BESTEFFORT"></span><span id="lineqosservicelevel_besteffort"></span>**LINEQOSSERVICELEVEL \_ BESTEFFORT**
</dt> <dd> <dl> <dt>

 0x00000003
</dt> <dt>



Le niveau de qualité de service requis est « meilleur effort ».


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



 

 




