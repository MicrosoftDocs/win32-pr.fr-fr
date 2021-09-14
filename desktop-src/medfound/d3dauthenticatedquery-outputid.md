---
description: Retourne l’un des identificateurs de sortie qui est associé à une session de chiffrement et un périphérique Direct3D spécifiés.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122178"
---
# <a name="d3dauthenticatedquery_outputid"></a>D3DAUTHENTICATEDQUERY \_ OUTPUTID

Retourne l’un des identificateurs de sortie qui est associé à une session de chiffrement et un périphérique Direct3D spécifiés.



| Condition requise | Valeur |
|-------------|--------------------------------------------------------------------------------------------------------|
| GUID de la requête  | **D3DAUTHENTICATEDQUERY \_ OUTPUTID**                                                                    |
| Données d’entrée  | [**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYOUTPUTID \_**](d3dauthenticatedchannel-queryoutputid-input.md)   |
| Retourner les données | [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_**](d3dauthenticatedchannel-queryoutputid-output.md) |



 

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

 

 




