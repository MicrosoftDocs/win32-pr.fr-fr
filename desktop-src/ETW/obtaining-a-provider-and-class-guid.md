---
description: Pour obtenir un GUID de fournisseur ou des GUID de classe de trace d’événements, vous pouvez utiliser l’outil Uuidgen.exe ou Guidgen.exe.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Obtention d’un GUID de fournisseur et de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12554cdb39459d824bf6622cd9d50e52f8c788d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973427"
---
# <a name="obtaining-a-provider-and-class-guid"></a><span data-ttu-id="c1ae7-103">Obtention d’un GUID de fournisseur et de classe</span><span class="sxs-lookup"><span data-stu-id="c1ae7-103">Obtaining a Provider and Class GUID</span></span>

<span data-ttu-id="c1ae7-104">Pour obtenir un GUID de fournisseur ou des GUID de classe de trace d’événements, vous pouvez utiliser l’outil Uuidgen.exe ou Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="c1ae7-104">To obtain a provider GUID or event trace class GUIDs, you can use the Uuidgen.exe or Guidgen.exe tool.</span></span>

<span data-ttu-id="c1ae7-105">Si vous utilisez l’outil Uuidgen.exe, utilisez l’option-d pour créer une macro définir le \_ GUID C, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c1ae7-105">If you use the Uuidgen.exe tool, use the -d option to create a DEFINE\_GUID C macro, as shown in the following example.</span></span> <span data-ttu-id="c1ae7-106">Pour plus d’informations sur l’utilisation de l’outil Uuidgen.exe, utilisez l’outil- ?</span><span class="sxs-lookup"><span data-stu-id="c1ae7-106">For information about using the Uuidgen.exe tool, use the -?</span></span> <span data-ttu-id="c1ae7-107">option.</span><span class="sxs-lookup"><span data-stu-id="c1ae7-107">option.</span></span> <span data-ttu-id="c1ae7-108">Si vous utilisez la macro définir le \_ GUID C pour définir votre GUID, vous devez inclure \# define INITGUID avant vos définitions GUID, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c1ae7-108">If you use the DEFINE\_GUID C macro to define your GUID, you must include \#define INITGUID before your GUID definitions, as shown in the following example.</span></span>

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

<span data-ttu-id="c1ae7-109">Le kit de développement logiciel (SDK) Microsoft Windows et Microsoft Visual Studio incluent l’outil Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="c1ae7-109">The Microsoft Windows Software Development Kit (SDK) and Microsoft Visual Studio include the Guidgen.exe tool.</span></span> <span data-ttu-id="c1ae7-110">L’outil Guidgen.exe dispose d’une interface utilisateur qui vous permet de sélectionner différents formats.</span><span class="sxs-lookup"><span data-stu-id="c1ae7-110">The Guidgen.exe tool has a user interface that lets you select from several formats.</span></span> <span data-ttu-id="c1ae7-111">Vous devez utiliser le format qui crée un GUID de constante statique, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="c1ae7-111">You should use the format that creates a static constant GUID, as shown in the following example.</span></span>

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



