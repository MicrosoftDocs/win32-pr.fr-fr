---
title: DllSurrogateExecutable
description: Permet aux serveurs DLL de s’exécuter dans un processus de substitution personnalisé, conjointement avec la valeur de Registre DllSurrogate. Si DllSurrogateExecutable n’est pas spécifié, COM transmet NULL comme valeur pour le premier paramètre de la fonction CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Valeur de Registre DllSurrogateExecutable COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106510101"
---
# <a name="dllsurrogateexecutable"></a><span data-ttu-id="e3909-105">DllSurrogateExecutable</span><span class="sxs-lookup"><span data-stu-id="e3909-105">DllSurrogateExecutable</span></span>

<span data-ttu-id="e3909-106">Permet aux serveurs DLL de s’exécuter dans un processus de substitution personnalisé, conjointement avec la valeur de Registre [**DllSurrogate**](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="e3909-106">Enables DLL servers to run in a custom surrogate process, in conjunction with the [**DllSurrogate**](dllsurrogate.md) registry value.</span></span> <span data-ttu-id="e3909-107">Si **DllSurrogateExecutable** n’est pas spécifié, com transmet **null** comme valeur pour le premier paramètre de la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="e3909-107">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e3909-108">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="e3909-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a><span data-ttu-id="e3909-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e3909-109">Remarks</span></span>

<span data-ttu-id="e3909-110">Cette valeur est de type **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="e3909-110">This value is of type **REG\_SZ**.</span></span> <span data-ttu-id="e3909-111">Il fonctionne conjointement avec la valeur [**DllSurrogate**](dllsurrogate.md) pour éviter toute ambiguïté lors de l’utilisation de la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="e3909-111">It works in conjunction with the [**DllSurrogate**](dllsurrogate.md) value to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="e3909-112">**DllSurrogate** indique si un substitut personnalisé doit être utilisé, et ces informations sont passées en tant que premier paramètre pour **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="e3909-112">**DllSurrogate** indicates whether a custom surrogate needs to be used, and this information is passed as the first parameter for **CreateProcess**.</span></span> <span data-ttu-id="e3909-113">Selon l’implémentation de **CreateProcess**, ces informations peuvent être ambiguës.</span><span class="sxs-lookup"><span data-stu-id="e3909-113">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="e3909-114">Si **DllSurrogateExecutable** est spécifié, com transmet la valeur en tant que premier paramètre de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="e3909-114">If **DllSurrogateExecutable** is specified, COM passes the value as the first parameter of **CreateProcess**.</span></span> <span data-ttu-id="e3909-115">Si **DllSurrogateExecutable** n’est pas spécifié, com transmet **null** comme valeur pour le premier paramètre de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="e3909-115">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3909-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e3909-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3909-117">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="e3909-117">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="e3909-118">Substituts de DLL</span><span class="sxs-lookup"><span data-stu-id="e3909-118">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="e3909-119">**DllSurrogate**</span><span class="sxs-lookup"><span data-stu-id="e3909-119">**DllSurrogate**</span></span>](dllsurrogate.md)
</dt> <dt>

[<span data-ttu-id="e3909-120">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="e3909-120">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 