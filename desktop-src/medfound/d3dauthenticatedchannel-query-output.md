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
ms.openlocfilehash: 2defeaf134db9a2464854554db721586f592fc62110d172e0ac804e010804966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600829"
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

## <a name="remarks"></a>Remarques

Pour **les membres** **QueryType**, **hChannel** et de l’application, le pilote utilise les mêmes valeurs que celles fournies par l’application dans la structure [**\_ \_ d’entrée de requête D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-query-input.md) . L’application doit vérifier que ces valeurs correspondent.

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

[**IDirect3DAuthenticatedChannel9 :: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




