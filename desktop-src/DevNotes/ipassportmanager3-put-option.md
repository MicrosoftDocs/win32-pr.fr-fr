---
description: Définit une option de connexion Microsoft .NET Passport spécifique.
ms.assetid: 5ec79faa-1c74-42a4-b964-ea15edacda79
title: IPassportManager3 ::p méthode ut_Option
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.put_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 52a1324c4b1a04a207b5bccac1a95bcd060be8ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950424"
---
# <a name="ipassportmanager3put_option-method"></a><span data-ttu-id="311e7-103">IPassportManager3 ::p \_ méthode d’option ut</span><span class="sxs-lookup"><span data-stu-id="311e7-103">IPassportManager3::put\_Option method</span></span>

<span data-ttu-id="311e7-104">Définit une option de connexion Microsoft .NET Passport spécifique.</span><span class="sxs-lookup"><span data-stu-id="311e7-104">Sets a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="311e7-105">La méthode **put \_ option** appartient à l’interface [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="311e7-105">The **put\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="311e7-106">Cette rubrique complète la documentation initiale.</span><span class="sxs-lookup"><span data-stu-id="311e7-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="311e7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="311e7-107">Syntax</span></span>


```C++
HRESULT put_Option(
   BSTR    name,
   VARIANT newVal
);
```



## <a name="parameters"></a><span data-ttu-id="311e7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="311e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="311e7-109">*name*</span><span class="sxs-lookup"><span data-stu-id="311e7-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="311e7-110">Option de connexion à définir.</span><span class="sxs-lookup"><span data-stu-id="311e7-110">The sign-in option to be set.</span></span> <span data-ttu-id="311e7-111">Actuellement, la seule option prise en charge est iMode.</span><span class="sxs-lookup"><span data-stu-id="311e7-111">Currently, the only supported option is iMode.</span></span>

</dd> <dt>

<span data-ttu-id="311e7-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="311e7-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="311e7-113">**Variante** (VT \_ bool) qui spécifie la nouvelle valeur de l’option.</span><span class="sxs-lookup"><span data-stu-id="311e7-113">A **VARIANT** (VT\_BOOL) that specifies the new value for the option.</span></span> <span data-ttu-id="311e7-114">Cette valeur peut être true ou false.</span><span class="sxs-lookup"><span data-stu-id="311e7-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="311e7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="311e7-115">Return value</span></span>

<span data-ttu-id="311e7-116">Retourne \_ la valeur OK lorsque la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="311e7-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="311e7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="311e7-117">Remarks</span></span>

<span data-ttu-id="311e7-118">Cette méthode est fournie avec les versions antérieures du kit de développement logiciel (SDK) Passport.</span><span class="sxs-lookup"><span data-stu-id="311e7-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
