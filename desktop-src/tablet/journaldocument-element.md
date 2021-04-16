---
description: Élément de niveau supérieur dans un fichier de note XML de journal.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Élément JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530171"
---
# <a name="journaldocument-element"></a><span data-ttu-id="17416-103">Élément JournalDocument</span><span class="sxs-lookup"><span data-stu-id="17416-103">JournalDocument Element</span></span>

<span data-ttu-id="17416-104">Élément de niveau supérieur dans un fichier de note XML de journal.</span><span class="sxs-lookup"><span data-stu-id="17416-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="17416-105">Définition</span><span class="sxs-lookup"><span data-stu-id="17416-105">Definition</span></span>

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a><span data-ttu-id="17416-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="17416-106">Parent Elements</span></span>

<span data-ttu-id="17416-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="17416-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="17416-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="17416-108">Child Elements</span></span>

[<span data-ttu-id="17416-109">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="17416-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="17416-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="17416-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="17416-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="17416-111">Attributes</span></span>



| <span data-ttu-id="17416-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="17416-112">Attribute</span></span>             | <span data-ttu-id="17416-113">Type</span><span class="sxs-lookup"><span data-stu-id="17416-113">Type</span></span>                      | <span data-ttu-id="17416-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="17416-114">Required</span></span> | <span data-ttu-id="17416-115">Description</span><span class="sxs-lookup"><span data-stu-id="17416-115">Description</span></span>                                                      | <span data-ttu-id="17416-116">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="17416-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="17416-117">**Version**</span><span class="sxs-lookup"><span data-stu-id="17416-117">**Version**</span></span>           | <span data-ttu-id="17416-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="17416-118">**xs:string**</span></span>             | <span data-ttu-id="17416-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="17416-119">Required</span></span> | <span data-ttu-id="17416-120">Version du document journal représenté dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="17416-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="17416-121">1.0</span><span class="sxs-lookup"><span data-stu-id="17416-121">1.0</span></span>                       |
| <span data-ttu-id="17416-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="17416-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="17416-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="17416-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="17416-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="17416-124">Required</span></span> | <span data-ttu-id="17416-125">Largeur par défaut de la page pour le document journal.</span><span class="sxs-lookup"><span data-stu-id="17416-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="17416-126">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="17416-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="17416-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="17416-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="17416-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="17416-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="17416-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="17416-129">Required</span></span> | <span data-ttu-id="17416-130">Hauteur par défaut de la page pour le document journal.</span><span class="sxs-lookup"><span data-stu-id="17416-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="17416-131">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="17416-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="17416-132">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="17416-132">Element Information</span></span>



|              |                                            |
|--------------|--------------------------------------------|
| <span data-ttu-id="17416-133">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="17416-133">Element type</span></span> | <span data-ttu-id="17416-134">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="17416-134">**JournalDocument**</span></span>                        |
| <span data-ttu-id="17416-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="17416-135">Namespace</span></span>    | <span data-ttu-id="17416-136">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="17416-136">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="17416-137">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="17416-137">Schema name</span></span>  | <span data-ttu-id="17416-138">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="17416-138">Journal Reader</span></span>                             |



 

 

 



