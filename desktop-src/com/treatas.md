---
title: TreatAs
description: Spécifie le CLSID d’une classe qui peut émuler la classe actuelle.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Traiter la clé de registre COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840282"
---
# <a name="treatas"></a><span data-ttu-id="bd753-104">TreatAs</span><span class="sxs-lookup"><span data-stu-id="bd753-104">TreatAs</span></span>

<span data-ttu-id="bd753-105">Spécifie le CLSID d’une classe qui peut émuler la classe actuelle.</span><span class="sxs-lookup"><span data-stu-id="bd753-105">Specifies the CLSID of a class that can emulate the current class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="bd753-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="bd753-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a><span data-ttu-id="bd753-107">Notes</span><span class="sxs-lookup"><span data-stu-id="bd753-107">Remarks</span></span>

<span data-ttu-id="bd753-108">Il s’agit d’une valeur de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="bd753-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="bd753-109">L’émulation est la possibilité pour une application d’ouvrir et de modifier un objet d’une classe différente, tout en conservant le format d’origine de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bd753-109">Emulation is the ability of one application to open and edit an object of a different class, while retaining the original format of the object.</span></span> <span data-ttu-id="bd753-110">La résolution se produit sur l’ordinateur local. par conséquent, dans le cas de l’activation à distance, la résolution se produit sur l’ordinateur client à l’aide du CLSID spécifié par **TreatAs**.</span><span class="sxs-lookup"><span data-stu-id="bd753-110">Resolution occurs on the local computer, so in remote activation case, resolution occurs on the client computer using the CLSID specified by **TreatAs**.</span></span>

<span data-ttu-id="bd753-111">DCOM examine le registre local pour **traiteras**, même si vous appelez la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) et spécifiez un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="bd753-111">DCOM looks at the local registry for **TreatAs**, even if you call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function and specify a remote server.</span></span> <span data-ttu-id="bd753-112">Cela signifie que si vous avez une entrée **TreatAs** pour Class1 à traiter comme Classe2 sur votre ordinateur local, mais que vous appelez **CoCreateInstance** pour créer une instance de Class1 et que vous spécifiez un serveur distant, DCOM tente de créer une instance de Class2 sur le serveur distant, même si Class2 n’est pas inscrit sur le serveur distant, ce qui entraîne l’échec de l’appel à **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="bd753-112">This means that if you have a **TreatAs** entry for Class1 to be treated as Class2 on your local computer, but you call **CoCreateInstance** to create an instance of Class1 and you specify a remote server, DCOM will try to create an instance of Class2 on the remote server, even if Class2 is not registered on the remote server, which will cause the call to **CoCreateInstance** to fail.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd753-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd753-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd753-114">**Traitement autotraité**</span><span class="sxs-lookup"><span data-stu-id="bd753-114">**AutoTreatAs**</span></span>](autotreatas.md)
</dt> <dt>

[<span data-ttu-id="bd753-115">**CoGetTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="bd753-115">**CoGetTreatAsClass**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[<span data-ttu-id="bd753-116">**CoTreatAsClass**</span><span class="sxs-lookup"><span data-stu-id="bd753-116">**CoTreatAsClass**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




