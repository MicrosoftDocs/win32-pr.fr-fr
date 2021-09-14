---
description: Définit le niveau de chiffrement effectué avant que le contenu protégé soit accessible au processeur ou au bus.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8b624c26c81549372e0e09b4a08ce73f6cd3dd27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196811"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a>D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE

Définit le niveau de chiffrement effectué avant que le contenu protégé soit accessible au processeur ou au bus.



| Condition requise | Valeur |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| GUID de la commande | **D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**                                                                     |
| Données d’entrée   | [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

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

[Commandes protection du contenu](content-protection-commands.md)
</dt> <dt>

[protection du contenu basé sur GPU](gpu-based-content-protection.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




