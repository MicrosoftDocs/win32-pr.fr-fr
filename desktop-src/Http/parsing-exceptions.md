---
title: Analyse des exceptions
description: L’API serveur HTTP fournit des clés de Registre pour prendre en charge l’analyse des exceptions à la spécification HTTP/1.1 pour la compatibilité descendante.
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- Analyse des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa071f141539a159d09f6a53f2e78a81bf75327b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940072"
---
# <a name="parsing-exceptions"></a><span data-ttu-id="ba088-104">Analyse des exceptions</span><span class="sxs-lookup"><span data-stu-id="ba088-104">Parsing Exceptions</span></span>

<span data-ttu-id="ba088-105">L’API serveur HTTP fournit des clés de Registre pour prendre en charge l’analyse des exceptions à la spécification HTTP/1.1 pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="ba088-105">HTTP Server API provides registry keys to support parsing exceptions to the HTTP/1.1 specification for backward compatibility.</span></span> <span data-ttu-id="ba088-106">Ces exceptions ne sont pas activées par défaut et doivent être activées au cas par cas, lorsque le serveur rencontre des problèmes de compatibilité avec les clients HTTP.</span><span class="sxs-lookup"><span data-stu-id="ba088-106">These exceptions are not enabled by default and should be enabled only on a case-by-case basis, when the server experiences compatibility issues with HTTP clients.</span></span> <span data-ttu-id="ba088-107">Ces valeurs sont créées sous l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="ba088-107">These values are created under the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

<span data-ttu-id="ba088-108">Le tableau suivant répertorie les clés de Registre fournies pour prendre en charge les exceptions répertoriées.</span><span class="sxs-lookup"><span data-stu-id="ba088-108">The following table lists registry keys provided to support the exceptions listed.</span></span> <span data-ttu-id="ba088-109">Pour activer une exception, affectez la valeur 1 à la valeur de clé correspondante, puis redémarrez le service HTTP.</span><span class="sxs-lookup"><span data-stu-id="ba088-109">To enable an exception set the corresponding key value to 1 and restart the HTTP service.</span></span>



| <span data-ttu-id="ba088-110">Nom de clé</span><span class="sxs-lookup"><span data-stu-id="ba088-110">Key name</span></span>                              | <span data-ttu-id="ba088-111">Description</span><span class="sxs-lookup"><span data-stu-id="ba088-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba088-112">AllowWeakHeaderNameSyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="ba088-112">AllowWeakHeaderNameSyntax (DWORD)</span></span>     | <span data-ttu-id="ba088-113">Permet à l’analyseur HTTP d’accepter les noms d’en-tête avec des caractères de séparation tels que «  ? ».</span><span class="sxs-lookup"><span data-stu-id="ba088-113">Allows the HTTP parser to accept header names with separator characters such as '?'.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ba088-114">AllowWeakHeaderValueSyntax (DWORD)</span><span class="sxs-lookup"><span data-stu-id="ba088-114">AllowWeakHeaderValueSyntax (DWORD)</span></span>    | <span data-ttu-id="ba088-115">Permet à l’analyseur HTTP d’accepter des valeurs d’en-tête avec des caractères de contrôle bruts (sans séquence d’échappement).</span><span class="sxs-lookup"><span data-stu-id="ba088-115">Allows the HTTP parser to accept header values with raw (unescaped) control characters in it.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="ba088-116">AllowCaseInsensitiveVerbs (DWORD)</span><span class="sxs-lookup"><span data-stu-id="ba088-116">AllowCaseInsensitiveVerbs (DWORD)</span></span>     | <span data-ttu-id="ba088-117">Permet à l’analyseur HTTP d’accepter des méthodes/verbes HTTP en minuscules, tels que « récupérer ».</span><span class="sxs-lookup"><span data-stu-id="ba088-117">Allows the HTTP parser to accept lowercase HTTP methods/verbs such as "get".</span></span>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ba088-118">AllowUnEscapedRestrictedChars (DWORD)</span><span class="sxs-lookup"><span data-stu-id="ba088-118">AllowUnEscapedRestrictedChars (DWORD)</span></span> | <span data-ttu-id="ba088-119">Permet à l’analyseur HTTP d’accepter des caractères de contrôle dans ABSPATH et des chaînes de requête de l’URL.</span><span class="sxs-lookup"><span data-stu-id="ba088-119">Allows the HTTP parser to accept control characters in abspath and query strings of the URL.</span></span> <span data-ttu-id="ba088-120">Dans le cas d’une URL absolue, les caractères de contrôle ne sont pas autorisés dans le nom d’hôte.</span><span class="sxs-lookup"><span data-stu-id="ba088-120">In case of an absolute URL, control characters will not be allowed in the hostname.</span></span> <span data-ttu-id="ba088-121">Toutes les versions des URL, à savoir UTF8, DBCS et ANSI, autorisent les caractères de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ba088-121">All flavors of URLs, namely UTF8, DBCS and ANSI, will allow control characters.</span></span> <span data-ttu-id="ba088-122">Tous les caractères de contrôle ASCII, à l’exception de NUL (0x00), LF (0x0A), CR (0x0D) et de la tabulation horizontale (0x09), sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="ba088-122">All ASCII control characters except NUL (0x00), LF (0x0a), CR (0x0d) and Horizontal Tab(0x09) will be allowed.</span></span> |



 

 

 




