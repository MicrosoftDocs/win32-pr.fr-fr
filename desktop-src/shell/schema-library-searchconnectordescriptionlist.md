---
description: Cet <searchConnectorDescriptionList> élément contient une liste de connecteurs de recherche qui correspondent aux emplacements inclus dans cette bibliothèque. Chaque connecteur de recherche est défini par un <searchConnectorDescription> élément. Cet élément est facultatif et n’a pas d’attributs.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: Élément searchConnectorDescriptionList (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973603"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a><span data-ttu-id="4da78-105">Élément searchConnectorDescriptionList (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="4da78-105">searchConnectorDescriptionList Element (Library Schema)</span></span>

<span data-ttu-id="4da78-106">Cet <searchConnectorDescriptionList> élément contient une liste de connecteurs de recherche qui correspondent aux emplacements inclus dans cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4da78-106">This <searchConnectorDescriptionList> element contains a list of search connectors that map to locations included in this library.</span></span> <span data-ttu-id="4da78-107">Chaque connecteur de recherche est défini par un <searchConnectorDescription> élément.</span><span class="sxs-lookup"><span data-stu-id="4da78-107">Each search connector is defined by a <searchConnectorDescription> element.</span></span> <span data-ttu-id="4da78-108">Cet élément est facultatif et n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="4da78-108">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4da78-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4da78-109">Syntax</span></span>

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a><span data-ttu-id="4da78-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4da78-110">Element Information</span></span>



| <span data-ttu-id="4da78-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="4da78-111">Parent Element</span></span>                                                               | <span data-ttu-id="4da78-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4da78-112">Child Elements</span></span>                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4da78-113">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="4da78-113">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="4da78-114">Élément searchConnectorDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="4da78-114">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a><span data-ttu-id="4da78-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4da78-115">Remarks</span></span>

<span data-ttu-id="4da78-116">Les connecteurs de recherche pour les étendues de recherche fédérée de Windows et de gestionnaire de protocole ne peuvent pas être inclus dans une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4da78-116">Search connectors for Windows Federated Search and protocol handler scopes cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4da78-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4da78-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4da78-118">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4da78-118">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

<span data-ttu-id="4da78-119">[Schéma de la description du connecteur de recherche](/previous-versions//dd743009(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4da78-119">[Search Connector Description Schema](/previous-versions//dd743009(v=vs.85))</span></span>
</dt> </dl>

 

 
