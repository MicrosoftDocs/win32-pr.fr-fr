---
title: Structure DRM_LICENSE_STATE_DATA (wmdrmsdk. h)
description: La \_ \_ \_ structure des données d’état de licence DRM contient des informations sur les restrictions de licence pour un droit DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- Structure DRM_LICENSE_STATE_DATA format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295206"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>Structure DRM_LICENSE_STATE_DATA (wmdrmsdk. h)

La structure des **\_ données d' \_ état \_ de licence DRM** contient des informations sur les restrictions de licence pour un droit DRM.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwStreamId**
</dt> <dd>

Numéro de flux auquel la licence s’applique. Doit avoir la valeur 0, ce qui indique que la licence s’applique à tous les flux du fichier.

</dd> <dt>

**dwCategory**
</dt> <dd>

Catégorie de chaîne à afficher. Consultez [**\_ catégorie d' \_ état \_ de licence DRM**](drmdrm-license-state-category.md) pour connaître les valeurs possibles et leur signification.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Nombre d’éléments fournis dans **dwCount**. Cette valeur est généralement 0 ou 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Tableau de 0 ou de 1 ou plusieurs valeurs **DWORD** qui représentent le nombre de fois que l’action spécifiée dans **dwCategory** peut être exécutée. Consultez la section Notes.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Nombre d’éléments fournis dans **DateTime**. En règle générale, il n’est pas possible d’utiliser plus de deux dates, par exemple avec une licence valide à partir d’une date jusqu’à une autre date.

</dd> <dt>

**DATEHEURE \[ 4\]**
</dt> <dd>

Tableau d’une ou de plusieurs structures **fileTime** représentant une ou plusieurs dates dans la licence. La signification d’une date particulière dépend de la valeur de **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zéro, un ou plusieurs des indicateurs suivants combinés avec une **opération or** au niveau du bit :



| Indicateur                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| données d’état de la \_ licence DRM \_ \_ \_ vague        | Si cette valeur est définie, il peut y avoir plus de licences qui s’appliquent au contenu. La seule façon d’être certain des licences individuelles qui s’appliquent à un ID de clé donné consiste à énumérer les licences. Pour ce faire, appelez [**IWMDRMLicenseManagement :: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), en passant l’ID de clé comme paramètre bstrKID. Utilisez ensuite l’interface IWMDRMLicense extraite pour examiner les licences. |
| \_OPL de données d’état de licence DRM \_ \_ \_ \_ présent | Si cette option est définie, la licence comprend des niveaux de protection de sortie (OPLs) qui doivent être récupérés et vérifiés par rapport à la destination de la sortie de votre application.                                                                                                                                                                                                                                                                                  |
| données d’état de la \_ licence DRM \_ \_ \_ \_ présentes | S’il est défini, le contenu doit être remis à l’aide d’un chemin d’accès audio sécurisé (SAP).                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est récupérée en appelant **IWMDRMLicenseQuery :: QueryLicenseState**.

Si **dwCategory** est **le \_ \_ \_ nombre d’États de licence WM DRM \_ \_ de \_ jusqu'** à, le tableau **DateTime** contient généralement deux dates : une date « de » et une date « jusqu’au ». Il est également possible de spécifier deux paires de dates pour créer des licences plus complexes.

Les éléments du tableau **dwCount** correspondent aux dates ou aux plages de dates spécifiées dans le tableau **DateTime** . Si **dwCategory** est **le \_ \_ \_ nombre d’États de licence WM DRM \_ \_ de \_ until et que** **DateTime** contient une paire de dates, **dwCount** contient un élément. Si **DateTime** contient deux paires de dates (quatre éléments), **dwCount** doit contenir deux éléments, un pour chaque paire de dates.

Dans certains cas, les utilisateurs ont peut-être émis plus d’une licence pour un fichier. Par exemple, ils peuvent avoir acquis une licence qui a autorisé cinq lectures jusqu’à la fin du mois et acquis ultérieurement une deuxième licence pour des droits illimités. Dans ce cas, l’indicateur de \_ données de l' \_ État de licence DRM \_ \_ est défini dans **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) et le composant DRM utilise un algorithme pour déterminer l’ensemble de droits le plus probable qui ont été appliqués. Lorsqu’une licence expire, le composant DRM examine les licences restantes, et ainsi de suite jusqu’à ce que toutes les licences aient expiré.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](drm-structures.md)
</dt> </dl>

 

 





