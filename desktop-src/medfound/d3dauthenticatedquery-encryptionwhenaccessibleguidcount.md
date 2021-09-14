---
description: Retourne le nombre de types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9cd281836436c1d11fe07f7a43ecceebc8e3b12e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192531"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a>D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT

Retourne le nombre de types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.



| Condition requise | Valeur |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de la requête  | **D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**                                                                                 |
| Données d’entrée  | [**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)                                                         |
| Retourner les données | [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a>Notes

Les types de canaux suivants prennent en charge cette requête :

-   **\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**
-   **\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**

## <a name="requirements"></a>Spécifications



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

 

 




