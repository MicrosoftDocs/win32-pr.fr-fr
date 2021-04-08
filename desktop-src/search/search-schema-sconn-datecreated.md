---
description: L' <dateCreated> élément facultatif identifie la date et l’heure de création de ce connecteur de recherche, à l’aide de la norme ISO 8601. Elle n’a pas d’éléments enfants ni d’attributs.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Élément dateCreated (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750341"
---
# <a name="datecreated-element-search-connector-schema"></a><span data-ttu-id="c4bbd-104">Élément dateCreated (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="c4bbd-104">dateCreated Element (Search Connector Schema)</span></span>

<span data-ttu-id="c4bbd-105">L' <dateCreated> élément facultatif identifie la date et l’heure de création de ce connecteur de recherche, à l’aide de la norme ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="c4bbd-105">The optional <dateCreated> element identifies the date and the time when this search connector was created, using the ISO 8601 standard.</span></span> <span data-ttu-id="c4bbd-106">Elle n’a pas d’éléments enfants ni d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c4bbd-106">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4bbd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4bbd-107">Syntax</span></span>


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="c4bbd-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c4bbd-108">Element Information</span></span>



| <span data-ttu-id="c4bbd-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="c4bbd-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="c4bbd-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c4bbd-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="c4bbd-111">Élément searchConnectorDescriptionType (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="c4bbd-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="c4bbd-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c4bbd-112">Remarks</span></span>

<span data-ttu-id="c4bbd-113">Le format de la valeur de cet élément suit la norme ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="c4bbd-113">The format of the value of this element follows the ISO 8601 standard.</span></span> <span data-ttu-id="c4bbd-114">Une utilisation courante est l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c4bbd-114">A common use would be either of the following:</span></span>

-   <span data-ttu-id="c4bbd-115">\[YYYY \] - \[ mm \] - \[ JJ \] T \[ hh \] : \[ mm \] : \[ SS \] ± \[ hh \] : \[ mm \] ("1981-04-05T14:30:30-05:00")</span><span class="sxs-lookup"><span data-stu-id="c4bbd-115">\[YYYY\]-\[MM\]-\[DD\]T\[hh\]:\[mm\]:\[ss\]±\[hh\]:\[mm\] ("1981-04-05T14:30:30-05:00")</span></span>
-   <span data-ttu-id="c4bbd-116">\[AAAA \] \[ mm \] \[ JJ \] T \[ hh \] \[ mm \] \[ SS \] Z (« 19810405T193030Z »)</span><span class="sxs-lookup"><span data-stu-id="c4bbd-116">\[YYYY\]\[MM\]\[DD\]T\[hh\]\[mm\]\[ss\]Z ("19810405T193030Z")</span></span>

## <a name="example"></a><span data-ttu-id="c4bbd-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="c4bbd-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



