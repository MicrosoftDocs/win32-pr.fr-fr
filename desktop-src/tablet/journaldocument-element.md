---
description: Élément de niveau supérieur dans un fichier de note XML de journal.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Élément JournalDocument
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432171"
---
# <a name="journaldocument-element"></a><span data-ttu-id="2f4af-103">Élément JournalDocument</span><span class="sxs-lookup"><span data-stu-id="2f4af-103">JournalDocument Element</span></span>

<span data-ttu-id="2f4af-104">Élément de niveau supérieur dans un fichier de note XML de journal.</span><span class="sxs-lookup"><span data-stu-id="2f4af-104">The top-level element in a Journal note XML file.</span></span>

## <a name="definition"></a><span data-ttu-id="2f4af-105">Définition</span><span class="sxs-lookup"><span data-stu-id="2f4af-105">Definition</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="2f4af-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2f4af-106">Parent Elements</span></span>

<span data-ttu-id="2f4af-107">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2f4af-107">None.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2f4af-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2f4af-108">Child Elements</span></span>

[<span data-ttu-id="2f4af-109">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="2f4af-109">**Stationery**</span></span>](stationery-element.md)

[<span data-ttu-id="2f4af-110">**JournalPage**</span><span class="sxs-lookup"><span data-stu-id="2f4af-110">**JournalPage**</span></span>](journalpage-element.md)

## <a name="attributes"></a><span data-ttu-id="2f4af-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="2f4af-111">Attributes</span></span>



| <span data-ttu-id="2f4af-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="2f4af-112">Attribute</span></span>             | <span data-ttu-id="2f4af-113">Type</span><span class="sxs-lookup"><span data-stu-id="2f4af-113">Type</span></span>                      | <span data-ttu-id="2f4af-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2f4af-114">Required</span></span> | <span data-ttu-id="2f4af-115">Description</span><span class="sxs-lookup"><span data-stu-id="2f4af-115">Description</span></span>                                                      | <span data-ttu-id="2f4af-116">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="2f4af-116">Possible Values</span></span>           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="2f4af-117">**Version**</span><span class="sxs-lookup"><span data-stu-id="2f4af-117">**Version**</span></span>           | <span data-ttu-id="2f4af-118">**xs:string**</span><span class="sxs-lookup"><span data-stu-id="2f4af-118">**xs:string**</span></span>             | <span data-ttu-id="2f4af-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2f4af-119">Required</span></span> | <span data-ttu-id="2f4af-120">Version du document journal représenté dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="2f4af-120">The version of the Journal document represented in the XML file.</span></span> | <span data-ttu-id="2f4af-121">1.0</span><span class="sxs-lookup"><span data-stu-id="2f4af-121">1.0</span></span>                       |
| <span data-ttu-id="2f4af-122">**DefaultPageWidth**</span><span class="sxs-lookup"><span data-stu-id="2f4af-122">**DefaultPageWidth**</span></span>  | <span data-ttu-id="2f4af-123">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2f4af-123">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2f4af-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2f4af-124">Required</span></span> | <span data-ttu-id="2f4af-125">Largeur par défaut de la page pour le document journal.</span><span class="sxs-lookup"><span data-stu-id="2f4af-125">The default width of the page for the Journal document.</span></span>          | <span data-ttu-id="2f4af-126">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="2f4af-126">Any non-negative integer.</span></span> |
| <span data-ttu-id="2f4af-127">**DefaultPageHeight**</span><span class="sxs-lookup"><span data-stu-id="2f4af-127">**DefaultPageHeight**</span></span> | <span data-ttu-id="2f4af-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="2f4af-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="2f4af-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2f4af-129">Required</span></span> | <span data-ttu-id="2f4af-130">Hauteur par défaut de la page pour le document journal.</span><span class="sxs-lookup"><span data-stu-id="2f4af-130">The default height of the page for the Journal document.</span></span>         | <span data-ttu-id="2f4af-131">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="2f4af-131">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="2f4af-132">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="2f4af-132">Element Information</span></span>



|  <span data-ttu-id="2f4af-133">Élément</span><span class="sxs-lookup"><span data-stu-id="2f4af-133">Element</span></span>     | <span data-ttu-id="2f4af-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f4af-134">Value</span></span>                                                     |
|--------------|--------------------------------------------|
| <span data-ttu-id="2f4af-135">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="2f4af-135">Element type</span></span> | <span data-ttu-id="2f4af-136">**JournalDocument**</span><span class="sxs-lookup"><span data-stu-id="2f4af-136">**JournalDocument**</span></span>                        |
| <span data-ttu-id="2f4af-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2f4af-137">Namespace</span></span>    | <span data-ttu-id="2f4af-138">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="2f4af-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="2f4af-139">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="2f4af-139">Schema name</span></span>  | <span data-ttu-id="2f4af-140">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="2f4af-140">Journal Reader</span></span>                             |



 

 

 



