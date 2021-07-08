---
description: Identifie le type de requête.
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: Énumération D3DQUERYTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0778e879a6147c185964808ee4b4c302bd211ef3
ms.sourcegitcommit: bfab92e16614d4fa54b044917358261232bda81a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "113489693"
---
# <a name="d3dquerytype-enumeration"></a>Énumération D3DQUERYTYPE

Identifie le type de requête. Pour plus d’informations sur les requêtes, consultez [requêtes (Direct3D 9)](queries.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_RESOURCEMANAGER    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ Vcache**
</dt> <dd>

Recherchez des indications de pilote sur la disposition des données pour la mise en cache des vertex.

</dd> <dt>

<span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**
</dt> <dd>

Interrogez le gestionnaire des ressources. Pour cette requête, les indicateurs de comportement de l’appareil doivent inclure la [ \_ gestion des \_ pilotes \_ D3DCREATE Disable](d3dcreate.md).

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**
</dt> <dd>

Statistiques des vertex de la requête.

</dd> <dt>

<span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**\_Événement D3DQUERYTYPE**
</dt> <dd>

Recherchez tous les événements asynchrones émis à partir d’appels d’API et tous les événements asynchrones.

</dd> <dt>

<span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**\_Occlusion D3DQUERYTYPE**
</dt> <dd>

Une requête d’occlusion retourne le nombre de pixels qui passent le test z. Ces pixels sont destinés aux primitives dessinées entre le problème de [**D3DISSUE \_ Begin**](d3dissue-begin.md) et [**D3DISSUE \_ end**](d3dissue-end.md). Cela permet à une application de vérifier le résultat d’occlusion par rapport à 0. Zéro est entièrement bloqués, ce qui signifie que les pixels ne sont pas visibles à partir de la position actuelle de la caméra.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**\_Horodateur D3DQUERYTYPE**
</dt> <dd>

Retourne un horodateur 64 bits.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**
</dt> <dd>

Utilisez cette requête pour notifier une application si la fréquence du compteur est modifiée par rapport à l' \_ horodateur D3DQUERYTYPE.

</dd> <dt>

<span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**
</dt> <dd>

Ce résultat de requête est **true** si les valeurs des \_ requêtes d’horodatage D3DQUERYTYPE ne peuvent pas être garanties en continu pendant toute la durée de la \_ requête de TIMESTAMPDISJOINT D3DQUERYTYPE. Dans le cas contraire, le résultat de la requête est **false**.

</dd> <dt>

<span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**
</dt> <dd>

Pourcentage de temps de traitement des données de pipeline.

</dd> <dt>

<span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ INTERFACETIMINGS**
</dt> <dd>

Pourcentage de temps de traitement des données dans le pilote.

</dd> <dt>

<span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**
</dt> <dd>

Pourcentage de temps de traitement des données de nuanceur de vertex.

</dd> <dt>

<span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**
</dt> <dd>

Pourcentage de temps de traitement des données de nuanceur de pixels.

</dd> <dt>

<span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**
</dt> <dd>

Les comparaisons de mesure du débit pour vous aider à comprendre les performances d’une application.

</dd> <dt>

<span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**
</dt> <dd>

Mesurez les performances du taux d’accès au cache pour les textures et les vertex indexés.

</dd> <dt>

<span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**
</dt> <dd>

Efficacité de l’allocation de mémoire contenue dans une structure [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) .

Différences entre Direct3D 9 et Direct3D 9Ex :

- D3DQUERYTYPE \_ MEMORYPRESSURE est disponible uniquement dans Direct3D9Ex qui s’exécute sur Windows 7 (ou plus le système d’exploitation actuel).



 

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9 :: CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
