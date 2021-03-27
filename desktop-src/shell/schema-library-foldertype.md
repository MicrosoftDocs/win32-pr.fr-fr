---
description: L' <folderType> élément spécifie un GUID pour le type de dossier. Cet élément est obligatoire si l' <templateInfo> élément existe ; sinon, il est facultatif. Cet élément n’a pas d’attributs ni d’éléments enfants.
title: Élément folderType (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972302"
---
# <a name="foldertype-element-library-schema"></a><span data-ttu-id="03cfa-105">Élément folderType (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-105">folderType Element (Library Schema)</span></span>

<span data-ttu-id="03cfa-106">L' <folderType> élément spécifie un GUID pour le type de dossier.</span><span class="sxs-lookup"><span data-stu-id="03cfa-106">The <folderType> element specifies a GUID for the folder type.</span></span> <span data-ttu-id="03cfa-107">Cet élément est obligatoire si l' <templateInfo> élément existe ; sinon, il est facultatif.</span><span class="sxs-lookup"><span data-stu-id="03cfa-107">This element is required if the <templateInfo> element exists, otherwise it is optional.</span></span> <span data-ttu-id="03cfa-108">Cet élément n’a pas d’attributs ni d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="03cfa-108">This element has no attributes and no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="03cfa-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03cfa-109">Syntax</span></span>


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="03cfa-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="03cfa-110">Element Information</span></span>



| <span data-ttu-id="03cfa-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="03cfa-111">Parent Element</span></span>                                                           | <span data-ttu-id="03cfa-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="03cfa-112">Child Elements</span></span> |
|--------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="03cfa-113">Élément templateInfo (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-113">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="03cfa-114">Notes</span><span class="sxs-lookup"><span data-stu-id="03cfa-114">Remarks</span></span>

<span data-ttu-id="03cfa-115">La définition d’un type de dossier détermine les colonnes et les détails qui s’affichent dans l’Explorateur Windows par défaut.</span><span class="sxs-lookup"><span data-stu-id="03cfa-115">Setting a folder type determines the columns and details that appear in Windows Explorer by default.</span></span> <span data-ttu-id="03cfa-116">Les identificateurs de type de dossier ([**FOLDERTYPEID**](foldertypeid.md)) sont des GUID définis dans shlguid. h.</span><span class="sxs-lookup"><span data-stu-id="03cfa-116">Folder type identifiers ([**FOLDERTYPEID**](foldertypeid.md)) are GUIDs defined in Shlguid.h.</span></span> <span data-ttu-id="03cfa-117">Le tableau suivant répertorie les GUID des types de dossiers courants.</span><span class="sxs-lookup"><span data-stu-id="03cfa-117">The following table lists the GUIDs of common folder types.</span></span>



| <span data-ttu-id="03cfa-118">Type de dossier</span><span class="sxs-lookup"><span data-stu-id="03cfa-118">Folder Type</span></span>      | <span data-ttu-id="03cfa-119">GUID</span><span class="sxs-lookup"><span data-stu-id="03cfa-119">GUID</span></span>                                   |
|------------------|----------------------------------------|
| <span data-ttu-id="03cfa-120">Bibliothèque générique</span><span class="sxs-lookup"><span data-stu-id="03cfa-120">Generic Library</span></span>  | <span data-ttu-id="03cfa-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span><span class="sxs-lookup"><span data-stu-id="03cfa-121">{5f4eab9a-6833-4f61-899d-31cf46979d49}</span></span> |
| <span data-ttu-id="03cfa-122">Bibliothèques d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="03cfa-122">Users Libraries</span></span>  | <span data-ttu-id="03cfa-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span><span class="sxs-lookup"><span data-stu-id="03cfa-123">{C4D98F09-6124-4fe0-9942-826416082DA9}</span></span> |
| <span data-ttu-id="03cfa-124">Dossier Documents</span><span class="sxs-lookup"><span data-stu-id="03cfa-124">Documents Folder</span></span> | <span data-ttu-id="03cfa-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span><span class="sxs-lookup"><span data-stu-id="03cfa-125">{7D49D726-3C21-4F05-99AA-FDC2C9474656}</span></span> |
| <span data-ttu-id="03cfa-126">Dossier images</span><span class="sxs-lookup"><span data-stu-id="03cfa-126">Pictures Folder</span></span>  | <span data-ttu-id="03cfa-127">{B3690E58-E961-423B-B687-386EBFD83239}</span><span class="sxs-lookup"><span data-stu-id="03cfa-127">{B3690E58-E961-423B-B687-386EBFD83239}</span></span> |
| <span data-ttu-id="03cfa-128">Dossier vidéos</span><span class="sxs-lookup"><span data-stu-id="03cfa-128">Videos Folder</span></span>    | <span data-ttu-id="03cfa-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span><span class="sxs-lookup"><span data-stu-id="03cfa-129">{5fa96407-7e77-483c-ac93-691d05850de8}</span></span> |
| <span data-ttu-id="03cfa-130">Dossier Games</span><span class="sxs-lookup"><span data-stu-id="03cfa-130">Games Folder</span></span>     | <span data-ttu-id="03cfa-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span><span class="sxs-lookup"><span data-stu-id="03cfa-131">{b689b0d0-76d3-4cbb-87f7-585d0e0ce070}</span></span> |
| <span data-ttu-id="03cfa-132">Dossier musique</span><span class="sxs-lookup"><span data-stu-id="03cfa-132">Music Folder</span></span>     | <span data-ttu-id="03cfa-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span><span class="sxs-lookup"><span data-stu-id="03cfa-133">{94d6ddcc-4a68-4175-a374-bd584a510b78}</span></span> |
| <span data-ttu-id="03cfa-134">Contacts</span><span class="sxs-lookup"><span data-stu-id="03cfa-134">Contacts</span></span>         | <span data-ttu-id="03cfa-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span><span class="sxs-lookup"><span data-stu-id="03cfa-135">{DE2B70EC-9BF7-4A93-BD3D-243F7881D492}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="03cfa-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="03cfa-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03cfa-137">Élément iconReference (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-137">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="03cfa-138">Élément isLibraryPinned (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-138">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="03cfa-139">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-139">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="03cfa-140">Élément Name (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-140">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="03cfa-141">Élément ownerSID (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-141">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="03cfa-142">Élément propertyStore (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="03cfa-143">Élément searchConnectorDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="03cfa-144">Élément searchConnectorDescriptionList (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="03cfa-145">Élément templateInfo (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="03cfa-146">version, élément (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="03cfa-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> </dl>

 

 



