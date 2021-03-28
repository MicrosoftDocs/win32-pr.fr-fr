---
description: L' <name> élément spécifie le nom de cette bibliothèque. Cet élément est obligatoire et n’a pas d’attributs ni d’éléments enfants.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Élément Name (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991812"
---
# <a name="name-element-library-schema"></a><span data-ttu-id="4dd17-104">Élément Name (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="4dd17-104">name Element (Library Schema)</span></span>

<span data-ttu-id="4dd17-105">L' <name> élément spécifie le nom de cette bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4dd17-105">The <name> element specifies the name of this library.</span></span> <span data-ttu-id="4dd17-106">Cet élément est obligatoire et n’a pas d’attributs ni d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="4dd17-106">This element is required and has no attributes or child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd17-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4dd17-107">Syntax</span></span>

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a><span data-ttu-id="4dd17-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4dd17-108">Element Information</span></span>



| <span data-ttu-id="4dd17-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="4dd17-109">Parent Element</span></span>                                                               | <span data-ttu-id="4dd17-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4dd17-110">Child Elements</span></span> |
|------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="4dd17-111">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="4dd17-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="4dd17-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4dd17-112">Remarks</span></span>

<span data-ttu-id="4dd17-113">Le nom est le nom de bibliothèque convivial qui s’affiche dans l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="4dd17-113">The name is the friendly library name that is displayed in Windows Explorer.</span></span> <span data-ttu-id="4dd17-114">Le nom peut être spécifié au <dllname> format, <index> comme dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4dd17-114">The name can be specified in a <dllname>,<index> format, as in the following example.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="4dd17-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4dd17-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dd17-116">Élément libraryDescription (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="4dd17-116">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="4dd17-117">Schéma de la description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="4dd17-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
