---
description: Contient des données d’entrée pour une \_ commande D3DAUTHENTICATEDCONFIGURE Initialize.
ms.assetid: 08677cb3-6f08-49d5-a3b6-c48c88516273
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 072d7886a024b1c28e8c3b7f0609dc8dd3e6add8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033811"
---
# <a name="d3dauthenticatedchannel_configureinitialize-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE, structure

Contient des données d’entrée pour une commande [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .

Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT Parameters;
  UINT                                    StartSequenceQuery;
  UINT                                    StartSequenceConfigure;
} D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Paramètres**
</dt> <dd>

Un [**D3DAUTHENTICATEDCHANNEL \_ configure une structure \_ d’entrée**](d3dauthenticatedchannel-configure-input.md) qui contient le GUID de la commande et d’autres données.

</dd> <dt>

**StartSequenceQuery**
</dt> <dd>

Numéro de séquence initial pour les requêtes.

</dd> <dt>

**StartSequenceConfigure**
</dt> <dd>

Numéro de séquence initial pour les commandes.

</dd> </dl>

## <a name="remarks"></a>Notes

Les membres **StartSequenceQuery** et **StartSequenceConfigure** contiennent chacun un nombre aléatoire 32 bits sécurisé par chiffrement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




