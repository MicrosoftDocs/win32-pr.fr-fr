---
title: CallFailureLoggingLevel
description: Définit le niveau de détail des entrées du journal des événements sur les appels ayant échoué aux composants.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- Valeur de Registre CallFailureLoggingLevel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839770"
---
# <a name="callfailurelogginglevel"></a><span data-ttu-id="3e334-104">CallFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="3e334-104">CallFailureLoggingLevel</span></span>

<span data-ttu-id="3e334-105">Définit le niveau de détail des entrées du journal des événements sur les appels ayant échoué aux composants.</span><span class="sxs-lookup"><span data-stu-id="3e334-105">Sets the verbosity of event log entries about failed calls to components.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3e334-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="3e334-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="3e334-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3e334-107">Remarks</span></span>

<span data-ttu-id="3e334-108">Il s’agit d’une valeur de **Registre \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="3e334-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="3e334-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e334-109">Value</span></span> | <span data-ttu-id="3e334-110">Description</span><span class="sxs-lookup"><span data-stu-id="3e334-110">Description</span></span>                                                                            |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e334-111">1</span><span class="sxs-lookup"><span data-stu-id="3e334-111">1</span></span>     | <span data-ttu-id="3e334-112">Consignez toujours les échecs lors d’un appel dans le processus serveur COM.</span><span class="sxs-lookup"><span data-stu-id="3e334-112">Always log failures during a call in the COM Server process.</span></span>                           |
| <span data-ttu-id="3e334-113">2</span><span class="sxs-lookup"><span data-stu-id="3e334-113">2</span></span>     | <span data-ttu-id="3e334-114">Ne consigne jamais de défaillances au cours d’un appel dans le processus serveur COM.</span><span class="sxs-lookup"><span data-stu-id="3e334-114">Never log failures during a call in the COM Server process.</span></span> <span data-ttu-id="3e334-115">Il s’agit de la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3e334-115">This is the default value.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3e334-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e334-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e334-117">Définition de la sécurité pour les applications COM</span><span class="sxs-lookup"><span data-stu-id="3e334-117">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




