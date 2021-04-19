---
description: Spécifie le contexte connenction d’un appareil haut débit mobile.
ms.assetid: 513e744d-bd62-43e9-a636-6690867d8b9b
title: Type complexe contextType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- contextType
api_type:
- Schema
ms.openlocfilehash: 63d221c6bd388196abfb73a8ac38a26de516d0df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543657"
---
# <a name="contexttype-complex-type"></a><span data-ttu-id="36e6b-103">Type complexe contextType</span><span class="sxs-lookup"><span data-stu-id="36e6b-103">contextType Complex Type</span></span>

<span data-ttu-id="36e6b-104">Le type complexe **ContextType** spécifie le contexte connenction d’un appareil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="36e6b-104">The **contextType** complex type specifies the connenction context of a Mobile Broadband device.</span></span>

``` syntax
<xs:complexType name="contextType">
    <xs:sequence>
        <xs:element name="AccessString"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:minLength
                        value="1"
                     />
                    <xs:maxLength
                        value="100"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="UserLogonCred"
            minOccurs="0"
        >
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
        <xs:element name="Compression"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="DISABLE"
                     />
                    <xs:enumeration
                        value="ENABLE"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="AuthProtocol"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="token"
                >
                    <xs:enumeration
                        value="NONE"
                     />
                    <xs:enumeration
                        value="PAP"
                     />
                    <xs:enumeration
                        value="CHAP"
                     />
                    <xs:enumeration
                        value="MsCHAPv2"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="36e6b-105">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="36e6b-105">Child elements</span></span>



| <span data-ttu-id="36e6b-106">Élément</span><span class="sxs-lookup"><span data-stu-id="36e6b-106">Element</span></span>                                                               | <span data-ttu-id="36e6b-107">Type</span><span class="sxs-lookup"><span data-stu-id="36e6b-107">Type</span></span>                                           | <span data-ttu-id="36e6b-108">Description</span><span class="sxs-lookup"><span data-stu-id="36e6b-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36e6b-109">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="36e6b-109">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)       |                                                | <span data-ttu-id="36e6b-110">APN ou chaîne de numérotation à utiliser pour établir une connexion de données</span><span class="sxs-lookup"><span data-stu-id="36e6b-110">APN or dial string to be used to establish a data connection</span></span><br/>                        |
| [<span data-ttu-id="36e6b-111">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="36e6b-111">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)       |                                                | <span data-ttu-id="36e6b-112">Protocole d’authentification à utiliser pour l’activation d’un contexte PDP.</span><span class="sxs-lookup"><span data-stu-id="36e6b-112">Authentication protocol to be used for activating a PDP context.</span></span><br/>                    |
| [<span data-ttu-id="36e6b-113">**Compressé**</span><span class="sxs-lookup"><span data-stu-id="36e6b-113">**Compression**</span></span>](schema-compression-contexttype-element.md)         |                                                | <span data-ttu-id="36e6b-114">Spécifie si la compression sera utilisée au niveau de la liaison de données pour l’en-tête et le transfert de données</span><span class="sxs-lookup"><span data-stu-id="36e6b-114">Specifies if compression will be used at the data link for header and data transfer</span></span><br/> |
| [<span data-ttu-id="36e6b-115">**IgnorePassword**</span><span class="sxs-lookup"><span data-stu-id="36e6b-115">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="36e6b-116">boolean</span><span class="sxs-lookup"><span data-stu-id="36e6b-116">boolean</span></span>                                        | <span data-ttu-id="36e6b-117">Comment gérer les mots de passe lors de la mise à niveau des profils.</span><span class="sxs-lookup"><span data-stu-id="36e6b-117">How to handle passwords when upgrading profiles.</span></span><br/>                                    |
| [<span data-ttu-id="36e6b-118">**De**</span><span class="sxs-lookup"><span data-stu-id="36e6b-118">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="36e6b-119">string</span><span class="sxs-lookup"><span data-stu-id="36e6b-119">string</span></span>                                         | <span data-ttu-id="36e6b-120">Mot de passe utilisé pour authentifier un utilisateur</span><span class="sxs-lookup"><span data-stu-id="36e6b-120">Password used to authenticate a user</span></span><br/>                                                |
| [<span data-ttu-id="36e6b-121">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="36e6b-121">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)     |                                                | <span data-ttu-id="36e6b-122">Informations d’identification d’ouverture de session pour une connexion.</span><span class="sxs-lookup"><span data-stu-id="36e6b-122">Log on credentials for a connection.</span></span><br/>                                                |
| [<span data-ttu-id="36e6b-123">**Nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="36e6b-123">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="36e6b-124">**nameType**</span><span class="sxs-lookup"><span data-stu-id="36e6b-124">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="36e6b-125">Nom d’utilisateur pour l’ouverture de session</span><span class="sxs-lookup"><span data-stu-id="36e6b-125">User name for logon</span></span><br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="36e6b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36e6b-126">Requirements</span></span>



| <span data-ttu-id="36e6b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36e6b-127">Requirement</span></span> | <span data-ttu-id="36e6b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="36e6b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="36e6b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36e6b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="36e6b-130">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="36e6b-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="36e6b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36e6b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="36e6b-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="36e6b-132">None supported</span></span><br/>                         |



 

 




