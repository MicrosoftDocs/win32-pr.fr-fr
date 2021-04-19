---
description: Définit un attribut d’un compteur qui spécifie le mode d’affichage des données de compteur dans une application consommateur.
ms.assetid: 3749501b-4f3e-42e5-b1d5-2700b6d4a48a
title: Type complexe counterAttribute
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1b34a3a802f0f7c79815956c3a364522ce0962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525056"
---
# <a name="counterattribute-complex-type"></a><span data-ttu-id="e2ece-103">Type complexe counterAttribute</span><span class="sxs-lookup"><span data-stu-id="e2ece-103">counterAttribute Complex Type</span></span>

<span data-ttu-id="e2ece-104">Définit un attribut d’un compteur qui spécifie le mode d’affichage des données de compteur dans une application consommateur.</span><span class="sxs-lookup"><span data-stu-id="e2ece-104">Defines an attribute of a counter that specifies how the counter data is displayed in a consumer application.</span></span>

``` syntax
<xs:complexType name="counterAttribute">
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                use="required"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="xs:string"
                    >
                        <xs:enumeration
                            value="reference"
                         />
                        <xs:enumeration
                            value="noDisplay"
                         />
                        <xs:enumeration
                            value="noDigitGrouping"
                         />
                        <xs:enumeration
                            value="displayAsHex"
                         />
                        <xs:enumeration
                            value="displayAsReal"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="e2ece-105">Attributs</span><span class="sxs-lookup"><span data-stu-id="e2ece-105">Attributes</span></span>



| <span data-ttu-id="e2ece-106">Nom</span><span class="sxs-lookup"><span data-stu-id="e2ece-106">Name</span></span> | <span data-ttu-id="e2ece-107">Type</span><span class="sxs-lookup"><span data-stu-id="e2ece-107">Type</span></span> | <span data-ttu-id="e2ece-108">Description</span><span class="sxs-lookup"><span data-stu-id="e2ece-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ece-109">name</span><span class="sxs-lookup"><span data-stu-id="e2ece-109">name</span></span> |      | <span data-ttu-id="e2ece-110">Nom de l’attribut d’affichage à appliquer.</span><span class="sxs-lookup"><span data-stu-id="e2ece-110">The name of the display attribute to apply.</span></span> <span data-ttu-id="e2ece-111">Vous pouvez spécifier l’un des noms suivants :</span><span class="sxs-lookup"><span data-stu-id="e2ece-111">You can specify one of the following names:</span></span><br/> <dl> <span data-ttu-id="e2ece-112"><dt><span id="reference"></span><span id="REFERENCE"></span>reference</dt></span><span class="sxs-lookup"><span data-stu-id="e2ece-112"><dt><span id="reference"></span><span id="REFERENCE"></span>reference</dt></span></span> <dd> <span data-ttu-id="e2ece-113">Récupérez la valeur du compteur par référence et non par valeur.</span><span class="sxs-lookup"><span data-stu-id="e2ece-113">Retrieve the value of the counter by reference as opposed to by value.</span></span><br/> </dd> <span data-ttu-id="e2ece-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>nodisplay</dt></span><span class="sxs-lookup"><span data-stu-id="e2ece-114"><dt><span id="noDisplay"></span><span id="nodisplay"></span><span id="NODISPLAY"></span>noDisplay</dt></span></span> <dd> <span data-ttu-id="e2ece-115">N’affiche pas la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="e2ece-115">Do not display the counter value.</span></span> <span data-ttu-id="e2ece-116">En général, vous utilisez cet attribut si les données du compteur sont utilisées comme entrée pour calculer la valeur d’un autre compteur.</span><span class="sxs-lookup"><span data-stu-id="e2ece-116">Typically, you use this attribute if the counter's data is used as input for calculating another counter's value.</span></span> <br/> </dd> <span data-ttu-id="e2ece-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span><span class="sxs-lookup"><span data-stu-id="e2ece-117"><dt><span id="noDigitGrouping"></span><span id="nodigitgrouping"></span><span id="NODIGITGROUPING"></span>noDigitGrouping</dt></span></span> <dd> <span data-ttu-id="e2ece-118">Les applications de consommateur ou de surveillance ne doivent pas utiliser de séparateurs de chiffres lors de l’affichage des valeurs de compteur.</span><span class="sxs-lookup"><span data-stu-id="e2ece-118">Consumer or monitoring applications should not use digit separators when displaying counter values.</span></span> <br/> </dd> <span data-ttu-id="e2ece-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span><span class="sxs-lookup"><span data-stu-id="e2ece-119"><dt><span id="displayAsHex"></span><span id="displayashex"></span><span id="DISPLAYASHEX"></span>displayAsHex</dt></span></span> <dd> <span data-ttu-id="e2ece-120">Les applications de consommateur ou de surveillance doivent afficher la valeur de compteur en tant que valeur hexadécimale, au lieu de la valeur entière par défaut.</span><span class="sxs-lookup"><span data-stu-id="e2ece-120">Consumer or monitoring applications should display the counter value as a hexadecimal, instead of the default integer value.</span></span><br/> </dd> <span data-ttu-id="e2ece-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span><span class="sxs-lookup"><span data-stu-id="e2ece-121"><dt><span id="displayAsReal"></span><span id="displayasreal"></span><span id="DISPLAYASREAL"></span>displayAsReal</dt></span></span> <dd> <span data-ttu-id="e2ece-122">Les applications de consommateur ou de surveillance doivent afficher la valeur de compteur sous la forme d’un nombre réel, au lieu de la valeur entière par défaut.</span><span class="sxs-lookup"><span data-stu-id="e2ece-122">Consumer or monitoring applications should display the counter value as a real number, instead of the default integer value.</span></span> <br/> </dd> </dl> |



## <a name="requirements"></a><span data-ttu-id="e2ece-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2ece-123">Requirements</span></span>



| <span data-ttu-id="e2ece-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2ece-124">Requirement</span></span> | <span data-ttu-id="e2ece-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2ece-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e2ece-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2ece-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e2ece-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2ece-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e2ece-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2ece-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e2ece-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2ece-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




