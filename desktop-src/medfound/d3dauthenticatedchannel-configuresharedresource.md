---
description: Contient des données d’entrée pour une \_ commande D3DAUTHENTICATEDCONFIGURE SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 0dbff67921f2ec6ad634c20b11b86b0384923db5548bcef113128fe5ede6bdd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742905"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a>D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE, structure

Contient des données d’entrée pour une commande [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .

Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Paramètres**
</dt> <dd>

Un [**D3DAUTHENTICATEDCHANNEL \_ configure une structure \_ d’entrée**](d3dauthenticatedchannel-configure-input.md) qui contient le GUID de la commande et d’autres données.

</dd> <dt>

**ProcessIdentiferType**
</dt> <dd>

Valeur [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) qui spécifie le type de processus. Pour spécifier le processus de Gestionnaire de fenêtrage (DWM), affectez la valeur **PROCESSIDTYPE \_ DWM** à ce membre. Sinon, définissez ce membre sur **\_ handle PROCESSIDTYPE** et définissez le membre **ProcessHandle** sur un handle valide.

</dd> <dt>

**ProcessHandle**
</dt> <dd>

Handle de processus. Si le membre **ProcessIdentifier** est égal **au \_ descripteur PROCESSTIDTYPE**, le membre **ProcessHandle** spécifie un handle vers un processus. Dans le cas contraire, la valeur est ignorée.

</dd> <dt>

**AllowAccess**
</dt> <dd>

Si la **valeur est true**, le processus spécifié a accès aux ressources partagées restreintes.

</dd> </dl>

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

 

 




