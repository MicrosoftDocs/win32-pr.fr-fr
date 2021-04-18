---
description: L’objet client représente une relation entre un composant et un produit client.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Objet client
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533084"
---
# <a name="client-object"></a><span data-ttu-id="70271-103">Objet client</span><span class="sxs-lookup"><span data-stu-id="70271-103">Client object</span></span>

<span data-ttu-id="70271-104">L’objet client représente une relation entre un composant et un produit client.</span><span class="sxs-lookup"><span data-stu-id="70271-104">The Client object represents a relationship between a component and client product.</span></span>

<span data-ttu-id="70271-105">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="70271-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="70271-106">Cet objet est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="70271-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="70271-107">Membres</span><span class="sxs-lookup"><span data-stu-id="70271-107">Members</span></span>

<span data-ttu-id="70271-108">L’objet **client** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="70271-108">The **Client** object has these types of members:</span></span>

-   [<span data-ttu-id="70271-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70271-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70271-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="70271-110">Properties</span></span>

<span data-ttu-id="70271-111">L’objet **client** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="70271-111">The **Client** object has these properties.</span></span>



| <span data-ttu-id="70271-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="70271-112">Property</span></span>                                                 | <span data-ttu-id="70271-113">Description</span><span class="sxs-lookup"><span data-stu-id="70271-113">Description</span></span>                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="70271-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="70271-114">**ComponentCode**</span></span>](client-componentcode.md)<br/> | <span data-ttu-id="70271-115">Code du composant en question.</span><span class="sxs-lookup"><span data-stu-id="70271-115">The component code of the component in question.</span></span><br/> |
| [<span data-ttu-id="70271-116">**Context**</span><span class="sxs-lookup"><span data-stu-id="70271-116">**Context**</span></span>](client-context.md)<br/>             | <span data-ttu-id="70271-117">Contexte du produit.</span><span class="sxs-lookup"><span data-stu-id="70271-117">The context of the product.</span></span><br/>                      |
| [<span data-ttu-id="70271-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="70271-118">**ProductCode**</span></span>](client-productcode.md)<br/>     | <span data-ttu-id="70271-119">Produit client du composant en question.</span><span class="sxs-lookup"><span data-stu-id="70271-119">The client product of the component in question.</span></span><br/> |
| [<span data-ttu-id="70271-120">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="70271-120">**UserSID**</span></span>](client-usersid.md)<br/>             | <span data-ttu-id="70271-121">SID de l’utilisateur du composant.</span><span class="sxs-lookup"><span data-stu-id="70271-121">The user SID for the component.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="70271-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70271-122">Requirements</span></span>



| <span data-ttu-id="70271-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70271-123">Requirement</span></span> | <span data-ttu-id="70271-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="70271-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="70271-125">Version</span><span class="sxs-lookup"><span data-stu-id="70271-125">Version</span></span><br/> | <span data-ttu-id="70271-126">Windows Installer 5,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="70271-126">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="70271-127">DLL</span><span class="sxs-lookup"><span data-stu-id="70271-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="70271-128"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70271-128"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="70271-129">IID</span><span class="sxs-lookup"><span data-stu-id="70271-129">IID</span></span><br/>     | <span data-ttu-id="70271-130">IID \_ IClient est défini en tant que 000C1098-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="70271-130">IID\_IClient is defined as 000C1098-0000-0000-C000-000000000046</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="70271-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70271-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70271-132">Utilisation de l’interface d’automatisation</span><span class="sxs-lookup"><span data-stu-id="70271-132">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="70271-133">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="70271-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




