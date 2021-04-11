---
title: DefaultIcon
description: Fournit des informations sur l’icône par défaut pour les présentations sous forme d’objets.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- Clé de Registre DefaultIcon COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031911"
---
# <a name="defaulticon"></a><span data-ttu-id="13d39-104">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="13d39-104">DefaultIcon</span></span>

<span data-ttu-id="13d39-105">Fournit des informations sur l’icône par défaut pour les présentations sous forme d’objets.</span><span class="sxs-lookup"><span data-stu-id="13d39-105">Provides default icon information for iconic presentations of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="13d39-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="13d39-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a><span data-ttu-id="13d39-107">Notes</span><span class="sxs-lookup"><span data-stu-id="13d39-107">Remarks</span></span>

<span data-ttu-id="13d39-108">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le chemin d’accès complet au nom de l’exécutable de l’application d’objet et l’index de ressource de l’icône dans l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="13d39-108">This is a **REG\_SZ** value that specifies the full path to the executable name of the object application and the resource index of the icon within the executable.</span></span>

<span data-ttu-id="13d39-109">**DefaultIcon** identifie l’icône à utiliser lorsque, par exemple, un contrôle est réduit à une icône.</span><span class="sxs-lookup"><span data-stu-id="13d39-109">**DefaultIcon** identifies the icon to use when, for example, a control is minimized to an icon.</span></span> <span data-ttu-id="13d39-110">Cette entrée contient le chemin d’accès complet au nom de l’exécutable de l’application serveur et l’index de ressource de l’icône dans l’exécutable.</span><span class="sxs-lookup"><span data-stu-id="13d39-110">This entry contains the full path to the executable name of the server application and the resource index of the icon within the executable.</span></span> <span data-ttu-id="13d39-111">Les applications peuvent utiliser les informations fournies par **DefaultIcon** pour obtenir un descripteur d’icône avec [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span><span class="sxs-lookup"><span data-stu-id="13d39-111">Applications can use the information provided by **DefaultIcon** to obtain an icon handle with [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span></span>

 

 