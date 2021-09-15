---
description: Permet à un processus d’ouvrir une ressource partagée ou désactive l’ouverture de ressources partagées par un processus.
ms.assetid: 5fa2b88f-e946-436c-953e-04e0e338146c
title: D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_SHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7404a4bed3ac3b1d4002bb03c45d7732500b77e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521481"
---
# <a name="d3dauthenticatedconfigure_sharedresource"></a>D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE

Permet à un processus d’ouvrir une ressource partagée ou désactive l’ouverture de ressources partagées par un processus.



| Condition requise | Valeur |
|--------------|-------------------------------------------------------------------------------------------------------------|
| GUID de la commande | **D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**                                                               |
| Données d’entrée   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**](d3dauthenticatedchannel-configuresharedresource.md) |



 

## <a name="remarks"></a>Notes

Les types de canaux suivants prennent en charge cette requête :

-   **D3DAUTHENTICATEDCHANNEL de \_ pilote \_ d3d9**
-   **\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Commandes protection du contenu](content-protection-commands.md)
</dt> <dt>

[protection du contenu basé sur GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




