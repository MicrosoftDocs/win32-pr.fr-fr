---
title: ActivateAtStorage
description: Configure le client pour instancier des objets sur le même ordinateur que l’état persistant qu’ils utilisent ou à partir desquels ils sont initialisés.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- valeur de registre COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031946"
---
# <a name="activateatstorage"></a><span data-ttu-id="808f5-104">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="808f5-104">ActivateAtStorage</span></span>

<span data-ttu-id="808f5-105">Configure le client pour instancier des objets sur le même ordinateur que l’état persistant qu’ils utilisent ou à partir desquels ils sont initialisés.</span><span class="sxs-lookup"><span data-stu-id="808f5-105">Configures the client to instantiate objects on the same computer as the persistent state they are using or from which they are initialized.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="808f5-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="808f5-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a><span data-ttu-id="808f5-107">Notes</span><span class="sxs-lookup"><span data-stu-id="808f5-107">Remarks</span></span>

<span data-ttu-id="808f5-108">Il s’agit d’une valeur de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="808f5-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="808f5-109">Toute valeur commençant par « Y » ou « y » indique que **ActivateAtStorage** doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="808f5-109">Any value that begins with 'Y' or 'y' indicates that **ActivateAtStorage** should be used.</span></span>

<span data-ttu-id="808f5-110">La fonctionnalité **ActivateAtStorage** offre un moyen transparent d’autoriser les clients à localiser des objets en cours d’exécution sur le même ordinateur que les données qu’ils utilisent.</span><span class="sxs-lookup"><span data-stu-id="808f5-110">The **ActivateAtStorage** capability provides a transparent way to allow clients to locate running objects on the same computer as the data that they use.</span></span> <span data-ttu-id="808f5-111">Cela réduit le trafic réseau car l’objet effectue des appels de système de fichiers locaux plutôt que des appels sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="808f5-111">This reduces network traffic because the object performs local file-system calls instead of calls across the network.</span></span>

<span data-ttu-id="808f5-112">Quand une valeur est définie pour **ActivateAtStorage**, cela devient le comportement par défaut dans les appels aux fonctions [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) et [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) , ainsi que l’implémentation du moniker de fichier [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="808f5-112">When a value is set for **ActivateAtStorage**, this becomes the default behavior in calls to the [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) and [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) functions, as well as to the file moniker implementation of [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="808f5-113">Dans tous ces appels, la spécification d’une structure [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) remplace la valeur de **ActivateAtStorage** pour la durée de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="808f5-113">In all of these calls, specifying a [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) structure overrides the setting of **ActivateAtStorage** for the duration of the function call.</span></span> <span data-ttu-id="808f5-114">L’appelant peut passer les informations **COSERVERINFO** à **IMoniker :: BindToObject** via la structure de [**liaison \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) .</span><span class="sxs-lookup"><span data-stu-id="808f5-114">The caller can pass **COSERVERINFO** information to **IMoniker::BindToObject** through the [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) structure.</span></span>

<span data-ttu-id="808f5-115">La valeur définie pour **ActivateAtStorage** est également le comportement par défaut lorsque \_ le \_ serveur distant CLSCTX est spécifié si aucune information de Registre pour la classe n’est installée sur l’ordinateur du client.</span><span class="sxs-lookup"><span data-stu-id="808f5-115">The value set for **ActivateAtStorage** is also the default behavior when CLSCTX\_REMOTE\_SERVER is specified if no registry information for the class is installed on the client's computer.</span></span> <span data-ttu-id="808f5-116">Les applications clientes écrites pour tirer parti de **ActivateAtStorage** peuvent donc nécessiter moins d’administration.</span><span class="sxs-lookup"><span data-stu-id="808f5-116">Client applications written to take advantage of **ActivateAtStorage** may therefore require less administration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="808f5-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="808f5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="808f5-118">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="808f5-118">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[<span data-ttu-id="808f5-119">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="808f5-119">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[<span data-ttu-id="808f5-120">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="808f5-120">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[<span data-ttu-id="808f5-121">**COSERVERINFO**</span><span class="sxs-lookup"><span data-stu-id="808f5-121">**COSERVERINFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[<span data-ttu-id="808f5-122">**IMoniker :: BindToObject**</span><span class="sxs-lookup"><span data-stu-id="808f5-122">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[<span data-ttu-id="808f5-123">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="808f5-123">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 