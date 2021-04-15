---
title: LocalServer32
description: Spécifie le chemin d’accès complet à une application serveur locale 32 bits.
ms.assetid: 5d922230-f53d-4bf9-be50-c8c00f45b7a8
keywords:
- Clé de registre LocalServer32 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd068f51f33b6c283384198c0206bc9c3b6357f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508166"
---
# <a name="localserver32"></a><span data-ttu-id="5b5a0-104">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="5b5a0-104">LocalServer32</span></span>

<span data-ttu-id="5b5a0-105">Spécifie le chemin d’accès complet à une application serveur locale 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-105">Specifies the full path to a 32-bit local server application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5b5a0-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="5b5a0-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer32
         (Default) = path
         ServerExecutable = path
```

## <a name="remarks"></a><span data-ttu-id="5b5a0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5b5a0-107">Remarks</span></span>

<span data-ttu-id="5b5a0-108">La valeur **ServerExecutable** , qui est de type **reg \_ SZ** et est prise en charge à partir de Windows Server 2003, fonctionne conjointement avec la sous-clé **LocalServer32** pour éviter toute ambiguïté lors de l’utilisation de la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="5b5a0-108">The **ServerExecutable** value, which is of type **REG\_SZ** and is supported starting with Windows Server 2003, works in conjunction with the **LocalServer32** subkey to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="5b5a0-109">**LocalServer32** spécifie l’emplacement de l’application de serveur com à lancer, et ces informations sont transmises en tant que premier paramètre *lpApplicationName* pour **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-109">**LocalServer32** specifies the location of the COM server application to launch, and this information is passed as the first parameter *lpApplicationName* for **CreateProcess**.</span></span> <span data-ttu-id="5b5a0-110">Selon l’implémentation de **CreateProcess**, ces informations peuvent être ambiguës.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-110">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="5b5a0-111">Pour cette raison, si **ServerExecutable** est spécifié, com transmet la valeur nommée **ServerExecutable** au paramètre *lpApplicationName* de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-111">For this reason, if **ServerExecutable** is specified, COM passes the **ServerExecutable** named value to the *lpApplicationName* parameter of **CreateProcess**.</span></span> <span data-ttu-id="5b5a0-112">Si **ServerExecutable** n’est pas spécifié, com transmet **null** comme valeur pour le premier paramètre de **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-112">If **ServerExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

<span data-ttu-id="5b5a0-113">Pour garantir la sécurité du système, utilisez des chaînes entre guillemets dans le chemin d’accès pour indiquer l’emplacement où le nom de fichier exécutable se termine et les arguments commencent.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-113">To help provide system security, use quoted strings in the path to indicate where the executable filename ends and the arguments begin.</span></span> <span data-ttu-id="5b5a0-114">Par exemple, au lieu de spécifier le chemin d’accès suivant comme entrée **LocalServer32** :</span><span class="sxs-lookup"><span data-stu-id="5b5a0-114">For example, instead of specifying the following path as the **LocalServer32** entry:</span></span>

<span data-ttu-id="5b5a0-115">« C : \\ Program Files \\ fichiers de la société \\Application.exe param1 param2 »</span><span class="sxs-lookup"><span data-stu-id="5b5a0-115">"C:\\Program Files\\Company Files\\Application.exe param1 param2"</span></span>

<span data-ttu-id="5b5a0-116">Spécifiez le chemin d’accès à l’aide de la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="5b5a0-116">specify the path using the following syntax:</span></span>

<span data-ttu-id="5b5a0-117">" \\ " C : \\ Program Files \\ fichiers de la société \\Application.exe\\ "param1 param2"</span><span class="sxs-lookup"><span data-stu-id="5b5a0-117">"\\"C:\\Program Files\\Company Files\\Application.exe\\" param1 param2"</span></span>

<span data-ttu-id="5b5a0-118">COM ajoute l’indicateur « -Embedding » à la chaîne, de sorte que l’application qui utilise les indicateurs doit analyser l’intégralité de la chaîne et vérifier l’indicateur d’incorporation.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-118">COM appends the "-Embedding" flag to the string, so the application that uses flags needs to parse the whole string and check for the -Embedding flag.</span></span>

<span data-ttu-id="5b5a0-119">Lorsque COM démarre un serveur local 32 bits, le serveur doit inscrire un objet de classe dans un délai écoulé défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-119">When COM starts a 32-bit local server, the server must register a class object within an elapsed time set by the user.</span></span> <span data-ttu-id="5b5a0-120">Par défaut, la valeur du temps écoulé doit être d’au moins 5 minutes, en millisecondes, mais ne peut pas dépasser le nombre de millisecondes dans 30 jours.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-120">By default, the elapsed time value must be at least 5 minutes, in milliseconds, but cannot exceed the number of milliseconds in 30 days.</span></span> <span data-ttu-id="5b5a0-121">En général, les applications ne doivent pas définir cette valeur, qui se trouve dans l’entrée HKEY de l' **\_ ordinateur local de l' \_ ordinateur \\ \\ Microsoft \\ COM2 \\ ServerStartElapsedTime** .</span><span class="sxs-lookup"><span data-stu-id="5b5a0-121">Applications typically should not set this value, which is in the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\COM2\\ServerStartElapsedTime** entry.</span></span>

<span data-ttu-id="5b5a0-122">Les entrées requises pour les serveurs locaux 32 bits sont [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32** et [**Insertable**](insertable.md).</span><span class="sxs-lookup"><span data-stu-id="5b5a0-122">The required entries for 32-bit local servers are [**InprocHandler32**](inprochandler32.md), [**LocalServer**](localserver.md), **LocalServer32**, and [**Insertable**](insertable.md).</span></span>

<span data-ttu-id="5b5a0-123">Si un conteneur recherche un serveur local dans le registre, un serveur local 32 bits est prioritaire sur un serveur local de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-123">If a container is searching the registry for a local server, a 32-bit local server has priority over a 16-bit local server.</span></span>

<span data-ttu-id="5b5a0-124">Si vous implémentez des classes en tant que services, vous devez savoir que la valeur nommée [**LocalService**](localservice.md) est utilisée de préférence à la clé **LocalServer32** pour l’activation locale et distante requestsâ» si **LocalService** existe et qu’il fait référence à un service valide, la clé **LocalServer32** est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5b5a0-124">If you are implementing classes as services, you should be aware that the [**LocalService**](localservice.md) named value is used in preference to the **LocalServer32** key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b5a0-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b5a0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b5a0-126">**LocalServer**</span><span class="sxs-lookup"><span data-stu-id="5b5a0-126">**LocalServer**</span></span>](localserver.md)
</dt> <dt>

[<span data-ttu-id="5b5a0-127">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="5b5a0-127">**LocalService**</span></span>](localservice.md)
</dt> </dl>

 

 