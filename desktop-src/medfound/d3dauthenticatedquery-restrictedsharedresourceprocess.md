---
description: Retourne des informations sur un processus autorisé à ouvrir des ressources partagées avec un accès restreint.
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520308"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a>D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS

Retourne des informations sur un processus autorisé à ouvrir des ressources partagées avec un accès restreint.



| Condition requise | Valeur |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de la requête  | **D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**                                                                                           |
| Données d’entrée  | [**\_Entrée D3DAUTHENTICATEDCHANNEL QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| Retourner les données | [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a>Notes

Les types de canaux suivants prennent en charge cette requête :

-   **D3DAUTHENTICATEDCHANNEL \_ d3d9**
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

 

 




