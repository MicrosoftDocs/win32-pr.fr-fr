---
title: Génération de l’UUID
description: La première étape de la définition de l’interface consiste à utiliser l’utilitaire uuidgen pour générer un identificateur unique universel (UUID).
ms.assetid: 870641b7-affc-4de4-bc7f-4c8ca2873fb6
keywords:
- Appel de procédure distante RPC, tâches, génération de l’UUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e263bfe21c4a564106c0d6328c0de891c18bca1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839950"
---
# <a name="generating-the-uuid"></a><span data-ttu-id="1c23c-104">Génération de l’UUID</span><span class="sxs-lookup"><span data-stu-id="1c23c-104">Generating the UUID</span></span>

<span data-ttu-id="1c23c-105">La première étape de la définition de l’interface consiste à utiliser l’utilitaire **uuidgen** pour générer un identificateur unique universel (UUID).</span><span class="sxs-lookup"><span data-stu-id="1c23c-105">The first step in defining the interface is to use the **uuidgen** utility to generate a universally unique identifier (UUID).</span></span> <span data-ttu-id="1c23c-106">Un UUID permet aux applications clientes et serveur de les identifier mutuellement.</span><span class="sxs-lookup"><span data-stu-id="1c23c-106">A UUID enables the client and server applications identify each other.</span></span> <span data-ttu-id="1c23c-107">L’utilitaire **uuidgen** (Uuidgen.exe) est installé automatiquement lorsque vous installez le kit de développement logiciel (SDK) de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="1c23c-107">The **uuidgen** utility (Uuidgen.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="1c23c-108">La commande suivante génère un UUID et crée un fichier de modèle appelé Hello. idl.</span><span class="sxs-lookup"><span data-stu-id="1c23c-108">The following command generates a UUID and creates a template file called Hello.idl.</span></span>

<span data-ttu-id="1c23c-109">**uuidgen/i/ohello.idl**</span><span class="sxs-lookup"><span data-stu-id="1c23c-109">**uuidgen /i /ohello.idl**</span></span>

<span data-ttu-id="1c23c-110">Votre modèle Hello. idl aura l’aspect suivant (avec un UUID différent, bien sûr).</span><span class="sxs-lookup"><span data-stu-id="1c23c-110">Your hello.idl template will look like this (with a different UUID, of course).</span></span>

``` syntax
[
    uuid(7a98c250-6808-11cf-b73b-00aa00b677a7),
    version(1.0)
]
interface INTERFACENAME
{
 
}
```

 

 




