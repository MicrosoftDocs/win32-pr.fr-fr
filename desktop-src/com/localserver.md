---
title: LocalServer
description: Spécifie le chemin d’accès complet à une application serveur locale 16 bits.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- Clé de Registre LocalServer COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029554"
---
# <a name="localserver"></a><span data-ttu-id="4fbf4-104">LocalServer</span><span class="sxs-lookup"><span data-stu-id="4fbf4-104">LocalServer</span></span>

<span data-ttu-id="4fbf4-105">Spécifie le chemin d’accès complet à une application serveur locale 16 bits.</span><span class="sxs-lookup"><span data-stu-id="4fbf4-105">Specifies the full path to a 16-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4fbf4-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="4fbf4-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a><span data-ttu-id="4fbf4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="4fbf4-107">Remarks</span></span>

<span data-ttu-id="4fbf4-108">Il s’agit d’une valeur de **reg \_ SZ** qui spécifie le chemin d’accès complet et peut inclure tous les arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="4fbf4-108">This is a **REG\_SZ** value that specifies the full path and can include any command-line arguments.</span></span>

<span data-ttu-id="4fbf4-109">COM ajoute l’indicateur « -Embedding » à la chaîne, de sorte que l’application qui utilise les indicateurs doit analyser l’intégralité de la chaîne et vérifier l’indicateur d’incorporation.</span><span class="sxs-lookup"><span data-stu-id="4fbf4-109">COM appends the "-Embedding" flag to the string, so the application that uses flags must parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="4fbf4-110">Pour exécuter un serveur d’objets COM dans un espace mémoire séparé, modifiez la valeur de **LocalServer** comme suit :</span><span class="sxs-lookup"><span data-stu-id="4fbf4-110">To run a COM object server in a separate memory space, change the value of **LocalServer** as follows:</span></span>

<span data-ttu-id="4fbf4-111">**cmd/c Start/Separate** *chemin d’accès \* \* *. exe**</span><span class="sxs-lookup"><span data-stu-id="4fbf4-111">**cmd /c start /separate** *path\*\*\*.exe*\*</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fbf4-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4fbf4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fbf4-113">**LocalServer32**</span><span class="sxs-lookup"><span data-stu-id="4fbf4-113">**LocalServer32**</span></span>](localserver32.md)
</dt> </dl>

 

 




