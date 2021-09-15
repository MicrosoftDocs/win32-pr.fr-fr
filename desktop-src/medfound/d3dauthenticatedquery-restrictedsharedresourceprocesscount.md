---
description: Retourne le nombre de processus autorisés à ouvrir des ressources partagées avec un accès restreint.
ms.assetid: e1b9ef18-fd08-4639-9ba9-4bccd33f5d16
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESSCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5238d027b5fe8ed7ebd1ab941b3877d5b545239b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520305"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocesscount"></a>D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT

Retourne le nombre de processus autorisés à ouvrir des ressources partagées avec un accès restreint.



| Condition requise | Valeur |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de la requête  | **D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**                                                                                                |
| Données d’entrée  | [**\_Entrée de requête D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)                                                                           |
| Retourner les données | [**Sortie de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md) |



 

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

 

 




