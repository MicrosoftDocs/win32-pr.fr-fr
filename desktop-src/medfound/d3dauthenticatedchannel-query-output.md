---
description: 'Contient la réponse de la méthode IDirect3DAuthenticatedChannel9 :: Query.'
ms.assetid: b2783b8e-0436-419a-a93e-93dc1b87024d
title: Structure D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 79fe02a483ade1ff60107287799624017496887b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111819"
---
# <a name="d3dauthenticatedchannel_query_output-structure"></a>Structure de sortie de la \_ requête D3DAUTHENTICATEDCHANNEL \_

Contient la réponse de la méthode [**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT {
  D3D_OMAC       omac;
  GUID           QueryType;
  hChannel       HANDLE;
  SequenceNumber UINT;
  HRESULT        ReturnCode;
} D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT;
```



## <a name="members"></a>Membres

<dl> <dt>

**omac**
</dt> <dd>

Structure [**D3D \_ OMAC**](d3d-omac.md) qui contient un code d’Authentification de message (Mac) des données. Le pilote utilise l’algorithme CBC MAC (OMAC) basé sur AES pour calculer cette valeur pour le bloc de données qui s’affiche après ce membre de la structure.

</dd> <dt>

**Affectée**
</dt> <dd>

GUID qui spécifie la requête. Pour obtenir la liste des valeurs, consultez [protection du contenu des requêtes](content-protection-queries.md).

</dd> <dt>

**TRAITÉE**
</dt> <dd>

Handle vers le canal authentifié.

</dd> <dt>

**UINT**
</dt> <dd>

Numéro de séquence de la requête.

</dd> <dt>

**ReturnCode**
</dt> <dd>

Code de résultat de la requête.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour **les membres** **QueryType**, **hChannel** et de l’application, le pilote utilise les mêmes valeurs que celles fournies par l’application dans la structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) . L’application doit vérifier que ces valeurs correspondent.

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

[**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




