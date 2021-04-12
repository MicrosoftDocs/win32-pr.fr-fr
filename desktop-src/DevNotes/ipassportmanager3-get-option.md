---
description: Récupère la valeur d’une option de connexion Microsoft .NET Passport spécifique.
ms.assetid: a38ffed3-a45b-4bac-8101-3e09f34f3891
title: 'IPassportManager3 :: get_Option, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPassportManager3.get_Option
api_type:
- COM
api_location: ''
ms.openlocfilehash: 289daf9ffbaad872115d0abfd7a618a4f7e44c10
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104392931"
---
# <a name="ipassportmanager3get_option-method"></a><span data-ttu-id="b2985-103">IPassportManager3 :: \_ méthode d’option, méthode</span><span class="sxs-lookup"><span data-stu-id="b2985-103">IPassportManager3::get\_Option method</span></span>

<span data-ttu-id="b2985-104">Récupère la valeur d’une option de connexion Microsoft .NET Passport spécifique.</span><span class="sxs-lookup"><span data-stu-id="b2985-104">Retrieves the value of a specific Microsoft .NET Passport sign-in option.</span></span>

> [!Note]  
> <span data-ttu-id="b2985-105">La méthode d' **\_ option d’extraction** appartient à l’interface [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="b2985-105">The **get\_Option** method belongs to the [**IPassportManager3**](/previous-versions/ms817681(v=msdn.10)) interface.</span></span> <span data-ttu-id="b2985-106">Cette rubrique complète la documentation initiale.</span><span class="sxs-lookup"><span data-stu-id="b2985-106">This topic supplements the initial documentation.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b2985-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2985-107">Syntax</span></span>


```C++
HRESULT get_Option(
  [in]  BSTR    name,
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b2985-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2985-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2985-109">*nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b2985-109">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2985-110">Option de connexion à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b2985-110">The sign-in option to be retrieved.</span></span> <span data-ttu-id="b2985-111">Actuellement, la seule option prise en charge est « iMode ».</span><span class="sxs-lookup"><span data-stu-id="b2985-111">Currently, the only supported option is "iMode".</span></span>

</dd> <dt>

<span data-ttu-id="b2985-112">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b2985-112">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2985-113">Pointeur vers un **Variant** (VT \_ bool) qui reçoit la valeur de l’option.</span><span class="sxs-lookup"><span data-stu-id="b2985-113">A pointer to a **VARIANT** (VT\_BOOL) that receives the value of the option.</span></span> <span data-ttu-id="b2985-114">Cette valeur peut être true ou false.</span><span class="sxs-lookup"><span data-stu-id="b2985-114">This value can be True or False.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2985-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2985-115">Return value</span></span>

<span data-ttu-id="b2985-116">Retourne \_ la valeur OK lorsque la méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="b2985-116">Returns S\_OK when the method succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2985-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b2985-117">Remarks</span></span>

<span data-ttu-id="b2985-118">Cette méthode est fournie avec les versions antérieures du kit de développement logiciel (SDK) Passport.</span><span class="sxs-lookup"><span data-stu-id="b2985-118">This method ships with older versions of the Passport SDK.</span></span>

 

 
