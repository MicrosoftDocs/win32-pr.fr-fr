---
description: 'Contient des données d’entrée pour la méthode IDirect3DAuthenticatedChannel9 :: configure.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: de968c83fee7ae68dcd756bdf83d529593eeb30b3c2776b03cda812bcd442c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974738"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a>D3DAUTHENTICATEDCHANNEL \_ configurer la \_ structure d’entrée

Contient des données d’entrée pour la méthode [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**omac**
</dt> <dd>

Structure [**D3D \_ OMAC**](d3d-omac.md) qui contient un code d’Authentification de message (Mac) des données. Le pilote utilise l’algorithme CBC MAC (OMAC) basé sur AES pour calculer cette valeur pour le bloc de données qui s’affiche après ce membre de la structure.

</dd> <dt>

**ConfigureType**
</dt> <dd>

GUID qui spécifie la commande. Pour obtenir la liste des valeurs, consultez [protection du contenu des commandes](content-protection-commands.md).

</dd> <dt>

**hChannel**
</dt> <dd>

Handle vers le canal authentifié. Pour récupérer le handle, appelez [**IDirect3DDevice9Video :: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Numéro de séquence de la requête. Au début de la session, générez un nombre aléatoire 32 bits sécurisé par chiffrement à utiliser comme numéro de séquence de départ. Pour chaque commande, incrémentez le numéro de séquence de 1.

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

 

 




