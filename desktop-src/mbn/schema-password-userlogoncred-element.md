---
description: Spécifie le mot de passe utilisé pour authentifier un utilisateur.
ms.assetid: 9c02413b-a4c7-4c1f-a150-e27cc125faf6
title: Élément Password (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Password
api_type:
- Schema
ms.openlocfilehash: b05e34bcbaa91aba5cbfbd14f2bc8534aa91dd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515647"
---
# <a name="password-userlogoncred-element"></a><span data-ttu-id="c073e-103">Élément Password (UserLogonCred)</span><span class="sxs-lookup"><span data-stu-id="c073e-103">Password (UserLogonCred) Element</span></span>

<span data-ttu-id="c073e-104">L’élément [**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) spécifie le mot de passe utilisé pour authentifier un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c073e-104">The [**Password (UserLogonCred)**](schema-ignorepassword-userlogoncred-element.md) element specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="c073e-105">L’élément est une chaîne allant jusqu’à 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="c073e-105">The element is a string of up to 255 characters.</span></span>

<span data-ttu-id="c073e-106">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c073e-106">This element is optional.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="c073e-107">L’élément **Password** est défini par l’élément [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c073e-107">The **Password** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c073e-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c073e-108">Requirements</span></span>



| <span data-ttu-id="c073e-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c073e-109">Requirement</span></span> | <span data-ttu-id="c073e-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c073e-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="c073e-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c073e-111">Minimum supported client</span></span><br/> | <span data-ttu-id="c073e-112">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c073e-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c073e-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c073e-113">Minimum supported server</span></span><br/> | <span data-ttu-id="c073e-114">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c073e-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c073e-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c073e-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="c073e-116">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="c073e-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c073e-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="c073e-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="c073e-118">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="c073e-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c073e-119">**UserLogonCred (contextType)**</span><span class="sxs-lookup"><span data-stu-id="c073e-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




