---
description: Contient les informations d’identification d’ouverture de session pour une connexion.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Élément UserLogonCred (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113447"
---
# <a name="userlogoncred-contexttype-element"></a><span data-ttu-id="2a1ab-103">Élément UserLogonCred (contextType)</span><span class="sxs-lookup"><span data-stu-id="2a1ab-103">UserLogonCred (contextType) Element</span></span>

<span data-ttu-id="2a1ab-104">L’élément **UserLogonCred (ContextType)** contient les informations d’identification d’ouverture de session pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="2a1ab-104">The **UserLogonCred (contextType)** element contains logon credentials for a connection.</span></span>

<span data-ttu-id="2a1ab-105">Cet élément peut avoir les éléments enfants suivants.</span><span class="sxs-lookup"><span data-stu-id="2a1ab-105">This element can have the following child elements.</span></span>

-   [<span data-ttu-id="2a1ab-106">**Nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-106">**UserName**</span></span>](schema-username-userlogoncred-element.md)
-   [<span data-ttu-id="2a1ab-107">**Mot de passe**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-107">**Password**</span></span>](schema-password-userlogoncred-element.md)
-   [<span data-ttu-id="2a1ab-108">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-108">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md)

<span data-ttu-id="2a1ab-109">Cet élément peut avoir au maximum une occurrence.</span><span class="sxs-lookup"><span data-stu-id="2a1ab-109">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="2a1ab-110">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="2a1ab-110">This element is optional.</span></span>

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="2a1ab-111">L’élément **UserLogonCred** est défini par le type complexe [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2a1ab-111">The **UserLogonCred** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2a1ab-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2a1ab-112">Child elements</span></span>



| <span data-ttu-id="2a1ab-113">Élément</span><span class="sxs-lookup"><span data-stu-id="2a1ab-113">Element</span></span>                                                               | <span data-ttu-id="2a1ab-114">Type</span><span class="sxs-lookup"><span data-stu-id="2a1ab-114">Type</span></span>                                           | <span data-ttu-id="2a1ab-115">Description</span><span class="sxs-lookup"><span data-stu-id="2a1ab-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="2a1ab-116">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-116">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="2a1ab-117">boolean</span><span class="sxs-lookup"><span data-stu-id="2a1ab-117">boolean</span></span>                                        | <span data-ttu-id="2a1ab-118">Comment gérer les mots de passe lors de la mise à niveau des profils.</span><span class="sxs-lookup"><span data-stu-id="2a1ab-118">How to handle passwords when upgrading profiles.</span></span><br/> |
| [<span data-ttu-id="2a1ab-119">**De**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-119">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="2a1ab-120">string</span><span class="sxs-lookup"><span data-stu-id="2a1ab-120">string</span></span>                                         | <span data-ttu-id="2a1ab-121">Mot de passe utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2a1ab-121">User password.</span></span><br/>                                   |
| [<span data-ttu-id="2a1ab-122">**Nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-122">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="2a1ab-123">**nameType**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-123">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="2a1ab-124">Nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2a1ab-124">User name.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="2a1ab-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a1ab-125">Requirements</span></span>



| <span data-ttu-id="2a1ab-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a1ab-126">Requirement</span></span> | <span data-ttu-id="2a1ab-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a1ab-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="2a1ab-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a1ab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2a1ab-129">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a1ab-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2a1ab-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a1ab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2a1ab-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a1ab-131">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="2a1ab-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a1ab-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a1ab-133">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2a1ab-134">**contextType**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-134">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="2a1ab-135">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2a1ab-136">**Contexte (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="2a1ab-136">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




