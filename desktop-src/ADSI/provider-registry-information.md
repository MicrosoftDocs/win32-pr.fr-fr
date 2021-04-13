---
title: Informations de Registre du fournisseur
description: Cette rubrique montre les clés et les valeurs qui doivent être définies lors de l’ajout d’un fournisseur ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790a80964bdcc6111a4c167056a0b85bda23e147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379589"
---
# <a name="provider-registry-information"></a><span data-ttu-id="91727-103">Informations de Registre du fournisseur</span><span class="sxs-lookup"><span data-stu-id="91727-103">Provider Registry Information</span></span>

<span data-ttu-id="91727-104">Le fournisseur est inscrit auprès d’ADSI avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="91727-104">The provider is registered with ADSI with the following keys and values:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

<span data-ttu-id="91727-105">Le fournisseur est inscrit auprès de Windows avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="91727-105">The provider is registered with Windows with the following keys and values:</span></span>

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

<span data-ttu-id="91727-106">L’espace de noms du fournisseur est inscrit auprès de Windows avec les clés et valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="91727-106">The provider namespace is registered with Windows with the following keys and values:</span></span>

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

<span data-ttu-id="91727-107">Dans les paragraphes précédents, le *fournisseur* est l’identificateur de l’objet de niveau supérieur du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="91727-107">In the previous paragraphs, the *provider* is the identifier of the provider's top-level object.</span></span> <span data-ttu-id="91727-108">L' *espace de noms du fournisseur* est l’identificateur de l’objet qui implémente l’espace de noms du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="91727-108">The *provider namespace* is the identifier of the object which implements the provider's namespace.</span></span>

<span data-ttu-id="91727-109">Pour obtenir un exemple spécifique, consultez [installation du composant de l’exemple de fournisseur](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="91727-109">For a specific example, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

 

 




