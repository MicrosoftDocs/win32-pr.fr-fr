---
title: Structure DRM_LICENSE_STATE_DATA (Drmexternals. h)
description: La \_ structure des \_ données d’état de licence DRM contient des informations de \_ licence sur un droit DRM spécifié.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- Structure DRM_LICENSE_STATE_DATA format Windows Media
- structure Windows Media format
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e6703481dc1d3608a8bf08ab2bbd216db4a9ecdc91bd4604d2b9de7d7de4fa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848532"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>Structure DRM_LICENSE_STATE_DATA (Drmexternals. h)

La structure des **données d’état de \_ licence \_ \_ DRM** contient des informations de [*licence*](wmformat-glossary.md) sur un droit [*DRM*](wmformat-glossary.md) spécifié.

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

Catégorie de chaîne à afficher. Consultez [**\_ catégorie d' \_ état \_ de licence DRM**](drm-license-state-category.md) pour connaître les valeurs possibles et leur signification.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Nombre d’éléments fournis dans **dwCount**. Cette valeur est généralement 0 ou 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Tableau de 0 ou 1 ou plusieurs **DWORD** s qui représentent le nombre de fois que l’action spécifiée dans **dwCategory** peut être exécutée. Consultez la section Remarques.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Nombre d’éléments fournis dans **DateTime**. En règle générale, il n’est pas possible d’utiliser plus de deux dates, par exemple avec une licence valide à partir d’une date jusqu’à une autre date.

</dd> <dt>

**DATEHEURE \[ 4\]**
</dt> <dd>

Tableau d’une ou de plusieurs structures FILETIME représentant une ou plusieurs dates dans la licence. La signification d’une date particulière dépend de la valeur de **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zéro, un ou plusieurs des indicateurs suivants combinés avec une **opération or** au niveau du bit :



| Indicateur                                    | Description                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| données d’état de la \_ licence DRM \_ \_ \_ vague        | Si cette valeur est définie, il peut y avoir plus de licences qui s’appliquent au contenu.                                                                                         |
| \_OPL de données d’état de licence DRM \_ \_ \_ \_ présent | Si cette option est définie, la licence comprend des niveaux de protection de sortie (OPLs) qui doivent être récupérés et vérifiés par rapport à la destination de la sortie de votre application. |
| données d’état de la \_ licence DRM \_ \_ \_ \_ présentes | S’il est défini, le contenu doit être remis à l’aide d’un chemin d’accès audio sécurisé (SAP).                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette structure est retournée (encapsulée dans une structure de [**\_ données d' \_ état \_ de licence WM**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) ) à partir d’un appel à [**IWMDRMReader :: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) lorsque vous spécifiez l’une des propriétés d’état de licence DRM. Ces propriétés sont :

-   [**\_Lecture DRM LicenseState \_**](drm-licensestate-playback.md)
-   [**\_LICENSESTATE DRM \_ CopyToCD**](drm-licensestate-copytocd.md)
-   [**\_LICENSESTATE DRM \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)
-   [**\_LICENSESTATE DRM \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)
-   [**\_LICENSESTATE DRM \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)
-   [**\_Copie DRM LicenseState \_**](drm-licensestate-copy.md)
-   [**\_LICENSESTATE DRM \_ PlaylistBurn**](drm-licensestate-playlistburn.md)

Si **dwCategory** est **le \_ \_ \_ nombre d’États de licence WM DRM \_ \_ de \_ until,** le tableau **DateTime** contient généralement deux dates, une date « from » et une date « until ». Il est également possible de spécifier deux paires de dates pour créer des licences plus complexes.

Les éléments du tableau **dwCount** correspondent aux dates ou aux plages de dates spécifiées dans le tableau **DateTime** . Si **dwCategory** est **le \_ \_ \_ nombre d’États de licence WM DRM \_ \_ de \_ until et que** **DateTime** contient une paire de dates, **dwCount** contient un élément. Si **DateTime** contient deux paires de dates (quatre éléments), **dwCount** doit contenir deux éléments, un pour chaque paire de dates.

Dans certains cas, les utilisateurs ont peut-être émis plus d’une licence pour un fichier. Par exemple, ils peuvent avoir acquis une licence qui a autorisé cinq lectures jusqu’à la fin du mois et acquis ultérieurement une deuxième licence pour des droits illimités. Dans ce cas, l’indicateur de \_ données de l' \_ État de licence DRM \_ \_ est défini dans **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) et le composant DRM utilise un algorithme pour déterminer l’ensemble de droits le plus probable qui ont été appliqués. Lorsqu’une licence expire, le composant DRM examine les licences restantes, et ainsi de suite jusqu’à ce que toutes les licences aient expiré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                      |
| Version<br/>                  | Windows Media Format 7 SDK ou les versions ultérieures du kit de développement logiciel (SDK)<br/>                       |
| En-tête<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

