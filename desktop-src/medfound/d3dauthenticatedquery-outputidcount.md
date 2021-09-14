---
description: Retourne le nombre d’identificateurs de sortie associés à une session de chiffrement et un périphérique Direct3D spécifiés.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122177"
---
# <a name="d3dauthenticatedquery_outputidcount"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT

Retourne le nombre d’identificateurs de sortie associés à une session de chiffrement et un périphérique Direct3D spécifiés.



| Condition requise | Valeur |
|-------------|------------------------------------------------------------------------------------------------------------------|
| GUID de la requête  | **D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**                                                                         |
| Données d’entrée  | [**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYOUTPUTIDCOUNT \_**](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| Retourner les données | [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_**](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

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

 

 




