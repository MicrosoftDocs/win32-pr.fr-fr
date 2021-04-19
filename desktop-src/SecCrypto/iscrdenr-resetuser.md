---
description: Efface le nom d’utilisateur du contrôle de carte à puce.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'ISCrdEnr :: resetUser, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530737"
---
# <a name="iscrdenrresetuser-method"></a><span data-ttu-id="1842c-103">ISCrdEnr :: resetUser, méthode</span><span class="sxs-lookup"><span data-stu-id="1842c-103">ISCrdEnr::resetUser method</span></span>

<span data-ttu-id="1842c-104">La méthode **resetUser** efface le nom d’utilisateur du contrôle de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="1842c-104">The **resetUser** method clears the user name from the smart card control.</span></span>

## <a name="syntax"></a><span data-ttu-id="1842c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1842c-105">Syntax</span></span>


```C++
HRESULT resetUser();
```



## <a name="parameters"></a><span data-ttu-id="1842c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1842c-106">Parameters</span></span>

<span data-ttu-id="1842c-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1842c-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="1842c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1842c-108">Remarks</span></span>

<span data-ttu-id="1842c-109">Cette méthode efface du nom d’utilisateur existant et du certificat précédemment inscrit de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="1842c-109">This method clears any existing user name and previously enrolled certificate from memory.</span></span> <span data-ttu-id="1842c-110">Toutefois, le certificat précédemment inscrit n’est pas supprimé de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="1842c-110">The previously enrolled certificate is not removed from the smart card, however.</span></span>

## <a name="requirements"></a><span data-ttu-id="1842c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1842c-111">Requirements</span></span>



| <span data-ttu-id="1842c-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1842c-112">Requirement</span></span> | <span data-ttu-id="1842c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1842c-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1842c-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1842c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1842c-115">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1842c-115">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1842c-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1842c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1842c-117">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1842c-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1842c-118">DLL</span><span class="sxs-lookup"><span data-stu-id="1842c-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1842c-119"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1842c-119"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="1842c-120">IID</span><span class="sxs-lookup"><span data-stu-id="1842c-120">IID</span></span><br/>                      | <span data-ttu-id="1842c-121">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="1842c-121">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="1842c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1842c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1842c-123">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="1842c-123">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="1842c-124">**ISCrdEnr :: getUserName**</span><span class="sxs-lookup"><span data-stu-id="1842c-124">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="1842c-125">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="1842c-125">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="1842c-126">**ISCrdEnr :: setUserName**</span><span class="sxs-lookup"><span data-stu-id="1842c-126">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




