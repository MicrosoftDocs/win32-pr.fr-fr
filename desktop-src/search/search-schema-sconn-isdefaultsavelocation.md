---
description: L’élément booléen facultatif <isDefaultSaveLocation> spécifie si l’emplacement décrit dans le connecteur de recherche doit être utilisé comme emplacement d’enregistrement par défaut. Cet élément n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Élément isDefaultSaveLocation (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b664e4cd6f7c88f1dfbeb44ba23faee5d24a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318141"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a><span data-ttu-id="7694a-104">Élément isDefaultSaveLocation (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="7694a-104">isDefaultSaveLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="7694a-105">L’élément booléen facultatif <isDefaultSaveLocation> spécifie si l’emplacement décrit dans le connecteur de recherche doit être utilisé comme emplacement d’enregistrement par défaut.</span><span class="sxs-lookup"><span data-stu-id="7694a-105">The optional Boolean <isDefaultSaveLocation> element specifies whether the location described in the search connector should be used as the default save location.</span></span> <span data-ttu-id="7694a-106">Cet élément n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="7694a-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7694a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7694a-107">Syntax</span></span>


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="7694a-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7694a-108">Element Information</span></span>



| <span data-ttu-id="7694a-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="7694a-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="7694a-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7694a-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="7694a-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="7694a-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="7694a-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7694a-112">Remarks</span></span>

<span data-ttu-id="7694a-113">Quand un utilisateur choisit d’enregistrer un élément, l’Explorateur Windows l’enregistre à l’emplacement spécifié dans l' <simpleLocation> élément.</span><span class="sxs-lookup"><span data-stu-id="7694a-113">When a user chooses to save an item, Windows Explorer saves the item to the location specified in the <simpleLocation> element.</span></span> <span data-ttu-id="7694a-114">Les utilisateurs peuvent modifier ce paramètre à l’aide de la boîte de dialogue Propriétés du connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="7694a-114">Users can change this setting using the Properties dialog for the search connector.</span></span>

## <a name="example"></a><span data-ttu-id="7694a-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="7694a-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



