---
description: 'Contient la réponse à un appel à la méthode IDirect3DAuthenticatedChannel9 :: configure.'
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317990"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a>D3DAUTHENTICATEDCHANNEL \_ configurer la \_ structure de sortie

Contient la réponse à un appel à la méthode [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
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

Handle vers le canal authentifié.

</dd> <dt>

**SequenceNumber**
</dt> <dd>

Numéro de séquence de la commande.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Code de résultat de la commande.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour **les membres** ConfigureType **, hChannel** et , le pilote utilise les mêmes valeurs que celles fournies par l’application dans [**D3DAUTHENTICATEDCHANNEL configurer la structure \_ \_ d’entrée**](d3dauthenticatedchannel-configure-input.md) . L’application doit vérifier que ces valeurs correspondent.

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

 

 




