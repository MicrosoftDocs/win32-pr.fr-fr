---
description: ModemDMConfigProfile \/ ... \/ UserLogonCred (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_UserLogonCred
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserLogonCred (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d563cf8-ea40-46b3-a74e-ec7640ca9824
api_name:
- UserLogonCred
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aea2cdfda61e557ff790b59e7af2a05d914d3403
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106543396"
---
# <a name="span-idwwan_profile_v4element_1_userlogoncredspanmodemdmconfigprofileuserlogoncred-v4"></a><span data-ttu-id="be2c7-103"><span id="WWAN_profile_v4.element_1_UserLogonCred"></span>ModemDMConfigProfile \/ ... \/ UserLogonCred (v4)</span><span class="sxs-lookup"><span data-stu-id="be2c7-103"><span id="WWAN_profile_v4.element_1_UserLogonCred"></span>ModemDMConfigProfile\/...\/UserLogonCred (v4)</span></span>

<span data-ttu-id="be2c7-104">Informations d’identification d’ouverture de session pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="be2c7-104">Logon credentials for a connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="be2c7-105">Hiérarchie d’éléments</span><span class="sxs-lookup"><span data-stu-id="be2c7-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserLogonCred\>**

## <a name="syntax"></a><span data-ttu-id="be2c7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be2c7-106">Syntax</span></span>

``` syntax
<UserLogonCred>

  <!-- Child elements -->
  UserName,
  IgnorePassword?,
  Password?

</UserLogonCred>
```

### <a name="key"></a><span data-ttu-id="be2c7-107">Clé</span><span class="sxs-lookup"><span data-stu-id="be2c7-107">Key</span></span>

<span data-ttu-id="be2c7-108">`?`   facultatif (zéro ou un)</span><span class="sxs-lookup"><span data-stu-id="be2c7-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="be2c7-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributs et éléments</span><span class="sxs-lookup"><span data-stu-id="be2c7-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="be2c7-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="be2c7-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="be2c7-111">Aucun</span><span class="sxs-lookup"><span data-stu-id="be2c7-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="be2c7-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="be2c7-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be2c7-113">Élément enfant</span><span class="sxs-lookup"><span data-stu-id="be2c7-113">Child Element</span></span></th>
<th><span data-ttu-id="be2c7-114">Description</span><span class="sxs-lookup"><span data-stu-id="be2c7-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="be2c7-115"><a href="element-1-ignorepassword.md">IgnorePassword</a></span><span class="sxs-lookup"><span data-stu-id="be2c7-115"><a href="element-1-ignorepassword.md">IgnorePassword</a></span></span></td>
<td><p><span data-ttu-id="be2c7-116">Spécifie la manière dont les mots de passe sont gérés lors de la mise à niveau des profils.</span><span class="sxs-lookup"><span data-stu-id="be2c7-116">Specifies how passwords are handled when upgrading profiles.</span></span></p>
<p><span data-ttu-id="be2c7-117">Si la valeur est <strong>true</strong> et qu’un profil portant le même nom existe au moment de l’opération de mise à jour, le mot de passe de ce profil est pris et stocké dans le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="be2c7-117">If set to <strong>TRUE</strong> and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span></p>
<p><span data-ttu-id="be2c7-118">Pour plus d’informations, consultez la documentation de l’élément <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="be2c7-118">For more details, see the documentation for the v1 <a href="../mbn/schema-ignorepassword-userlogoncred-element.md"><strong>IgnorePassword</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be2c7-119"><a href="element-1-password.md">Mot de passe</a></span><span class="sxs-lookup"><span data-stu-id="be2c7-119"><a href="element-1-password.md">Password</a></span></span></td>
<td><p><span data-ttu-id="be2c7-120">Spécifie le mot de passe utilisé pour authentifier un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be2c7-120">Specifies the password used to authenticate a user.</span></span></p>
<p><span data-ttu-id="be2c7-121">Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-password-userlogoncred-element.md"><strong>mot de passe</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="be2c7-121">For more information, see the documentation for the v1 <a href="../mbn/schema-password-userlogoncred-element.md"><strong>Password</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be2c7-122"><a href="element-1-username.md">UserName</a></span><span class="sxs-lookup"><span data-stu-id="be2c7-122"><a href="element-1-username.md">UserName</a></span></span></td>
<td><p><span data-ttu-id="be2c7-123">Nom d’utilisateur à utiliser pour l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="be2c7-123">The user name to use for logon.</span></span></p>
<p><span data-ttu-id="be2c7-124">Pour plus d’informations, consultez la documentation de l’élément de <a href="../mbn/schema-username-userlogoncred-element.md"><strong>nom d’utilisateur</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="be2c7-124">For more details, see the documentation for the v1 <a href="../mbn/schema-username-userlogoncred-element.md"><strong>UserName</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="be2c7-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Éléments parents</span><span class="sxs-lookup"><span data-stu-id="be2c7-125"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="be2c7-126">Élément parent</span><span class="sxs-lookup"><span data-stu-id="be2c7-126">Parent Element</span></span></th>
<th><span data-ttu-id="be2c7-127">Description</span><span class="sxs-lookup"><span data-stu-id="be2c7-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="be2c7-128"><a href="element-1-context.md">Contexte</a></span><span class="sxs-lookup"><span data-stu-id="be2c7-128"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="be2c7-129">Spécifie les paramètres requis pour établir une connexion de données.</span><span class="sxs-lookup"><span data-stu-id="be2c7-129">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="be2c7-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be2c7-130">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be2c7-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="be2c7-131">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



