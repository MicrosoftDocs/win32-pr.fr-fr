---
title: Handles de liaison automatiques
description: Les handles de liaison automatiques sont utiles lorsque l’application ne nécessite pas de serveur spécifique et lorsqu’il n’est pas nécessaire de conserver les informations d’État entre le client et le serveur.
ms.assetid: ba049369-6c8b-4313-a266-e0364a30056e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fe83d3f9029e0384c87e5e409583ff70f1e91ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316115"
---
# <a name="automatic-binding-handles"></a><span data-ttu-id="364b6-103">Handles de liaison automatiques</span><span class="sxs-lookup"><span data-stu-id="364b6-103">Automatic Binding Handles</span></span>

<span data-ttu-id="364b6-104">Les handles de liaison automatiques sont utiles lorsque l’application ne nécessite pas de serveur spécifique et lorsqu’il n’est pas nécessaire de conserver les informations d’État entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="364b6-104">Automatic binding handles are useful when the application does not require a specific server and when it does not need to maintain any state information between the client and server.</span></span> <span data-ttu-id="364b6-105">Lorsque vous utilisez un handle de liaison automatique, vous n’êtes pas obligé d’écrire du code d’application cliente pour gérer la liaison et les handles. il vous suffit de spécifier l’utilisation du handle de liaison automatique dans le fichier de configuration de l’application (ACF).</span><span class="sxs-lookup"><span data-stu-id="364b6-105">When you use an automatic binding handle, you do not have to write any client application code to deal with binding and handles—you simply specify the use of the automatic binding handle in the application configuration file (ACF).</span></span> <span data-ttu-id="364b6-106">Le stub définit ensuite le handle et gère la liaison.</span><span class="sxs-lookup"><span data-stu-id="364b6-106">The stub then defines the handle and manages the binding.</span></span>

<span data-ttu-id="364b6-107">Par exemple, une opération d’horodatage peut être implémentée à l’aide d’un handle automatique.</span><span class="sxs-lookup"><span data-stu-id="364b6-107">For example, a time-stamp operation can be implemented using an auto handle.</span></span> <span data-ttu-id="364b6-108">Il ne fait aucune différence avec l’application cliente que le serveur lui fournit avec l’horodatage, car elle peut accepter l’heure de n’importe quel serveur disponible.</span><span class="sxs-lookup"><span data-stu-id="364b6-108">It makes no difference to the client application which server provides it with the time stamp because it can accept the time from any available server.</span></span>

> [!Note]  
> <span data-ttu-id="364b6-109">Les handles automatiques ne sont pas pris en charge pour la plateforme Macintosh.</span><span class="sxs-lookup"><span data-stu-id="364b6-109">Auto handles are not supported for the Macintosh platform.</span></span>

 

<span data-ttu-id="364b6-110">Vous spécifiez l’utilisation de handles auto en incluant l’attribut de \[ [**\_ gestion automatique**](/windows/desktop/Midl/auto-handle) \] dans le CCP.</span><span class="sxs-lookup"><span data-stu-id="364b6-110">You specify the use of auto handles by including the \[[**auto\_handle**](/windows/desktop/Midl/auto-handle)\] attribute in the ACF.</span></span> <span data-ttu-id="364b6-111">L’exemple d’horodatage utilise le ACF suivant :</span><span class="sxs-lookup"><span data-stu-id="364b6-111">The time-stamp example uses the following ACF:</span></span>

``` syntax
/* ACF file */
[
  auto_handle
]
interface autoh
{
}
```

<span data-ttu-id="364b6-112">Lorsque le ACF n’inclut aucun autre attribut de handle et que les procédures distantes n’utilisent pas de handles explicites, le compilateur MIDL utilise des handles automatiques par défaut.</span><span class="sxs-lookup"><span data-stu-id="364b6-112">When the ACF does not include any other handle attribute, and when the remote procedures do not use explicit handles, the MIDL compiler uses automatic handles by default.</span></span> <span data-ttu-id="364b6-113">Il utilise également des handles automatiques comme valeur par défaut lorsque le ACF n’est pas présent.</span><span class="sxs-lookup"><span data-stu-id="364b6-113">It also uses automatic handles as the default when the ACF is not present.</span></span>

<span data-ttu-id="364b6-114">Les procédures distantes sont spécifiées dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="364b6-114">The remote procedures are specified in the IDL file.</span></span> <span data-ttu-id="364b6-115">Le descripteur automatique ne doit pas apparaître en tant qu’argument de la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="364b6-115">The auto handle must not appear as an argument to the remote procedure.</span></span> <span data-ttu-id="364b6-116">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="364b6-116">For example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid (6B29FC40-CA47-1067-B31D-00DD010662DA),
  version(1.0),
  pointer_default(unique)
]
interface autoh
{
  void GetTime([out] long * time);
  void Shutdown(void);
}
```

<span data-ttu-id="364b6-117">L’avantage du descripteur automatique est que le développeur n’a pas besoin d’écrire du code pour gérer le descripteur ; les stubs gèrent automatiquement la liaison.</span><span class="sxs-lookup"><span data-stu-id="364b6-117">The benefit of the auto handle is that the developer does not have to write any code to manage the handle; the stubs manage the binding automatically.</span></span> <span data-ttu-id="364b6-118">Cela est très différent de l' [exemple Hello, World](tutorial.md), où le client gère le handle primitif implicite défini dans le ACF et doit appeler plusieurs fonctions runtime pour établir le handle de liaison.</span><span class="sxs-lookup"><span data-stu-id="364b6-118">This is significantly different from the [Hello, World example](tutorial.md), where the client manages the implicit primitive handle defined in the ACF and must call several run-time functions to establish the binding handle.</span></span>

 

 