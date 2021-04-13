---
description: MBNProfileExt \/ ... \/ Nom d’utilisateur (v4)
MS-HAID: WWAN\_profile\_v4.element\_UserName
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserName
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1f06d5b0-f229-4db7-a06b-9b66a8d792c1
api_name:
- UserName
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4c901a78e37bd3a4d883e0bd1c5c2006c7e2bc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526032"
---
# <a name="span-idwwan_profile_v4element_usernamespanmbnprofileextusername-v4"></a><span data-ttu-id="0ec57-103"><span id="WWAN_profile_v4.element_UserName"></span>MBNProfileExt \/ ... \/ Nom d’utilisateur (v4)</span><span class="sxs-lookup"><span data-stu-id="0ec57-103"><span id="WWAN_profile_v4.element_UserName"></span>MBNProfileExt\/...\/UserName (v4)</span></span>

<span data-ttu-id="0ec57-104">Nom d’utilisateur à utiliser pour l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="0ec57-104">The user name to use for logon.</span></span>

<span data-ttu-id="0ec57-105">Pour plus d’informations, consultez la documentation de l’élément de [**nom d’utilisateur**](./schema-username-userlogoncred-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="0ec57-105">For more details, see the documentation for the v1 [**UserName**](./schema-username-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="0ec57-106">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="0ec57-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserName\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserName\>**

## <a name="syntax"></a><span data-ttu-id="0ec57-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ec57-107">Syntax</span></span>

``` syntax
<UserName>

  nameType

</UserName>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="0ec57-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="0ec57-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="0ec57-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="0ec57-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="0ec57-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="0ec57-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="0ec57-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0ec57-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="0ec57-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="0ec57-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="0ec57-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0ec57-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ec57-114">Élément parent</span><span class="sxs-lookup"><span data-stu-id="0ec57-114">Parent Element</span></span></th>
<th><span data-ttu-id="0ec57-115">Description</span><span class="sxs-lookup"><span data-stu-id="0ec57-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0ec57-116"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="0ec57-116"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="0ec57-117">Informations d’identification d’ouverture de session pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="0ec57-117">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="0ec57-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ec57-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ec57-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0ec57-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
