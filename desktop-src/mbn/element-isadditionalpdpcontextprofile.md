---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318318"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile

L’élément **IsAdditionalPdpContextProfile** contient une valeur **booléenne** **true** s’il s’agit d’un profil « contexte PDP (Packet Data Protocol) » supplémentaire et **false**, dans le cas contraire. La valeur par défaut est **false**.

Un profil « contexte PDP supplémentaire » est un profil qui n’est pas activé sur le port par défaut de la carte physique, et l’affectation de la valeur true à cet élément garantit que ce profil ne s’affiche pas de manière inappropriée dans l’interface utilisateur.

Notez que si cet élément a la valeur true, les éléments suivants doivent également avoir la valeur true.

-   L’élément [**IsDefault**](./schema-isdefault-mbnprofile-element.md) ne doit pas être spécifié ou a la valeur **false** pour que le profil soit valide.
-   L’élément [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) doit être non spécifié ou défini sur **Manual** pour que le profil soit valide.

## <a name="element-hierarchy"></a>Hiérarchie d’éléments

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a>Syntaxe

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs

Aucun

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants

Aucun

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents

Cet élément (document) le plus à l’extérieur ne peut pas être contenu dans d’autres éléments.

## <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Espace de noms</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
