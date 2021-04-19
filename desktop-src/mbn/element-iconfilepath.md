---
description: ICONFilePath
MS-HAID: WWAN\_profile\_v4.element\_ICONFilePath
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ICONFilePath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273f8a48cb099c95aaa0b54d438e06b3e1f0bb63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544653"
---
# <a name="span-idwwan_profile_v4element_iconfilepathspaniconfilepath"></a><span data-ttu-id="bcb42-103"><span id="WWAN_profile_v4.element_ICONFilePath"></span>ICONFilePath</span><span class="sxs-lookup"><span data-stu-id="bcb42-103"><span id="WWAN_profile_v4.element_ICONFilePath"></span>ICONFilePath</span></span>

<span data-ttu-id="bcb42-104">Chemin d’accès au fichier d’icône pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="bcb42-104">The path to the icon file for the connection.</span></span> <span data-ttu-id="bcb42-105">L’interface utilisateur de la connexion au système d’exploitation affiche l’icône lorsqu’une connexion est établie à l’aide de ce profil.</span><span class="sxs-lookup"><span data-stu-id="bcb42-105">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span>

<span data-ttu-id="bcb42-106">Pour plus d’informations sur l’utilisation de cet élément, consultez la documentation v1 pour [**ICONFilePath**](./schema-iconfilepath-mbnprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="bcb42-106">For more details on using this element, see the v1 documentation for [**ICONFilePath**](./schema-iconfilepath-mbnprofile-element.md).</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="bcb42-107">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="bcb42-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ICONFilePath>**

## <a name="syntax"></a><span data-ttu-id="bcb42-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcb42-108">Syntax</span></span>

``` syntax
<ICONFilePath>

  iconFileType

</ICONFilePath>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="bcb42-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="bcb42-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="bcb42-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="bcb42-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="bcb42-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="bcb42-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="bcb42-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bcb42-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="bcb42-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="bcb42-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="bcb42-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bcb42-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bcb42-115">Élément parent</span><span class="sxs-lookup"><span data-stu-id="bcb42-115">Parent Element</span></span></th>
<th><span data-ttu-id="bcb42-116">Description</span><span class="sxs-lookup"><span data-stu-id="bcb42-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bcb42-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="bcb42-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="bcb42-118">L’élément <strong>MBNProfileExt</strong> est une extension de l’élément MBNProfile précédent.</span><span class="sxs-lookup"><span data-stu-id="bcb42-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="bcb42-119">Il identifie un profil haut débit mobile avec un ensemble d’options plus riche que l’élément MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="bcb42-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="bcb42-120">Un profil peut contenir plusieurs éléments MbnProfileExt, décrivant des paramètres de profil pour un ensemble particulier de conditions de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="bcb42-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="bcb42-121">Utilisez l’élément enfant <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> pour spécifier les conditions de fonctionnement qui font d’un profil particulier le profil actif.</span><span class="sxs-lookup"><span data-stu-id="bcb42-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="bcb42-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcb42-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bcb42-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bcb42-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
