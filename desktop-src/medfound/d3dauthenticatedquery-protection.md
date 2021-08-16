---
description: Retourne le niveau de protection actuel de l’appareil.
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd91ee37187d8b2a6906d88832d06250b05c572d789d15db3b5621f78b890ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742609"
---
# <a name="d3dauthenticatedquery_protection"></a>\_Protection D3DAUTHENTICATEDQUERY

Retourne le niveau de protection actuel de l’appareil.



| Condition requise | Valeur |
|-------------|------------------------------------------------------------------------------------------------------------|
| GUID de la requête  | **\_Protection D3DAUTHENTICATEDQUERY**                                                                      |
| Données d’entrée  | [**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)                       |
| Retourner les données | [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_**](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a>Remarques

Cette requête est valide pour tous les types de canaux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Requêtes protection du contenu](content-protection-queries.md)
</dt> <dt>

[protection du contenu basé sur GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




