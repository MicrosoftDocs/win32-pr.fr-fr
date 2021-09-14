---
description: Retourne l’un des types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192528"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a>D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID

Retourne l’un des types de chiffrement qui peuvent être utilisés pour chiffrer le contenu avant qu’il ne soit accessible au processeur ou au bus.



| Condition requise | Valeur |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| GUID de la requête  | **D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**                                                                            |
| Données d’entrée  | [**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYEVICTIONENCRYPTIONGUID \_**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| Retourner les données | [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

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

 

 




