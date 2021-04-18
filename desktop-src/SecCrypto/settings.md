---
description: Utilisé pour configurer les composants CAPICOM.
title: Settings (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528883"
---
# <a name="settings-object-cryptography"></a><span data-ttu-id="24e87-103">Objet Settings (Cryptography)</span><span class="sxs-lookup"><span data-stu-id="24e87-103">Settings object (Cryptography)</span></span>

<span data-ttu-id="24e87-104">\[L’objet **Settings** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.\]</span><span class="sxs-lookup"><span data-stu-id="24e87-104">\[The **Settings** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="24e87-105">L’objet **Settings** est utilisé pour configurer les composants CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="24e87-105">The **Settings** object is used to configure CAPICOM components.</span></span>

## <a name="members"></a><span data-ttu-id="24e87-106">Membres</span><span class="sxs-lookup"><span data-stu-id="24e87-106">Members</span></span>

<span data-ttu-id="24e87-107">L’objet **Settings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="24e87-107">The **Settings** object has these types of members:</span></span>

-   [<span data-ttu-id="24e87-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="24e87-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24e87-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="24e87-109">Properties</span></span>

<span data-ttu-id="24e87-110">L’objet **Settings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="24e87-110">The **Settings** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="24e87-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="24e87-111">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="24e87-112">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="24e87-112">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="24e87-113">Description</span><span class="sxs-lookup"><span data-stu-id="24e87-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="24e87-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e87-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="24e87-115">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="24e87-115">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="24e87-116">Définit ou récupère le Active Directory emplacement de recherche.</span><span class="sxs-lookup"><span data-stu-id="24e87-116">Sets or retrieves the Active Directory search location.</span></span> <span data-ttu-id="24e87-117">L’emplacement initial n’est pas spécifié par défaut.</span><span class="sxs-lookup"><span data-stu-id="24e87-117">The initial location is unspecified by default.</span></span> <span data-ttu-id="24e87-118">Lorsque l’emplacement n’est pas spécifié, la recherche s’effectue dans le catalogue global, puis la recherche est effectuée dans le domaine par défaut.</span><span class="sxs-lookup"><span data-stu-id="24e87-118">When the location is unspecified, the global catalog is searched, then the default domain is searched.</span></span> <span data-ttu-id="24e87-119">La recherche détermine si l’attribut de certificat de l’utilisateur est publié à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="24e87-119">The search determines whether the user certificate attribute is published at that location.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="24e87-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="24e87-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="24e87-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="24e87-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="24e87-122">Définit ou récupère une valeur booléenne qui indique si les invites de l’interface utilisateur pour l’identité de l’expéditeur ou du signataire peuvent être utilisées.</span><span class="sxs-lookup"><span data-stu-id="24e87-122">Sets or retrieves a Boolean value that indicates whether user interface prompts for a signer or sender's identity can be used.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="24e87-123">La définition de cette propriété ne désactive pas les avertissements générés avant l’utilisation d’une clé privée à partir d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="24e87-123">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="24e87-124">Notes</span><span class="sxs-lookup"><span data-stu-id="24e87-124">Remarks</span></span>

<span data-ttu-id="24e87-125">L’objet **Settings** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="24e87-125">The **Settings** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="24e87-126">Le ProgID de l’objet **Settings** est CAPICOM. Paramètres. 1.</span><span class="sxs-lookup"><span data-stu-id="24e87-126">The ProgID for the **Settings** object is CAPICOM.Settings.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="24e87-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24e87-127">Requirements</span></span>



| <span data-ttu-id="24e87-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24e87-128">Requirement</span></span> | <span data-ttu-id="24e87-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="24e87-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24e87-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="24e87-130">Redistributable</span></span><br/> | <span data-ttu-id="24e87-131">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="24e87-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="24e87-132">DLL</span><span class="sxs-lookup"><span data-stu-id="24e87-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="24e87-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24e87-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24e87-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24e87-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e87-135">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="24e87-135">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 




