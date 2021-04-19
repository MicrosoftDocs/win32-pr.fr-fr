---
title: Identificateurs de fournisseur intégrés (Fwpmu. h)
description: Les identificateurs des fournisseurs intégrés à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060f6d63d703d7c91e5538b7bfdd8758ee2e1cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510558"
---
# <a name="built-in-provider-identifiers"></a>Identificateurs de fournisseur intégrés

Les identificateurs des fournisseurs intégrés à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID.

Ces identificateurs sont définis comme suit.

<dl> <dt>

<span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**\_IKEEXT du fournisseur FWPM \_**
</dt> <dd> <dl> <dt>

{10ad9216-ccde-456c-8b16-e9f04e60a90b}
</dt> <dt>



Utilisé pour identifier tous les filtres ajoutés par IKE/AuthIP.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**\_ \_ \_ configuration dos IPSec du fournisseur FWPM \_**
</dt> <dd> <dl> <dt>

{3c6c0519-c05c-4bb9-8338-2327814ce8bf}
</dt> <dt>



Permet d’identifier tous les filtres ajoutés par la protection DoS IPsec.

> [!Note]  
> Disponible uniquement sur Windows 7 et Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_ \_ \_ déchargement TCP \_ Chimney du fournisseur FWPM**
</dt> <dd> <dl> <dt>

{896aa19e-9a34-4bcb-ae79-beb9127c84b9}
</dt> <dt>



Utilisé pour identifier tous les filtres ajoutés par le déchargement TCP Chimney.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**\_ \_ modèles TCP du fournisseur FWPM \_**
</dt> <dd> <dl> <dt>

{76cfcd30-3394-432d-bed3-441ae50e63c3}
</dt> <dt>



Utilisé pour identifier tous les filtres ajoutés par les modèles TCP.

> [!Note]  
> Disponible uniquement sur Windows 8 et Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





