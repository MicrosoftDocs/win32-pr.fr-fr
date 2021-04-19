---
description: Indique comment gérer les mots de passe lors de la mise à niveau des profils.
ms.assetid: 74d7ceb1-d778-4a12-907b-0528d9ff45be
title: Élément IgnorePassword (UserLogonCred)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IgnorePassword
api_type:
- Schema
ms.openlocfilehash: 40211a8f848d8d0551ed39297178bc985d9efba4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544686"
---
# <a name="ignorepassword-userlogoncred-element"></a><span data-ttu-id="4b56f-103">Élément IgnorePassword (UserLogonCred)</span><span class="sxs-lookup"><span data-stu-id="4b56f-103">IgnorePassword (UserLogonCred) Element</span></span>

<span data-ttu-id="4b56f-104">L’élément **IgnorePassword (UserLogonCred)** indique comment gérer les mots de passe lors de la mise à niveau des profils.</span><span class="sxs-lookup"><span data-stu-id="4b56f-104">The **IgnorePassword (UserLogonCred)** element specifies how to handle passwords when upgrading profiles.</span></span>

<span data-ttu-id="4b56f-105">Si la valeur est **true** et qu’un profil portant le même nom existe au moment de l’opération de mise à jour, le mot de passe de ce profil est pris et stocké dans le nouveau profil.</span><span class="sxs-lookup"><span data-stu-id="4b56f-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in new profile.</span></span>

<span data-ttu-id="4b56f-106">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="4b56f-106">This element is optional.</span></span>

``` syntax
<xs:element name="IgnorePassword"
    type="boolean"
 />
```

<span data-ttu-id="4b56f-107">L’élément **IgnorePassword** est défini par l’élément [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4b56f-107">The **IgnorePassword** element is defined by the [**UserLogonCred**](schema-userlogoncred-contexttype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b56f-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b56f-108">Requirements</span></span>



| <span data-ttu-id="4b56f-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b56f-109">Requirement</span></span> | <span data-ttu-id="4b56f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b56f-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="4b56f-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b56f-111">Minimum supported client</span></span><br/> | <span data-ttu-id="4b56f-112">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4b56f-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="4b56f-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b56f-113">Minimum supported server</span></span><br/> | <span data-ttu-id="4b56f-114">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b56f-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="4b56f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b56f-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="4b56f-116">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="4b56f-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4b56f-117">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="4b56f-117">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> <dt>

<span data-ttu-id="4b56f-118">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="4b56f-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4b56f-119">**UserLogonCred (contextType)**</span><span class="sxs-lookup"><span data-stu-id="4b56f-119">**UserLogonCred (contextType)**</span></span>](schema-userlogoncred-contexttype-element.md)
</dt> </dl>

 

 




