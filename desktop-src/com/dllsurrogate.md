---
title: DllSurrogate
description: Permet aux serveurs DLL de s’exécuter dans un processus de substitution. Si une chaîne vide est spécifiée, le substitut fourni par le système est utilisé ; Sinon, la valeur spécifie le chemin d’accès du substitut à utiliser.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- Valeur de Registre DllSurrogate COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382955"
---
# <a name="dllsurrogate"></a><span data-ttu-id="ade09-105">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="ade09-105">DllSurrogate</span></span>

<span data-ttu-id="ade09-106">Permet aux serveurs DLL de s’exécuter dans un processus de substitution.</span><span class="sxs-lookup"><span data-stu-id="ade09-106">Enables DLL servers to run in a surrogate process.</span></span> <span data-ttu-id="ade09-107">Si une chaîne vide est spécifiée, le substitut fourni par le système est utilisé ; Sinon, la valeur spécifie le chemin d’accès du substitut à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ade09-107">If an empty string is specified, the system-supplied surrogate is used; otherwise, the value specifies the path of the surrogate to be used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ade09-108">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="ade09-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a><span data-ttu-id="ade09-109">Notes</span><span class="sxs-lookup"><span data-stu-id="ade09-109">Remarks</span></span>

<span data-ttu-id="ade09-110">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie que la classe est une dll qui doit être activée dans un processus de substitution et le processus de substitution à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ade09-110">This is a **REG\_SZ** value that specifies that the class is a DLL that is to be activated in a surrogate process, and the surrogate process to be used.</span></span> <span data-ttu-id="ade09-111">Pour utiliser le processus de substitution générique fourni par le système, définissez le *chemin d’accès* à une chaîne vide ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ade09-111">To use the system-supplied generic surrogate process, set *path* to an empty string or **NULL**.</span></span> <span data-ttu-id="ade09-112">Pour spécifier un autre processus de substitution, définissez *path* sur le chemin d’accès du substitut.</span><span class="sxs-lookup"><span data-stu-id="ade09-112">To specify another surrogate process, set *path* to the path of the surrogate.</span></span> <span data-ttu-id="ade09-113">Comme dans la spécification du chemin d’accès d’un serveur sous la clé [**LocalServer32**](localserver32.md) , une spécification de chemin d’accès complet n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ade09-113">As in the specification of the path of a server under the [**LocalServer32**](localserver32.md) key, a full path specification is not necessary.</span></span> <span data-ttu-id="ade09-114">Le substitut doit être écrit pour communiquer correctement avec le service DCOM, comme décrit dans [écriture d’un substitut personnalisé](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="ade09-114">The surrogate must be written to properly communicate with the DCOM service as described in [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

<span data-ttu-id="ade09-115">La valeur **DllSurrogate** doit être présente pour qu’un serveur dll soit activé dans un substitut.</span><span class="sxs-lookup"><span data-stu-id="ade09-115">The **DllSurrogate** value must be present for a DLL server to be activated in a surrogate.</span></span> <span data-ttu-id="ade09-116">L’activation fait référence à un appel à [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)ou [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="ade09-116">Activation refers to a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage), or [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="ade09-117">L’exécution de dll dans un processus de substitution offre les avantages d’une implémentation exécutable, y compris l’isolation des erreurs, la possibilité de traiter plusieurs clients simultanément et d’autoriser le serveur à fournir des services aux clients distants dans un environnement distribué.</span><span class="sxs-lookup"><span data-stu-id="ade09-117">Running DLLs in a surrogate process provides the benefits of an executable implementation, including fault isolation, the ability to serve multiple clients simultaneously, and allowing the server to provide services to remote clients in a distributed environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ade09-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ade09-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ade09-119">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="ade09-119">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="ade09-120">Substituts de DLL</span><span class="sxs-lookup"><span data-stu-id="ade09-120">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="ade09-121">**DllSurrogateExecutable**</span><span class="sxs-lookup"><span data-stu-id="ade09-121">**DllSurrogateExecutable**</span></span>](dllsurrogateexecutable.md)
</dt> <dt>

[<span data-ttu-id="ade09-122">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="ade09-122">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 