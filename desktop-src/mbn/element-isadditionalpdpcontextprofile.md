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
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span data-ttu-id="f7687-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span><span class="sxs-lookup"><span data-stu-id="f7687-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span></span>

<span data-ttu-id="f7687-104">L’élément **IsAdditionalPdpContextProfile** contient une valeur **booléenne** **true** s’il s’agit d’un profil « contexte PDP (Packet Data Protocol) » supplémentaire et **false**, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f7687-104">The **IsAdditionalPdpContextProfile** element contains a **boolean** that is **true** if this is an "additional PDP (Packet Data Protocol) context" profile and **false**, otherwise.</span></span> <span data-ttu-id="f7687-105">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="f7687-105">Default is **false**.</span></span>

<span data-ttu-id="f7687-106">Un profil « contexte PDP supplémentaire » est un profil qui n’est pas activé sur le port par défaut de la carte physique, et l’affectation de la valeur true à cet élément garantit que ce profil ne s’affiche pas de manière inappropriée dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f7687-106">An "additional PDP context" profile is a profile that does not get activated over the physical adapter default port, and setting this element to true ensures that this profile is not displayed inappropriately in the user interface.</span></span>

<span data-ttu-id="f7687-107">Notez que si cet élément a la valeur true, les éléments suivants doivent également avoir la valeur true.</span><span class="sxs-lookup"><span data-stu-id="f7687-107">Note that if this element is set to true, then the following must also be true.</span></span>

-   <span data-ttu-id="f7687-108">L’élément [**IsDefault**](./schema-isdefault-mbnprofile-element.md) ne doit pas être spécifié ou a la valeur **false** pour que le profil soit valide.</span><span class="sxs-lookup"><span data-stu-id="f7687-108">The [**IsDefault**](./schema-isdefault-mbnprofile-element.md) element must be unspecified or set to **false** for the profile to be valid.</span></span>
-   <span data-ttu-id="f7687-109">L’élément [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) doit être non spécifié ou défini sur **Manual** pour que le profil soit valide.</span><span class="sxs-lookup"><span data-stu-id="f7687-109">The [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) element must be unspecified or set to **manual** for the profile to be valid.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="f7687-110">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="f7687-110">Element hierarchy</span></span>

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a><span data-ttu-id="f7687-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7687-111">Syntax</span></span>

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="f7687-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="f7687-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="f7687-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="f7687-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="f7687-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="f7687-114">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="f7687-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f7687-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="f7687-116">Aucun</span><span class="sxs-lookup"><span data-stu-id="f7687-116">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="f7687-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f7687-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="f7687-118">Cet élément (document) le plus à l’extérieur ne peut pas être contenu dans d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="f7687-118">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7687-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7687-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7687-120">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f7687-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
