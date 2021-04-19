---
description: Ces constantes sont utilisées par un TSP pour identifier le type de niveau de qualité de service (QoS) requis.
ms.assetid: 9fc3f6eb-7103-43c5-84f8-3842757e5be7
title: Constantes LINEQOSSERVICELEVEL_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c0629715e461a15e21e1730f86edb61d83d60db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534824"
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



 

 




