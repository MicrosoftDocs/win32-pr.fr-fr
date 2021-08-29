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
ms.openlocfilehash: 27f94dd5aca19d24742d553a65ce3c7f9164edf48cb1aab335d87d338f7e7499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958769"
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

## <a name="remarks"></a>Remarques

Les membres **StartSequenceQuery** et **StartSequenceConfigure** contiennent chacun un nombre aléatoire 32 bits sécurisé par chiffrement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Structures vidéo Direct3D](direct3d-video-structures.md)
</dt> <dt>

[**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




