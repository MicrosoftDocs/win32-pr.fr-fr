---
title: Identificateurs de poids de filtre (Fwpmu. h)
description: Identificateurs de poids de filtre utilisés par le moteur de filtrage de base (BFE) pour calculer les pondérations de filtre générées automatiquement.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513629"
---
# <a name="filter-weight-identifiers"></a>Identificateurs de poids de filtre

Les identificateurs de poids de filtre utilisés par le moteur de filtrage de base (BFE) pour calculer les pondérations de filtre générées automatiquement sont répertoriés ci-dessous.

Pour plus d’informations sur la génération de poids de filtre, consultez [assignation de poids de filtre](filter-weight-assignment.md) .

<dl> <dt>

<span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**\_bits de \_ poids \_ automatique FWPM**
</dt> <dd> <dl> <dt>

(60)
</dt> <dt>



Nombre de bits utilisés pour les pondérations de filtre générées automatiquement.


</dt> </dl> </dd> <dt>

<span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM \_ - \_ poids automatique \_ maximal**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 4)
</dt> <dt>



Poids maximal du filtre généré automatiquement.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ \_ exemptions IKE de la plage de poids FWPM \_**
</dt> <dd> <dl> <dt>

0XC
</dt> <dt>



BFE affecte un poids avec cette valeur de plage aux filtres IKE et AuthIP.

Pour plus d’informations sur les filtres IKE/AuthIP, consultez [exemptions IKE/AuthIP](ike-exemptions.md) .


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**\_plage de poids FWPM \_ \_ IPSec**
</dt> <dd> <dl> <dt>

(0x0)
</dt> <dt>



BFE affecte un poids avec cette valeur de plage aux filtres de stratégie IPsec.


</dt> </dl> </dd> <dt>

<span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM \_ de \_ poids \_ maximal**
</dt> <dd> <dl> <dt>

(**MAXUINT64** >> 60)
</dt> <dt>



Valeur maximale de la plage de poids du filtre autorisée.


</dt> </dl> </dd> </dl>

> [!Note]  
> **MAXUINT64** représente la plus grande valeur possible de **UINT64**. La valeur de cette constante est 0xFFFFFFFFFFFFFFFF.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





