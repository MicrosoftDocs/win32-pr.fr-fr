---
description: Les méthodes utilisées pour travailler avec des fichiers DirectX. x peuvent retourner les valeurs suivantes en plus des valeurs de retour COM standard.
ms.assetid: b1d04fab-25cb-431d-942e-74092bc9c5c2
title: D3DXFERR les valeurs de retour (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFERR
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: b6e106fc7163ed4ff66e74332336cc85b2a95afdc0fa6b712b00f3b32e2af248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096064"
---
# <a name="d3dxferr-return-values"></a>D3DXFERR les valeurs de retour

Les méthodes utilisées pour travailler avec des fichiers DirectX. x peuvent retourner les valeurs suivantes en plus des valeurs de retour COM standard.

<dl> <dt>

<span id="D3DXFERR_BADARRAYSIZE"></span><span id="d3dxferr_badarraysize"></span>**D3DXFERR \_ BADARRAYSIZE**
</dt> <dd>

Un tableau dépasse la taille autorisée.

</dd> <dt>

<span id="D3DXFERR_BADCACHEFILE"></span><span id="d3dxferr_badcachefile"></span>**D3DXFERR \_ BADCACHEFILE**
</dt> <dd>

Impossible de lire un fichier cache.

</dd> <dt>

<span id="D3DXFERR_BADDataReference"></span><span id="d3dxferr_baddatareference"></span><span id="D3DXFERR_BADDATAREFERENCE"></span>**D3DXFERR \_ BADDataReference**
</dt> <dd>

Impossible de récupérer les données du membre du modèle.

</dd> <dt>

<span id="D3DXFERR_BADFILE"></span><span id="d3dxferr_badfile"></span>**D3DXFERR \_ BadFile**
</dt> <dd>

Échec d’une opération de lecture ou d’écriture de fichier.

</dd> <dt>

<span id="D3DXFERR_BADFILEFLOATSIZE"></span><span id="d3dxferr_badfilefloatsize"></span>**D3DXFERR \_ BADFILEFLOATSIZE**
</dt> <dd>

La taille du fichier n’est pas la taille attendue.

</dd> <dt>

<span id="D3DXFERR_BADFILETYPE"></span><span id="d3dxferr_badfiletype"></span>**D3DXFERR \_ BADFILETYPE**
</dt> <dd>

Le format du fichier n’est pas valide.

</dd> <dt>

<span id="D3DXFERR_BADFILEVERSION"></span><span id="d3dxferr_badfileversion"></span>**D3DXFERR \_ BADFILEVERSION**
</dt> <dd>

Le fichier a une version de format non valide.

</dd> <dt>

<span id="D3DXFERR_BADOBJECT"></span><span id="d3dxferr_badobject"></span>**D3DXFERR \_ BADOBJECT**
</dt> <dd>

Les données n’ont pas pu être lues ou écrites dans un objet.

</dd> <dt>

<span id="D3DXFERR_BADRESOURCE"></span><span id="d3dxferr_badresource"></span>**D3DXFERR \_ BADRESOURCE**
</dt> <dd>

Une opération sur une ressource a échoué.

</dd> <dt>

<span id="D3DXFERR_BADTYPE"></span><span id="d3dxferr_badtype"></span>**D3DXFERR \_ BADTYPE**
</dt> <dd>

Le fichier ne correspond pas aux types de modèles connus.

</dd> <dt>

<span id="D3DXFERR_BADVALUE"></span><span id="d3dxferr_badvalue"></span>**D3DXFERR \_ BADVALUE**
</dt> <dd>

Une variable est en dehors de la plage attendue. généralement retourné lorsqu’un pointeur d’objet n’est pas valide.

</dd> <dt>

<span id="D3DXFERR_FILENOTFOUND"></span><span id="d3dxferr_filenotfound"></span>**D3DXFERR \_ FILENOTFOUND**
</dt> <dd>

Aucun handle valide n’a été trouvé pour le fichier spécifié.

</dd> <dt>

<span id="D3DXFERR_NOMOREDATA"></span><span id="d3dxferr_nomoredata"></span>**D3DXFERR \_ NOMOREDATA**
</dt> <dd>

Décalage du pointeur étendu au-delà de la fin de la mémoire tampon.

</dd> <dt>

<span id="D3DXFERR_NOMOREOBJECTS"></span><span id="d3dxferr_nomoreobjects"></span>**D3DXFERR \_ NOMOREOBJECTS**
</dt> <dd>

Aucun autre objet enfant n’est disponible.

</dd> <dt>

<span id="D3DXFERR_NOTDONEYET"></span><span id="d3dxferr_notdoneyet"></span>**D3DXFERR \_ NOTDONEYET**
</dt> <dd>

Le type de données ne correspond pas aux types autorisés.

</dd> <dt>

<span id="D3DXFERR_NOTFOUND"></span><span id="d3dxferr_notfound"></span>**D3DXFERR \_ NotFound**
</dt> <dd>

L’objet est introuvable à partir des paramètres spécifiés.

</dd> <dt>

<span id="D3DXFERR_PARSEERROR"></span><span id="d3dxferr_parseerror"></span>**D3DXFERR \_ PARSEERROR**
</dt> <dd>

Impossible d’analyser le flux de données.

</dd> <dt>

<span id="D3DXFERR_RESOURCENOTFOUND"></span><span id="d3dxferr_resourcenotfound"></span>**D3DXFERR \_ RESOURCENOTFOUND**
</dt> <dd>

Un handle valide est introuvable pour la ressource spécifiée.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le code d’erreur de fichier. x \_ FACD3DXF est utilisé pour générer des codes d’erreur. Par exemple :


```
#define _FACD3DXF           0x876
#define D3DXFERR_BADOBJECT  MAKE_HRESULT( 1, _FACD3DXF, 900 )
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9xof. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de fichier D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> </dl>

 

 




